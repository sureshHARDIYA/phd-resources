# Introduction

The aim of this technical documentation is to provide sufficient insights for interested parties to validate prototypes developed during my Ph.D. My research falls under `software engineering` in general, however my study tries to include other fields including `health informatics`, `IoT`, and `data science`. To backup my proposed solutions for solving problem associated with my study, we have developed several web and mobile based application as prototypes. However, we must emphasis that the prototypes developed must be used as a source of inspiration or general ideas rather than complete commercial solutions.

# Architecture

The prototype contains following major components:

- `Resource Server`:This is a FHIR compliant web server that is able to respond to HTTP requests using Access Tokens issued by the Authorization Server.
- `The User:` This is the person who is actually logging into the application to perform some function. Not all SMART on FHIR flows actually require a user to be present but most do.

- `The SMART on FHIR Application` (referred to as the “SMART App” or “Client” below): This is an application that the user wishes to access to perform some function.

- `Authorization Server:` This is an OpenID Connect compliant web server that is able to authenticate users and issue Access Tokens. Smile CDR is able to perform this role but other Authorization Servers may also be used.

## Resource Server

## Mobile Client

## Web Client

### FAQ

- <details><summary>Can I get source code for it?</summary>
  <p>

#### yes, even hidden code blocks!

```python
print("hello world!")
```

</p>
</details>

## Authorization Server

# Technologies

## [`ReactJS`](https://reactjs.org/)

ReactJS is a component-based JavaScript library that follows the declarative programming paradigm. The declarative views can be utilized to create complex interactive UI which serves as the presentational component of the web[[1]](#1). The library is easy to learn, promotes code reusability, offers lightweight DOM for better performance, enforces unidirectional data flow, ensures Search Engine Optimizations (SEO), forms the views of Model View Controller(MVC) architecture and supports virtual DOM.

## `Redux`

With the great prevalence of web applications and companies transforming from traditional desktop-based systems to web-based systems, there are now a multitude of opportunities on the World Wide Web. There are various programming languages for server-side scripting (SSR), client-side scripting, presentation logic (HTML and CSS), and query languages. JavaScript is one of the most popular languages on the web, and it encompasses several frameworks that assist in its development, compilation, and production. React is one of the most popular JavaScript frameworks, and it is developed and distributed by Facebook. While React helps in building highly sophisticated, interactive user interfaces, Redux, on the other hand, is getting very popular in the frontend community for state management [[2]](#2).

## `Redux Saga`

`Redux-saga` is a third-party JavaScript library that helps to easily and efficiently manage an application's side effects, including asynchronous activities such as fetching data and accessing browser cache. Mukhiya and Hung outline the essential importance of using redux-saga in a web application [[3]](#3). We can use the image used in this paper as a reference to better understand the need for redux-saga. To explain it in one sentence, we can say that redux-saga is responsible for handling side effects. Saga uses [ES6 Generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*) to make asynchronous flows easy to read, write, and test. If you are not familiar with generators, it would be best to pause before the next section and read up on them. Here is a couple of [suggested articles:](https://redux-saga.js.org/docs/ExternalResources.html).

## `Immutable JS`

The home page for immutable JS briefs the merits of using the library. However, it is a bit difficult to understand. In this section, we will explain the importance of immutable JS in simple terms. The use of Immutable JS is a hot topic of discussion in the frontend community. A couple of important aspects of immutability are that it increases predictability and performance and allows for mutation tracking. In addition to that, immutable JS provides a convenient way to modify deeply nested properties. Let us explore two problems it solves. The examples is taken from [[2]](#2).

### The data reference problem

A lot of bloggers and developers seem to accuse Immutable JS of certain things, without understanding its core concepts. React is not just about building interactive UI/UX interfaces; it is about performance. The purpose of its development was to be performant and to only update the DOM when required, and also, to only update the portion that was required to be updated. An optimized React app should contain simple, stateless functional components, and can have a `shouldComponentUpdate` that returns `false`:

```
shouldComponentUpdate(nextProps, nextState) {
   return false;
}
```

You should be familiar with React life cycle functions. The most notable function in the React component life cycle is shouldComponentUpdate, and it is expected to return false whenever possible. Why? Well, as the name suggests, this ensures that the component, with `shouldComponentUpdate` returning `false`, will never re-render, making the `React` app extremely performant.

Our primary goal should be to compare old props and states with new props and states; if they are not changed, the component should never re-render. However, remember that in `JavaScript`, equality checks can be sophisticated. Consider the equality in primary data types:

```
33 === 33
'yoshimi' === 'yoshmi'
false === false
```

Let's look at the equality in complex objects and arrays, as follows:

```
const object1 = { prop: ‘simpleValue’ };
const object2 = { prop: ‘simpleValue’ };
console.log(object1 === object2);   // false
```

The `object1` and `object2` appear to be the same, but their references are different. As these two objects are judged to be different, equaling them within the `shouldComponentUpdate` function naively will make our component needlessly re-render. Data comes from Redux reducers. If these reducers are not set correctly, they will be presented with different references, which will cause the component to re-render every time. This is one of the major problems with respect to performance.

### Reference handling

When we start to work on a real application, sooner or later, we come across deeply nested objects. We assume that there is a need to compare the objects with the previous values. One way to achieve this is to loop through each object recursively. We can imagine that this computation will be expensive and will require another solution.

Another way to solve this is by inspecting the reference. However, this requires us to preserve the reference if nothing has changed, and to also change the reference if any of the nested object/array prop values have changed. This task is very complicated. Although there are some libraries that help in deep comparing the objects, if we want to do it in a clean, optimized way, immutable JS is our solution. Facebook developers faced these obstacles in the very early stages of development, and hence, they developed immutable JS to overcome the issues.

## `mongoDB`

## `Ant Design Pro`

## `GraphQL`

- How does `GraphQL` work?
- How is `GraphQL` queries validated and executed?

## `Apollo-tags`

## `Redux-Form`

# Getting Started

# Discussion

# Conclusion

# FAQs

1. Why did we build our application using `ReactJS`?
2. What is `Redux`? Why do we need it?
3. What is `Redux-Saga`? Why do we need it?
4. Why is our prototype using `mongoDB`? Why not others?
5. What is `HL7 FHIR`? And why should we use it?
6. What is `INTROMAT`?

# References

1. <a name="1"></a>Suresh Kumar Mukhiya, Fazle Rabbi, Violet Ka I Pun, Yngve Lamo, An architectural design for creating self-reporting e-health systems. InICSE 2019Proceedings in the IEEE Digital Library(2018).
2. <a name="2"></a> Redux Quick Start Guide: A Beginner's Guide to Managing App State with Redux, James Lee, Tao Wei, Suresh Kumar Mukhiya, Packt Publishing, Feb 28, 2019
3. <a name="3"></a> Mukhiya, S. K., & Hoang Hung, K. (2018). An Architectural Style for Single Page Scalable Modern Web Application, 5(4), 6–13. Retrieved from https://www.ijrra.net/Vol5issue4/IJRRA-05-04-02.pdf
