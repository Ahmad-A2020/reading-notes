####  Resources: 
- [Intent Filters](https://developer.android.com/training/basics/intents/filters)

### Allowing Other Apps to Start Your Activity
 - To allow other apps to start your activity in this way, you need to add an <intent-filter> element in your manifest file for the corresponding <activity> element.
 - Add an Intent Filter: The system may send a given Intent to an activity if that activity has an intent filter fulfills the following criteria of the Intent object:
            - Action : A string naming the action to perform. Usually one of the platform-defined values such as ACTION_SEND or ACTION_VIEW.
            - Data: A description of the data associated with the intent.
           - Category:  Provides an additional way to characterize the activity handling the intent, usually related to the user gesture or location from which it's started.
           - Below is an example:
  

         <activity android:name="ShareActivity">
         <intent-filter>
         <action android:name="android.intent.action.SEND"/>
         <category android:name="android.intent.category.DEFAULT"/>
         <data android:mimeType="text/plain"/>
         <data android:mimeType="image/*"/>
         </intent-filter>
         </activity>

- Handle the Intent in Your Activity: In order to decide what action to take in your activity, you can read the Intent that was used to start it.As your activity starts, call getIntent() to retrieve the Intent that started the activity. You can do so at any time during the lifecycle of the activity, but you should generally do so during early callbacks such as onCreate() or onStart().For example: 


    @Override
    protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    
        setContentView(R.layout.main);
    
        // Get the intent that started this activity
        Intent intent = getIntent();
        Uri data = intent.getData();
    
        // Figure out what to do based on the intent type
        if (intent.getType().indexOf("image/") != -1) {
            // Handle intents with image data ...
        } else if (intent.getType().equals("text/plain")) {
            // Handle intents with text ...
        }
    }            

- Return a Result: If you want to return a result to the activity that invoked yours, simply call setResult() to specify the result code and result Intent. When your operation is done and the user should return to the original activity, call finish() to close (and destroy) your activity. For example:


        // Create intent to deliver some kind of result data
        Intent result = new Intent("com.example.RESULT_ACTION", Uri.parse("content://result_uri"));
        setResult(Activity.RESULT_OK, result);
        finish();
