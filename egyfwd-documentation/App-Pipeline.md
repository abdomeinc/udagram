# udagram
 EgyFwd Project 03

## App Pipeline

- [Click Here](diagrams/App-Pipeline.png) - to display diagram.

### Continuous Integration
#### GitHub
The developers commit then push their code to the GitHub repository.
Then GitHub (Which is linked to the CircleCI platform) triggers the CircleCI platform when code is pushed to the repository.

#### CircleCI
CircleCI reads the `.circleci/config.yml` file to load the project configuration and to know what steps to be done. In this project there are 2 jobs (frontend & server) to be run by CircleCI.
``
``
- **Frontend**: Runs the `build` script given in the `package.json` file. Then uses AWS CLI to upload Frontend UI assets to Amazon S3.

- **Backend**: Runs the `build` script, exports all environment variables from CircleCI configuration to a `.env` file,
  then runs the `archive` script. Then uses AWS CLI to upload archive to S3.