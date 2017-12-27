# Puppeteer examples

Puppeteer Headless Chrome examples for real life use cases. Clone this repo and run them directy with a simple `node` command.

```bash
git clone https://github.com/checkly/puppeteer-examples
cd puppeteer-examples
npm i
node search/amazon.js
```
- [1. basics](#1-basics)
  * [alerts](#alerts)
  * [emulate devices](#emulate-devices)
  * [get list of links](#get-list-of-links)
  * [get title](#get-title)
  * [hover](#hover)
  * [keyboard](#keyboard)
  * [mouse](#mouse)
  * [pdf](#pdf)
  * [screenshots](#screenshots)
  * [screenshots clipped](#screenshots-clipped)
  * [set cookie](#set-cookie)
- [2. search](#2-search)
  * [Amazon search](#amazon-search)
  * [Booking.com search](#booking-com-search)
  * [Youtube search](#youtube-search)
- [3. login](#3-login)
  * [Github](#github)
- [4. shopping-carts](#4-shopping-carts)
  * [Walmart shopping cart](#walmart-shopping-cart)
- [5. mocha-tests](#5-mocha-tests)
  * [Alibaba product search](#alibaba-product-search)
  * [Alibaba product search](#alibaba-product-search)
  * [Google search](#google-search)
  * [Walmart shopping cart](#walmart-shopping-cart)
- [6. jest-tests](#6-jest-tests)
  * [Alibaba product search](#alibaba-product-search)
  * [Alibaba product search](#alibaba-product-search)
  * [Google search](#google-search)
  * [Walmart shopping cart](#walmart-shopping-cart)


## 1. basics
The very basic on getting useful info from web page. Highlights the basic Puppeteer functions.  
### alerts
Create an alert dialog and close it again.


[1. basics/alerts.js](https://github.com/checkly/puppeteer-examples/blob/master/1.%20basics/alerts.js)
### emulate devices
Use the built in devices descriptors to emulate an Iphone 6. These are actually shortcuts for calling page.setUserAgent() and page.setViewPort().


[1. basics/emulate_devices.js](https://github.com/checkly/puppeteer-examples/blob/master/1.%20basics/emulate_devices.js)
### get list of links
Scrapes Hacker News for links on the home page and returns the top 10


[1. basics/get_list_of_links.js](https://github.com/checkly/puppeteer-examples/blob/master/1.%20basics/get_list_of_links.js)
### get title
Get the title of a page and print it to the console.


[1. basics/get_title.js](https://github.com/checkly/puppeteer-examples/blob/master/1.%20basics/get_title.js)
### hover
The hover function is a combination of scrolling and putting the mouse into a hover state over the requested element. This example hovers the first track we find on the soundcloud.com homepage, which should trigger the play and like buttons to be visible


[1. basics/hover.js](https://github.com/checkly/puppeteer-examples/blob/master/1.%20basics/hover.js)
### keyboard
types into a text editor


[1. basics/keyboard.js](https://github.com/checkly/puppeteer-examples/blob/master/1.%20basics/keyboard.js)
### mouse
Most of the things you can click using straight .click() handlers, but for some situation directly instructing the mouse might be convenient. This example load a page that plays back what mouse actions are used on the page.


[1. basics/mouse.js](https://github.com/checkly/puppeteer-examples/blob/master/1.%20basics/mouse.js)
### pdf
Renders a PDF of the Puppeteer API spec. This is a pretty long page and will generate a nice, A4 size multi-page PDF.


[1. basics/pdf.js](https://github.com/checkly/puppeteer-examples/blob/master/1.%20basics/pdf.js)
### screenshots
Snaps a basic screenshot of the full New York Time homepage and saves it a .png file.


[1. basics/screenshots.js](https://github.com/checkly/puppeteer-examples/blob/master/1.%20basics/screenshots.js)
### screenshots clipped
Grabs and clips out just the stock tickers on the Yahoo finance page


[1. basics/screenshots_clipped.js](https://github.com/checkly/puppeteer-examples/blob/master/1.%20basics/screenshots_clipped.js)
### set cookie
Sets the "login_email" property in a Paypal cookie so the login screen is pre-filled with an email address.


[1. basics/set_cookie.js](https://github.com/checkly/puppeteer-examples/blob/master/1.%20basics/set_cookie.js)
## 2. search
Common search input and select methods on search results.  
### Amazon search
Looks for a "nyan cat pullover" on amazon.com, goes two page two clicks the third one.


[2. search/amazon.js](https://github.com/checkly/puppeteer-examples/blob/master/2.%20search/amazon.js)
### Booking.com search
Finds accommodations in Berlin on Booking.com, takes a screenshot and logs the top 10.


[2. search/booking.js](https://github.com/checkly/puppeteer-examples/blob/master/2.%20search/booking.js)
### Youtube search
Looks for Fleetwood Mac's "Dreams" video on youtube.com and clicks on the third video. Waits for 5 seconds for the video to load.


[2. search/youtube.js](https://github.com/checkly/puppeteer-examples/blob/master/2.%20search/youtube.js)
## 3. login
Common login scenarios on popular website. Credentials mostly supplied with setting `ENV` variables.  
### Github
Logs into Github. Provide your username and password as environment variables when running the script, i.e: `GITHUB_USER=myuser GITHUB_PWD=mypassword node github.js`


[3. login/github.js](https://github.com/checkly/puppeteer-examples/blob/master/3.%20login/github.js)
## 4. shopping-carts
How to handle shopping cart functions like adding and removing items.  
### Walmart shopping cart
Looks for a Nintendo's Mario Odyssey and adds it to the shopping cart.


[4. shopping-carts/walmart.js](https://github.com/checkly/puppeteer-examples/blob/master/4.%20shopping-carts/walmart.js)
## 5. mocha-tests
Mocha test runner scripts that use Puppeteer and the standard `assert` library to check specific properties and actions on a page. Install Mocha as a global dependency and run them as any other script

```bash
npm i -g mocha
mocha mocha-tests/alibaba.js
```  
### Alibaba product search
Searches Alibaba.com for a product and checks if the results show up


[5. mocha-tests/alibaba.js](https://github.com/checkly/puppeteer-examples/blob/master/5.%20mocha-tests/alibaba.js)
### Alibaba product search
Searches Alibaba.com for a product and checks if the results show up


[5. mocha-tests/amazon.js](https://github.com/checkly/puppeteer-examples/blob/master/5.%20mocha-tests/amazon.js)
### Google search
Searches Google.com for a term and checks if the first link matches. This check should fail.


[5. mocha-tests/google.js](https://github.com/checkly/puppeteer-examples/blob/master/5.%20mocha-tests/google.js)
### Walmart shopping cart
Goes to walmart.com and adds a Nintendo game to an empty shopping cart. Validates the correct amount.


[5. mocha-tests/walmart.js](https://github.com/checkly/puppeteer-examples/blob/master/5.%20mocha-tests/walmart.js)
## 6. jest-tests
Jest test runner scripts that use Puppeteer to check specific properties and actions on a page. Very similar to the Mocha tests, but using the Jest `expect` assertions. Install Jest as a global dependency and run them as any other script

```bash
npm i -g jest
jest jest-tests/alibaba.js
```  
### Alibaba product search
Searches Alibaba.com for a product and checks if the results show up


[6. jest-tests/alibaba.spec.js](https://github.com/checkly/puppeteer-examples/blob/master/6.%20jest-tests/alibaba.spec.js)
### Alibaba product search
Searches Alibaba.com for a product and checks if the results show up


[6. jest-tests/amazon.spec.js](https://github.com/checkly/puppeteer-examples/blob/master/6.%20jest-tests/amazon.spec.js)
### Google search
Searches Google.com for a term and checks if the first link matches. This check should fail.


[6. jest-tests/google.spec.js](https://github.com/checkly/puppeteer-examples/blob/master/6.%20jest-tests/google.spec.js)
### Walmart shopping cart
Goes to walmart.com and adds a Nintendo game to an empty shopping cart. Validates the correct amount.


[6. jest-tests/walmart.spec.js](https://github.com/checkly/puppeteer-examples/blob/master/6.%20jest-tests/walmart.spec.js)