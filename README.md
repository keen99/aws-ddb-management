

mvn package

java -cp target/aws-ddb-management-1.0-SNAPSHOT.jar \
com.cfelde.aws.ddb.management.TableThroughput



Configuration:




# AWS DynamoDB table throughput management

Long ago I wrote a blog post about [building a better DynamoDB scaling tool](http://blog.cfelde.com/2014/07/building-a-better-dynamodb-throughput-scaling-tool-part-2/). So I did, but I didn't share it
with anyone. Since then, multiple people have asked me to share it, and now, finally I've given in ;)

The tool as initially released needs some work on moving various parameters into external configuration. But, as is,
it works and I've been using it for a few years now.

I don't expect to spend too much time improving it, and in fact I am myself moving off of DynamoDB. But if you want to help out feel free to send me some pull requests.



# Building the jar

  mvn package



# Configuration

AWS Region (required)
Supported environment variables:   AWS_REGION AWS_DEFAULT_REGION
Support java property:   aws.region property

AWS credentials are supplied via the default AWS credential provider chain - see http://docs.aws.amazon.com/AWSSdkDocsJava/latest/DeveloperGuide/credentials.html


Table configuration:  TBD

State file/table:  TBD



# running the jar

  java -jar target/aws-ddb-management-1.0-SNAPSHOT.jar




# TODO
- be friendly when we dont find a table.

- read tables from external config
  - read tables from a ddb table (create it, manage it for state..)

- read aws config from external config - if not set, use profile, env vars, etc as apropos
 http://docs.aws.amazon.com/AWSSdkDocsJava/latest/DeveloperGuide/credentials.html




