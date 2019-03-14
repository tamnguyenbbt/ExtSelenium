# ExtSelenium
Extend Selenium with the following added methods. Support .NetCore >=2.1

## Methods
The main extensions are the methods to find elements and xpaths by one anchor element or two anchor elements

###
* public static IList<string> **FindXPathsByTwoAnchors**(this IWebDriver driver, ElementInfo parentAnchorElementInfo, ElementInfo anchorElementInfo, string searchCssSelector, int timeoutInSeconds = 10, DomUtilConfig config = null)
       
* public static string **FindXPathByTwoAnchors**(this IWebDriver driver, ElementInfo parentAnchorElementInfo, ElementInfo anchorElementInfo, string searchCssSelector, int timeoutInSeconds = 10, DomUtilConfig config = null)
        
* public static IList<string> **FindXPathsByAnchor**(this IWebDriver driver, ElementInfo anchorElementInfo, ElementInfo searchElementInfo, int timeoutInSeconds = 10, DomUtilConfig config = null)
        
* public static string **FindXPathByAnchor**(this IWebDriver driver, ElementInfo anchorElementInfo, ElementInfo searchElementInfo, int timeoutInSeconds = 10, DomUtilConfig config = null)
        
* public static IList<IWebElement> **FindElementsByTwoAnchors**(this IWebDriver driver, ElementInfo parentAnchorElementInfo, ElementInfo anchorElementInfo, string searchCssSelector, int timeoutInSeconds = 10, DomUtilConfig config = null)
       
* public static IWebElement **FindElementByTwoAnchors**(this IWebDriver driver, ElementInfo parentAnchorElementInfo, ElementInfo anchorElementInfo, string searchCssSelector, int timeoutInSeconds = 10, DomUtilConfig config = null)
       
* public static IList<IWebElement> **FindElementsByAnchor**(this IWebDriver driver, ElementInfo anchorElementInfo, ElementInfo searchElementInfo, int timeoutInSeconds = 10, DomUtilConfig config = null)
       
* public static IWebElement **FindElementByAnchor**(this IWebDriver driver, ElementInfo anchorElementInfo, ElementInfo searchElementInfo, int timeoutInSeconds = 10, DomUtilConfig config = null)
        
* public static IList<IWebElement> **FindElementsById**(this IWebDriver driver, string id, int timeoutInSeconds = 10)
       
* public static IWebElement **FindElementById**(this IWebDriver driver, string id, int timeoutInSeconds = 10)

* public static IList<IWebElement> **FindElementsByClassName**(this IWebDriver driver, string className, int timeoutInSeconds = 10)
       
* public static IWebElement **FindElementByClassName**(this IWebDriver driver, string className, int timeoutInSeconds = 10)

* public static IList<IWebElement> **FindElementsByName**(this IWebDriver driver, string name, int timeoutInSeconds = 10)
       
* public static IWebElement **FindElementByName**(this IWebDriver driver, string name, int timeoutInSeconds = 10)
        
* public static IList<IWebElement> **FindElementsByTagName**(this IWebDriver driver, string tagName, int timeoutInSeconds = 10)
       
* public static IWebElement **FindElementByTagName**(this IWebDriver driver, string tagName, int timeoutInSeconds = 10)

* public static IList<IWebElement> **FindElementsByCssSelector**(this IWebDriver driver, string cssSelector, int timeoutInSeconds = 10)
        
* public static IWebElement **FindElementByCssSelector***(this IWebDriver driver, string cssSelector, int timeoutInSeconds = 10)
        
* public static IList<IWebElement> **FindElementsByXPath**(this IWebDriver driver, string xPath, int timeoutInSeconds = 10)
        
* public static IWebElement **FindElementByXPath**(this IWebDriver driver, string xPath, int timeoutInSeconds = 10)

* public static IList<IWebElement> **FindElementsByPartialLinkText**(this IWebDriver driver, string partialLinkText, int timeoutInSeconds = 10)
        
* public static IWebElement **FindElementByPartialLinkText**(this IWebDriver driver, string partialLinkText, int timeoutInSeconds = 10)
       
* public static IList<IWebElement> **FindElementsByLinkText**(this IWebDriver driver, string linkText, int timeoutInSeconds = 10)
        
* public static IWebElement **FindElementByLinkText**(this IWebDriver driver, string linkText, int timeoutInSeconds = 10)
        
* public static void **OpenPageByUrl**(this IWebDriver driver, string url)
        
* public static void **SwitchToDefaultContent**(this IWebDriver driver)
        
* public static void **SwitchToParentFrame**(this IWebDriver driver)
        
* public static void **SwitchToFrame**(this IWebDriver driver, string name)
       
* public static IList<string> **GetIFrameNames**(this IWebDriver driver, int timeoutInSeconds = 10)
       
* public static string **GetActiveFrameName**(this IWebDriver driver)
       
* public static string **GetHtmlDocument**(this IWebDriver driver, int timeoutInSeconds = 10)


## Example

	    IWebDriver driver = new ChromeDriver();
        string url = "https://accounts.google.com/signup/v2/webcreateaccount?hl=en-GB&flowName=GlifWebSignIn&flowEntry=SignUp";
        driver.OpenPageByUrl(url);
            
        ElementInfo anchorInfo = new ElementInfo("div", "First name");
        ElementInfo searchInfo = new ElementInfo("input");
        firstNameTextBox = driver.FindElementByAnchor(anchorInfo, searchInfo);
        firstNameTextBox.SendKeys("Tester");
            
## Versions
* Version **1.0.0.2** released on 03/14/2019
* Version **1.0.0.1** released on 03/11/2019

## NuGet
* https://www.nuget.org/packages/ExtSelenium/1.0.0.2
* Install-Package ExtSelenium -Version 1.0.0.2

## Dependencies
###.NETCoreApp 2.0
*dcsoup (>= 1.0.0)
*Selenium.Support (>= 3.141.0)
*Selenium.WebDriver (>= 3.141.0)
*System.Net.Http (>= 4.3.4)

###.NETCoreApp 2.1
*dcsoup (>= 1.0.0)
*Selenium.Support (>= 3.141.0)
*Selenium.WebDriver (>= 3.141.0)
*System.Net.Http (>= 4.3.4)

###.NETFramework 4.5
*dcsoup (>= 1.0.0)
*Selenium.Support (>= 3.141.0)
*Selenium.WebDriver (>= 3.141.0)
*System.Net.Http (>= 4.3.4)

###.NETFramework 4.6
*dcsoup (>= 1.0.0)
*Selenium.Support (>= 3.141.0)
*Selenium.WebDriver (>= 3.141.0)
*System.Net.Http (>= 4.3.4)

###.NETStandard 2.0
*dcsoup (>= 1.0.0)
*Selenium.Support (>= 3.141.0)
*Selenium.WebDriver (>= 3.141.0)
*System.Net.Http (>= 4.3.4)

## Author
###  **Tam Nguyen**
[![View My profile on LinkedIn](https://static.licdn.com/scds/common/u/img/webpromo/btn_viewmy_160x33.png)](https://www.linkedin.com/in/tam-nguyen-a0792930/)
			
