### Resources: 
- [Amplify and Kinesis](https://docs.amplify.aws/sdk/analytics/kinesis/q/platform/android/#working-with-the-api)
- [Amplify Getting Started Analytics](https://docs.amplify.aws/lib/analytics/getting-started/q/platform/android/)

#### [lab](https://github.com/Ahmad-A2020/taskmaster):
![lab39](C:\Users\Ahmad\asac\reading-notes\Code-401\ScreenShot\lab39-1.PNG)

### Using Amazon Kinesis

- The two classes KinesisRecorder and KinesisFirehoseRecorder allow you to interface with Amazon Kinesis Data Streams and Amazon Kinesis Data. 
- Amazon Kinesis Data Streams:  is a fully managed service for real-time processing of streaming data at massive scale
- Amazon Kinesis Data Streams Applications:build real-time dashboards, capture exceptions and generate alerts, drive recommendations, and make other real-time business or operational decisions. You can also easily send data to other services such as Amazon Simple Storage Service, Amazon DynamoDB, and Amazon Redshift.
- Amazon Kinesis Data Firehose is a fully managed service for delivering real-time streaming data to destinations such as Amazon Simple Storage Service (Amazon S3) and Amazon Redshift.
- To integrate  Amazon Kinesis including the following libraries in your app/build.gradle dependencies list:
 

              dependencies {
              implementation 'com.amazonaws:aws-android-sdk-kinesis:2.15.+'
              implementation ('com.amazonaws:aws-android-sdk-mobile-client:2.15.+@aar') { transitive = true }
              }

- then , add the following import to the main activity. 


            import com.amazonaws.mobileconnectors.kinesis.kinesisrecorder.*;
            import com.amazonaws.mobile.client.AWSMobileClient;
            import com.amazonaws.regions.Regions;
- To use Kinesis Data Streams in an application, you must set the correct permissions. The following IAM policy allows the user to submit records to a specific data stream, which is identified by ARN.


                {
                "Statement": [{
                    "Effect": "Allow",
                    "Action": "kinesis:PutRecords",
                    "Resource": "arn:aws:kinesis:us-west-2:111122223333:stream/mystream"
                }]
            }
- Working with the API
        - You can use AWSMobileClient to setup the Cognito credentials that are required to authenticate your requests with Amazon Kinesis.
        - Once you have credentials, you can use KinesisRecorder with Amazon Kinesis.
        - To use KinesisFirehoseRecorder, you need to pass the object in a directory where streaming data is saved. 
        - 