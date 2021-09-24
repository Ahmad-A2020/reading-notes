##### REsources: 
- [Introduction to Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)
- [S3 with Amplify](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)
- [S3 Amplify](https://docs.amplify.aws/lib/storage/getting-started/q/platform/android/)
- [Amplify Getting Started](https://docs.amplify.aws/)
- [Android File Picker](https://developer.android.com/guide/topics/providers/document-provider)

#### [lab](https://github.com/Ahmad-A2020/taskmaster):
![lab33](/Code-401/ScreenShot/lab37-1.PNG)

### Introduction to Amazon S3
- Amazon Simple Storage Service (Amazon S3) is storage for the Internet. It is designed to make web-scale computing easier.
- Advantages of using Amazon S3: 
        - Creating buckets – Create and name a bucket that stores data.
        - Storing data – Store an infinite amount of data in a bucket.
        - Downloading data – Download your data or enable others to do so. 
        - Permissions – Grant or deny access to others who want to upload or download data into your Amazon S3 bucket. 
        - Standard interfaces – Use standards-based REST and SOAP interfaces designed to work with any internet-development toolkit.
##### Amazon S3 concepts
- Buckets: A bucket is a container for objects stored in Amazon S3. Every object is contained in a bucket.
- Objects: Objects are the fundamental entities stored in Amazon S3. Objects consist of object data and metadata.
- Keys:   A key is the unique identifier for an object within a bucket. Every object in a bucket has exactly one key.
- Regions:   You can choose the geographical AWS Region where Amazon S3 will store the buckets that you create. 

##### Amazon S3 data consistency model
- Amazon S3 provides strong read-after-write consistency for PUTs and DELETEs of objects in your Amazon S3 bucket in all AWS Regions. This applies to both writes to new objects as well as PUTs that overwrite existing objects and DELETE

### S3 with Amplify: 
- To start provisioning storage resources in the backend, go to your project directory and execute the command: `amplify add storage`
- push your changes to the cloud, execute the command: `amplify push`
- Install Amplify Libraries: add the following dependencies to the app gradle file.
 

                      dependencies {
                      implementation 'com.amplifyframework:aws-storage-s3:1.24.0'
                      implementation 'com.amplifyframework:aws-auth-cognito:1.24.0'
                       }

- Initialize Amplify Storage: Add the following code to your onCreate() method in your application class:


                        Amplify.addPlugin(new AWSCognitoAuthPlugin());
                        Amplify.addPlugin(new AWSS3StoragePlugin());
- Uploading data to your bucket:   To upload to S3 from a data object, specify the key and the data object to be uploaded.

`private void uploadFile() {
``File exampleFile = new File(getApplicationContext().getFilesDir(), "ExampleKey");
`
    try {
        BufferedWriter writer = new BufferedWriter(new FileWriter(exampleFile));
        writer.append("Example file contents");
        writer.close();
    } catch (Exception exception) {
        Log.e("MyAmplifyApp", "Upload failed", exception);
    }

    Amplify.Storage.uploadFile(
            "ExampleKey",
            exampleFile,
            result -> Log.i("MyAmplifyApp", "Successfully uploaded: " + result.getKey()),
            storageFailure -> Log.e("MyAmplifyApp", "Upload failed", storageFailure)
    );
}                       
