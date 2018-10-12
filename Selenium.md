# Installing selenium


Install selenium using the following command:

  ```sh
$ pip install -U selenium
```

# Chrome Driver Setup
Chrome Driver enable Selenium to run all the test cases with chrome browser.
  - Download **chrome driver** from the below link and install it. https://sites.google.com/a/chromium.org/chromedriver/downloads. 
  - Make sure the driver is in the executable path.
  - start the driver and run the tests.
```sh
from selenium import webdriver
from selenium.webdriver.common.keys import Keys

browser = webdriver.Chrome()

browser.get('http://www.google.com')
print(browser.title)

browser.quit()
```
# Adding a Headless argument
  - For the tests to occur in the background, we should make the following changes.
  - Add a "headless" argument to ChromeOptions() instead of just using Chrome().
  ```sh
  options = webdriver.ChromeOptions()
  options.add_argument('headless')
  ```
  - Now, start the driver and run the tests as we did earlier
  ```sh
  browser = webdriver.Chrome(options = options)

browser.get("http://www.google.com")
print(browser.title)

browser.close()
  ```
