## Application State with Redux
What are the advantages of storing tokens in “Cookies” vs “Local Storage”
Local storage is vulnerable because it’s easily accessible using JavaScript and an attacker can retrieve your access token and use it later.
The cookie is not accessible via JavaScript; hence, it is not as vulnerable to XSS attacks as localStorage.
Explain 3rd party cookies.
Third-party cookies are cookies that are set by a website other than the one you are currently on.
For example, you can have a “Like” button on your website which will store a cookie on visitor’s computer
that cookie can later be accessed by Facebook to identify visitor and see which websites he visited. Such cookie is considered to be a third-party cookie.

## How do pixel tags work?
For marketing or media without a click event (such as navigating directly to a marketer’s website),
click redirects cannot be used. In those cases, pixel tags (also known as pixels, 1x1 pixels, image tags or web bugs) are used instead.
Pixel tags are typically single pixel, transparent GIF images that are added to a web page. Even though the pixel tag is virtually invisible,
it is still served just like any other image you may see online.
The trick is that the web page is served from the website’s domain while the image is served from the ad server’s domain.
This allows the ad server to read and record the cookie with the unique ID and the extended information it needs to record.

## Vocabulary Terms
cookies They are pieces of code that web servers use to put information on a user’s browser, and then retrieve that information at a later time for various uses.

authorization access rights/privileges to resources

access control selective restriction of access to a place or other resource while access management describes the process. The act of accessing may mean consuming, entering, or using. Permission to access a resource is called authorization.

conditional rendering Conditional rendering in React works the same way conditions work in JavaScript. Use JavaScript operators like if or the conditional operator to create elements representing the current state, and let React update the UI to match them

## Reading Materials
#### What is a redux
Redux provides a solid, stable, and mature solution to managing state in your React application. Through a handful of small, useful patterns, Redux can transform your application from a total mess of confusing and scattered state, into a delightfully organized, easy to understand modern JavaScript powerhouse. So it’s is a predictable state container for JavaScript apps.
#### Why use Redux?
A lot of developers love Redux is the developer experience that comes with it. A lot of other tools have begun to do similar things, but big credits to Redux.
Some of the nice things you get with using Redux include logging, hot reloading, time travel, universal apps, record and replay — all without doing so much on your end as the developer. These things will likely sound fancy until you use them and see for yourself.
The Redux Store can be likened to the Bank Vault. It holds the state of your application — and keeps it safe.
The Structure of the React Hello World Application
import React, { Component } from “react”; import HelloWorld from “./HelloWorld”
class App extends Component { state = { tech : “React” } render() { return }
export default App;`
Redux Toolkit
Redux Toolkit is our official recommended approach for writing Redux logic. It wraps around the Redux core, and contains packages and functions that we think are essential for building a Redux app. Redux Toolkit builds in our suggested best practices, simplifies most Redux tasks, prevents common mistakes, and makes it easier to write Redux applications.
