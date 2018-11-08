# LambdaFunction

Lambda function connected with SNS and consuming SES and DynamoDB service. This function sends a reset token to the user who has requested to reset password for their corresponding account.

## The flow

The flow of the diagram is as follows
[![Alt Function_flow](https://github.com/ShreyasKraman/LamdaFunction/LambdaFuncationCall.PNG)]


## Built with

* [TrackXpense](https://github.com/ShreyasKraman/TracXpense) - The webapi which makes SNS event request to call this lambda function
* [Amazon SNS](https://aws.amazon.com/sns/) - Amazon SNS topic sends a push notification which activates the lambda function.
* [Amazon SES](https://aws.amazon.com/ses/) - Lambda function after execution in turn sends mail to the user with reset link
* [Amazon DynamoDB](https://aws.amazon.com/dynamodb/) - Lambda function checks for the user in the dynamodb table and returns the same token if already present in the table, else stores the new token and returns the password link to the user through SES.

## Author

**Shreyas Kalyanaraman** - [Linkedin](https://www.linkedin.com/in/shreyaskalyanaraman)



