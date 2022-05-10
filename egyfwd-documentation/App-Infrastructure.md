# udagram
 EgyFwd Project 03

## App Infrastructure

- [Click Here](diagrams/App-Infrastructure.png) - to display diagram.

### AWS
#### RDS Postgres
The application server uses AWS RDS Postgres as database for storing and retrieving information.

#### Elastic Beanstalk
The application server is deployed on AWS Elastic Beanstalk service. The application is build, archived and uploaded
to and S3 bucket from where Elastic Beanstalk extracts and runs the application on an endpoint.

EB URL: [Click Here](http://egyfwd-udagram-api-dev.eba-v2rrs8pf.us-east-1.elasticbeanstalk.com/)

#### S3 Bucket
The frontend application is deployed using AWS S3 Bucket. The bundled assets are uploaded to an S3 bucket and that
bucket is made publicly readable.

Bucket URL: [Click Here](http://egyfwd-udagram.s3-website-us-east-1.amazonaws.com/)

End users can access the application from the Bucket URL.