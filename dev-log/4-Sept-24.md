# Dev Log 2

## 4 Sept 2024

### Setup

Setup is more of a nontrivial process than I had initially expected. The project requires the use of 3 discrete software projects. One of them is supabase, which is an alternative to Google's Firebase. Supabase can be used through a simple typescript based cli, which drives many docker containers. The docker containers handle user storage, a backend api, authentication, etc. This means each team member needed to have node.js, npm, typescript all up to date and installed correctly. This proved frustrating and time consuming. 

### Interfaces in Typescript

It is hard to tell whether or not interfaces are practically deprecated in Typescript. They throw an error if fields are not re-declared in the implemented classes. Which kind of defeats the point of having interfaces. However there are robust seeming mechanisms for utilizing polymorphism.

### Plans for Data Acquisition

Data acquisition is a simple seeming problem. Just get the users, authorize the various services and maybe check for new users.

The original plan for this part of the application was to have no endpoints. However the mechanism for checking for new users, taking the current map of users and removing the existing ones will not scale well. It is now apparent that another method is required.

The need for a scheduler has become apparent