Core Framework

         •	The core framework consists of the Page object Model. For each of the App page,
            I have created separate page class. The page specific functionalities are implemented as
            reusable methods inside the page class.
         •	I have also created a class called “BasePage” which contains some of the utility methods 
            like WebDriver Wait, Send Keys,Tap etc.
Page Class package: com.game.pages	
        
         •	BasePage
         •	WelcomePage
         •	SigninPage
         •	LeaguePage
         •	NBABasketBallPage
         •	LeaderPage
         •	PlayerPage
         •	AndroidCapabilities

TestNG	

          •	I have used the TestNG Framework to create & execute the Automation Test case. 
            Appropriate Annotations are being within the Test case.
	
            Test case is located in folder:src/test/java. The name of the test case is RandomPlayer_TC001. 
            
How to execute the Test case
         
          •	 Open the RandomPlayer_TC001 Test case file from the src/test/java .Right Click and
             choose the option TestNG Test to execute the Test case
          •	 Test data is maintained in a separate excel spreadsheet as the test data
             is parameterized in the Test case

              Test data sheet is located in folder: src/main/resources
              The Score.Apk file is located inthe folder:  src/main/resources
 
 Logging
 
           •  For the Logging and Debugging purpose, I have implemented the Log4J Framework.
              All the log information from the test case execution will be captured using the Log4J.

           •  The log4j2.xml is located in the properties folder. Place the log4j2.xml file into the classpath. Only then all the log statements will get logged to console.

MacOS Setup/Consideration:

           • Please follow the below steps to setup the MacOS test infrastructure
               o	Download and Build the iOS App in Local Machine using XCODE
               o	Do the Simulator/Real Device Setup
               o	Download the Appium Desktop
               o	Create Desired Capabilities for iOS

           • Please follow the below steps to execute the test case in Mac Laptop
               o	Use Appium Inspector to Identify the iOS Locators for the below Pages,
               o	Add the iOS Locators using the @iOSFindby in the below pages

                     WelcomePage
                     SigninPage
                     LeaguePage
                     NBABasketBallPage
                     LeaderPage
                     PlayerPage
                     AndroidCapabilities
                    
Below are the list of things that differ from Android and IOS

              1. Capability Setting for IOS
                     cap.setCapability(MobileCapabilityType.DEVICE_NAME, "iphone 6");
                     cap.setCapability(MobileCapabilityType.PLATFORM_NAME, "ios");
                     cap.setCapability(MobileCapabilityType.AUTOMATION_NAME,AutomationName.IOS_XCUI_TEST);
                     cap.setCapability(MobileCapabilityType.APP,  "//users//xcodeclub//Desktop//theScore.app");
                     driver=new IOSDriver<IOSElement>(new URL("http://127.0.0.1:4723/wd/hub"), cap)

              2. Page Factory Pattern for the IOSElements will be 
                 @iOSBy annotation followed by the identified locator value for the webElement
                
              3. Scrolling 
                    Scrolling in ios can be done by using the Dimension class.
                    
