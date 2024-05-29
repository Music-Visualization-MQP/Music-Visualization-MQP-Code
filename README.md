# Music-Visualization-MQP-Code

Again... I am not sure if this is the right way to do this....

the way i thought through this though was to have a git repository for the main docker containers where they could all be built and deployed from the same convinent repo with submodules for the other repos

this, like everything is subject to change

so many security vulnerabilities,

so many reasons for the apps to fail to communicate

## Wed 29 May 2024

### the problem

* I think java is the wrong way to go for this project its so clunky and frustrating to look back on

* I feel that the main 2 contenders for a backend is something nodejs based or go based
* from the little research I have done go is trickier to work with but is faster
  * I dont really care about speed so much, I'd like a nice dev experience.
  * id like the environment to get in the way as little as possible

### The path forward

* **affirmations**
  * the system must have a simple dev experience
    * portability and ease of deployment
  * the system should be designed in such a way that each contributer has a defined task which interferes with other's work as little as possible
  * the system must implement typing in some way
  * the system might benefit from minimal boilerplate
  * the system must use abstraction sparingly and only where nescicary
  * the system should be performant for 100 + users
  * the system should have tests which are easy to implement
  * the system should outsource authentication

* **GO**
  * the more I read the less I want to deal with it
  * the idea of moving away from java is to improve the dev experience

* **NodeJS**
  * **Frameworks**
    * **NestJS**
      * seems pretty similar to spring which is both good and bad
        * boilerplate
        * schema? of controllers, providers, middleware, etc.
        * people say its like writing java (mmmmmmmm, no thanks)
    * **TypeORM**
      *
    * **FoalTS**
      * Less boilerplate, documentation is a bit more confusing but the code is easier to read, imo
      * "Controllers are the front door of your application. They intercept all incoming requests and return the responses to the client."
      * Not exactly what I think im looking for
    * **Adonis**
      * javascript first framework, i don't really feel like figuring out how to cram ts down its throat
      * looks really similar to nest js, too much boilerplate for me
    * **Prisma**
      * simple and no nonsense, seeming
      * easy to create custom db objects, might be ideal for dealing with our db and then the musicbrainz db
      *
    * **Compiling ts to js**
      * just writing vanilla typescript and running it under node
        * no boilerplate or frameworks to become familiar with
        * some framework like express
      * not as easy to scale, though
  * **Load balancing**
    * if we really want to support many users a load balancer would be needed
      * nest has support for it, i don't care
      * node actually has support for it
    * load balancing with mongodb seems easier than with mysql
      * after webware, i have really fallen for mongo, it's so easy to work with
  
* **architecture**
  * ci/cd
    * would be great for getting software in testers hands
  * microservice philosiphy might apply well here
    * web api
    * musicbrainz
    * data aquisition

* **the front runners**
  * Prisma
  * minimal framework, like express

## Sources

Auth0. n.d. “Introduction to Identity and Access Management (IAM).” Auth0 Docs. Accessed May 29, 2024. <https://auth0.com/docs/>.
“Documentation | NestJS - A Progressive Node.Js Framework.” n.d. Documentation | NestJS - A Progressive Node.Js Framework. Accessed May 29, 2024. <https://docs.nestjs.com>.

hyderox. 2023. “What NodeJS Framework Do You Use in Production?” Reddit Post. R/Node. <www.reddit.com/r/node/comments/13hf4om/what_nodejs_framework_do_you_use_in_production/>.

“Introduction | FoalTS.” n.d. Accessed May 29, 2024. <https://foalts.org/docs/>.

Kathiriya, Akash. 2019. “An Overview of MongoDB and Load Balancing.” Severalnines (blog). October 22, 2019. <https://severalnines.com/blog/overview-mongodb-and-load-balancing/>.

“Koa - next Generation Web Framework for Node.Js.” n.d. Accessed May 29, 2024. <https://koajs.com/>.

“Node.Js — Node.Js with TypeScript.” n.d. Accessed May 29, 2024. <https://nodejs.org/en/learn/getting-started/nodejs-with-typescript>.

“Scaling Node.Js Applications.” 2017. freeCodeCamp.Org. July 14, 2017. <https://www.freecodecamp.org/news/scaling-node-js-applications-8492bd8afadc/>.

“Tutorial: Developing a RESTful API with Go and Gin - The Go Programming Language.” n.d. Accessed May 29, 2024. <https://go.dev/doc/tutorial/web-service-gin>.

“What Are Microservices? | AWS.” n.d. Amazon Web Services, Inc. Accessed May 29, 2024. <https://aws.amazon.com/microservices/>.
