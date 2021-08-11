#### [Android fundamentals](https://developer.android.com/guide/components/fundamentals)
- there are many languages could be use to create android application including Kotlin, Java, and C++. 
- A software development kit (SDK) is a collection of software development tools in one installable package. They facilitate the creation of applications by having a compiler, debugger and perhaps a software framework.
- Android Package is the Android application package file format used by the Android operating system, and a number of other Android-based operating systems for distribution and installation of mobile apps, mobile games and middleware.
- An Android App Bundle is a publishing format that includes all your app's compiled code and resources, and defers APK generation and signing to Google Play.
- Each Android app lives in its own security sandbox, protected by the following Android security features:
            - The Android operating system is a multi-user Linux system in which each app is a different user.
            - By default, the system assigns each app a unique Linux user ID.
            - Each process has its own virtual machine (VM), so an app's code runs in isolation from other apps.
            - By default, every app runs in its own Linux process.
 -  principle of least privilege: it is the method that the Android system use in implementation, on which each app, by default, has access only to the components that it requires to do its work and no more. 
##### App components: 
There are four different types of app components:
- Activities: An activity is the entry point for interacting with the user. It represents a single screen with a user interface.
- Services: A service is a general-purpose entry point for keeping an app running in the background for all kinds of reasons.
- Broadcast receivers: A broadcast receiver is a component that enables the system to deliver events to the app outside of a regular user flow, allowing the app to respond to system-wide broadcast announcements.
  
- Content providers: A content provider manages a shared set of app data that you can store in the file .

##### Activating components:
- activities, services, and broadcast receivers—are activated by an asynchronous message called an intent, wherase the content providers are activated when targeted by a request from a ContentResolver