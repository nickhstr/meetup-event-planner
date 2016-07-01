# Let's Meetup

A meetup event planner web app.

[The app is live](https://meetup-event-planner-4d9bb.firebaseapp.com), for all of your meet-up
event management pleasure, and please do yourself the favor of using Chrome.

## First Project of the Senior Web Developer Nanodegree

Forms are often not fun to fill out or navigate. This app serves to demonstrate how forms
can be used as a force for good. The amount of inputs have been kept to a minimum, and validation
occurs immediately, all in an effort to preserve the user's sanity.

## Using the App

To view, edit, or create events, the user must be signed in. Luckily, signing up is simple, only requiring the user's name, email, and password, with the other fields being optional.

Immediately after the user has signed up or signed in, the app navigates to the events view. Now the fun begins - that is, as much fun as event creation can be.

Each event includes the usual suspects: a title, type, location, dates and times, host, guests. Optionally, events also offer room to leave some extra info as well as an image for the event.

And of course, there is a view for the user's account information; you know, in case the user forgets who they are.

For those who cannot or will not create an account, there is a test account available; its email is "bob@mail.com", and its password is the oh-so-creative "password1".

## Tools and Technologies

Out of all the wonderful libraries and frameworks for web development, I chose Polymer and its companion
Polymer CLI. Concerning the former, there's no better time to adopt component-driven development as it is undoubtedly the future, and Polymer with it's standards-based approach, largely accessibility-minded components, and simplicity puts the focus of development where it belongs, on delivering a great app.

Normally, my build process would be Gulp-driven, however with Polymer's own Polymer CLI and its build process, I decided to give the unfamiliar a go. Configuration is simple, done either inline on the command line, or done with a JSON file. The build process creates two builds, "bundled" and "unbundled"; the first is best for bundling all components into one file, limiting the number of requests to the server, and the second is best paired with HTTP2. For this app, despite not utilizing HTTP2, I opted for unbundled to practice lazy-loading components.

In any case, the build process also creates a service worker, which this app utilizes to cache the app's shell and its fragments - or in other words, the foundation of the app and its main views.

For the back end, in lieu of slapping together my own sad excuse for a back end with Node.js - and going even further out of scope of the project - I've employed Firebase. Firebase made authentication and database management simple, has an easy to use CLI tool for deploying, and it doesn't hurt that they have their very own Polymer components.

### Finally...

Thanks for using the app, and stayed tuned for the next project in my adventures of the Senior Web Developer Nanodegree!