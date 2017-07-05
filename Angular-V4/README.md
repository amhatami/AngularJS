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

      Verify that you are running at least node 6.9.x and npm 3.x.x by running 
      node -v and npm -v in a terminal/console window. Older versions produce 
      errors, but newer versions are fine.
      
Then install the Angular CLI globally.
```cmd
npm install -g @angular/cli
```

## Step 2. Create a new project

Open a terminal window.

Generate a new project and skeleton application by running the following commands:
```
ng new my-app
```
      Patience please. It takes time to set up a new project, most of it spent installing npm packages.

## Step 3: Serve the application

Go to the project directory and launch the server.
```
cd my-app
ng serve --open
```

The `ng serve` command launches the server, watches your files, and rebuilds the app as you make changes to those files.

Using the `--open` (or just `-o`) option will automatically open your browser on `http://localhost:4200/`.

Your app greets you with a message:
![angular logo](https://angular.io/generated/images/guide/cli-quickstart/app-works.png)

## Step 4: Edit your first Angular component
The CLI created the first Angular component for you. This is the root component and it is named `app-root`. You can find it in `./src/app/app.component.ts`.

Open the component file and change the `title` property from Welcome to app!! to Welcome to My First Angular App!!:

**src/app/app.component.ts**
```ts
export class AppComponent {
  title = 'My First Angular App';
}
```
The browser reloads automatically with the revised title. That's nice, but it could look better.

Open `src/app/app.component.css` and give the component some style.

**src/app/app.component.css**
```css
h1 {
  color: #369;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 250%;
}
```
![app output](https://angular.io/generated/images/guide/cli-quickstart/my-first-app.png)
Looking good!
