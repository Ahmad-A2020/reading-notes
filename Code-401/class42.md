### Get the last known location

Using the Google Play services location APIs, your app can request the last known location of the user's device. The fused location provider is one of the location APIs in Google Play services.To access the fused location provider, your app's development project must include Google Play services. Download and install the Google Play services component via the SDK Manager and add the library to your project. this happened by adding the following dependency:

            dependencies {
            implementation 'com.google.android.gms:play-services-location:18.0.0'
            }

 - The next step is to Specify app permissions:To protect user privacy, apps that use location services must request location permissions.Android's location permissions deal with two catagories; Foreground location, and Background location. As for foreground location; it used If your app contains a feature that shares or receives location information only once, or for a defined amount of time.
 - Create location services client: In your activity's onCreate() method, create an instance of the Fused Location Provider Client as the following code snippet shows.

 
            private FusedLocationProviderClient fusedLocationClient;

            // ..
            
            @Override
            protected void onCreate(Bundle savedInstanceState) {
            // ...
            
                fusedLocationClient = LocationServices.getFusedLocationProviderClient(this);
            }

- Get the last known location: Once you have created the Location Services client you can get the last known location of a user's device. When your app is connected to these you can use the fused location provider's getLastLocation() method to retrieve the device location. The precision of the location returned by this call is determined by the permission setting you put in your app manifest, as described in the guide on how to request location permissions.


            fusedLocationClient.getLastLocation()
            .addOnSuccessListener(this, new OnSuccessListener<Location>() {
            @Override
            public void onSuccess(Location location) {
            // Got last known location. In some rare situations this can be null.
            if (location != null) {
            // Logic to handle location object
            }
            }
            });
