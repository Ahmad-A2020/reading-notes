

### Resources:
- [Espresso Testing](https://developer.android.com/training/testing/espresso)
- [Ridiculous superpower: the Espresso Test Recorder](https://developer.android.com/studio/test/espresso-test-recorder)

#### Espresso :
- Definition: Espresso is a testing framework for Android to make it easy to write reliable user interface tests.
- features : Espresso automatically synchronizes your test actions with the user interface of your application. The framework also ensures that your activity is started before the tests run. It also let the test wait until all observed background activities have finished.
- example:  the following is an exa,example of use the framwork
                        @Test
                        public void greeterSaysHello() {
                            onView(withId(R.id.name_field)).perform(typeText("Steve"));
                            onView(withId(R.id.greet_button)).perform(click());
                            onView(withText("Hello Steve!")).check(matches(isDisplayed()));
                        }
- Espresso has basically three components:

        -  ViewMatchers - allows to find view in the current view hierarchy

        -  ViewActions - allows to perform actions on the views

        -  ViewAssertions - allows to assert state of a view
-  The case construct for Espresso tests is the following:

                         onView(ViewMatcher)
                          .perform(ViewAction)
                            .check(ViewAssertion);