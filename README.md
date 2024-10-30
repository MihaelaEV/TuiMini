Project Overview: 
This is a mini framework with 3 tests for the Tui Mobile Challenge app. The framework is in Java, and uses Appium and Cucumber.

Structure:
The framework is organized with pageobjects, runners, steps, utilities and features

pageobjects contains LoginPage and HomePage 
LoginPage contains locators for the login form, and methods for login
HomePage contains locators for the home page, and methods for navigating the tabs and checking the offers

runners contains TestRunner where we have the run configuration and the reporting

steps contains Hooks, LoginSteps, OfferTypeSteps
in Hooks there are setUp and tearDown methods for setting up and logging in before each test, and closing the app after each test
in LoginSteps there are methods for logging in and assertion
in OfferTypesSteps there are methods for navigating the tabs and verifying offers

utilities contains TestDataReader with methods for reading the loginData.json and formatting the dates

in resources there are the three features login.feature, offer_type.feature and offer_view.feature
login.feature tests the ability to login, asserts the visibility of the login fields, and the tabs on the homepage after login
offer_type.feature checks that in All tab there is at least one hotel and at least one holiday offer
offer_view.feature tests that offers load when user clicks on each one of the tabs

How to run the tests:
Option 1:
1.Open the project in Intellij and Android Studio
2. Turn on a device in Android Studio
3. Connect to Appium (open cmd, enter appium)
4. In Inttelij terminal or Android Studio terminal run mvn test or mvn clean test
5. Report should be visible in target (cucumber-reports.html)

Option 2:
1. In Intellij, create a new configuration run
2. Choose Class TestRunner and save
3. Connect to Appium
4. Open the emulator in Android studio
5. Run the configuration
6. Report should be visible in target 



