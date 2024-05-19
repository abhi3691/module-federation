# Module Federation Example

This example shows you how to setup Re.Pack with its `ModuleFederationPlugin`.

For a more comprehensive example of a Super App setup with Module Federation please visit our [Super App Showcase repository](https://github.com/abhi3691/module-federation).




Module Federation#

Before diving deep into Module Federation, it's important to understand how Code Splitting works in React Native with Re.Pack and what are the challenges.

Module Federation is similar to Code Splitting, but offers more control, flexibility and scalability.



What is Module Federation?#

Module Federation is an architecture, which splits the application into multiple pieces. These pieces are called containers. Similarly to micro-services, Module Federation splits application into a distributed frontends, sometimes referred to as micro-frontends.


<img width="1469" alt="Screenshot 2024-05-18 at 11 17 19 PM" src="https://github.com/abhi3691/module-federation/assets/54738565/5eb89bc9-e6ef-44a2-8335-4b5a415d884f">

Benefits#
The main benefits or Module Federation are:

Ability to split application into multiple isolated micro-frontends.
Ability to customize build configuration and process for each micro-frontend.
Ability to dynamically load micro-frontends on demand.
Ability to load different versions of the micro-fontends.
Ability to use external micro-frontends.
Keep in mind that this list is not exhaustive. It's possible you could benefit from Module Federation in another way as well.

Challenges#
Not every project or application is a good fit for Module Federation. Due to nature of Module Federation there's are few challenges and overheads you need to consider:

It's easy to cause dependency duplication, e.g. if you're using incompatible versions in micro-frontends/container.
It requires coordination when configuring Webpack for each micro-frontend/container - otherwise, your micro-frontend/container might not be compatible.
It complicates deployment - each micro-frontend/container has to be deployed and available to the clients (usually via Internet).
It complicates release management - you need to make sure micro-frontend/container are as much isolated as possible and not co-dependent on each other, otherwise you need to make sure that dependent micro-frontend/container are released altogether.
... - there might be more challenges, depending on your use-case, internal processes, policies and specifics of your project.

https://re-pack.dev/docs/module-federation


