# Angular 4
Angular 4 is here for some time. It is a good time to enhance your skills on angular 4. I find myself more powerful while using angular 4. You should know that there are not many differences between angular 2 and angular 4. So anything I will discuss here would work with angular 2. You probably know the angular team is aiming to call angular 4 or angular 2 is as just Angular. Let’s get started by knowing what we are going to build now. I will try to be as detailed as possible.

## TYPESCRIPT
TypeScript starts from the same syntax and semantics that millions of JavaScript developers know today. Use existing JavaScript code, incorporate popular JavaScript libraries, and call TypeScript code from JavaScript.

TypeScript compiles to clean, simple JavaScript code which runs on any browser, in Node.js, or in any JavaScript engine that supports 

## let Start

Good tools make application development quicker and easier to maintain than if you did everything by hand.

The Angular CLI is a command line interface tool that can create a project, add files, and perform a variety of ongoing development tasks such as testing, bundling, and deployment.

The goal in this guide is to build and run a simple Angular application in TypeScript, using the Angular CLI while adhering to the Style Guide recommendations that benefit every Angular project.

By the end of the chapter, you'll have a basic understanding of development with the CLI and a foundation for both these documentation samples and for real world applications.

## Step 1. Set up the Development Environment
You need to set up your development environment before you can do anything.

Install Node.js® and npm if they are not already on your machine.

      Verify that you are running at least node 6.9.x and npm 3.x.x by running node -v and npm -v in a terminal/console window. Older versions produce errors, but newer versions are fine.
      
Then install the Angular CLI globally.
```cmd
npm install -g @angular/cli
```


Angular applications are made up of components. A component is the combination of an HTML template and a component class that controls a portion of the screen. Here is an example of a component that displays a simple string:
Step 1. Set up the Development Environment
**src/app/app.component.ts**
```TYPESCRIPT
import { Component } from '@angular/core';

@Component({
  selector: 'my-app',
  template: `<h1>Hello {{name}}</h1>`
})
export class AppComponent { name = 'Angular'; }
```
Every component begins with an @Component decorator function that takes a metadata object. The metadata object describes how the HTML template and component class work together.

The selector property tells Angular to display the component inside a custom <my-app> tag in the index.html.

**index.html (inside <body>)**
```html
<my-app>Loading AppComponent content here ...</my-app>
````
The template property defines a message inside an ```<h1>``` header. The message starts with "Hello" and ends with `{{name}}`, which is an Angular interpolation binding expression. At runtime, Angular replaces `{{name}}` with the value of the component's `name` property. Interpolation binding is one of many Angular features you'll discover in this documentation.

In the example, change the component class's `name` property from `'Angular'` to `'World'` and see what happens.

## A WORD ABOUT TYPESCRIPT
This example is written in TypeScript, a superset of JavaScript. Angular uses TypeScript because its types make it easy to support developer productivity with tooling. You can also write Angular code in JavaScript; this guide explains how.

Also Topics include:
*What is Angular?
*Setting up an Angular template
*Creating a component
*Binding events and properties
*Getting data to components
*Using directives and pipes
*Creating Angular forms
*Validating form data
*Understanding dependency injection
*Providing services
*Making HTTP calls
*Routing
