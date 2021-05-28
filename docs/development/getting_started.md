# Getting Started

This onboarding tutorial is meant to supplement and guide you so that you can dive into working with us on our VCL web framework

You should take the time to go over the [Architecture](../architecture) section in addition to the role that you are onboarding for (either ‘Software Developer’ or ‘Technical Researcher’, you **don’t have to read both**). 

Please keep in mind that roles in our team are not rigid, and you will not be pigeonholed into a single role. The idea of splitting up roles into ‘Software Developer’ and ‘Technical Researcher’ stemmed from the necessity of simplifying the onboarding process, as the codebase is quite daunting for new members initially. You will likely onboard with the role that you are interested in, but after onboarding, the role that you have within our team will likely be quite fluid depending on the needs of the lab and your personal goals and interests.

Lastly, as you probably know, Google and StackOverflow will be your best friend when working with a new codebase, and if you have any questions, feel free to message our senior members on Slack. The tutorial will assume that you have little baseline knowledge of our tech stack, but feel free to skip over parts that you are already familiar with.

## Technical Researcher Onboarding

If you’ve chosen this route, you will likely work with developing experiments/conditions for research purposes. You might even be a COGS 402 student, as we’ve noticed many past members go with this path as a student in that course. This section will provide some background on what we feel are the necessary skills to succeed in this role.

## Prerequisite Knowledge - Technical Researcher

!!! Note
    Please feel free to skip over the skills you are already experienced with.

### Github

Github is a hosting platform for Git version control, and it allows different users to remotely collaborate on the same project. We use Github to host our VCL web framework repository. The main skills you will need with regards to git are understanding branches, commits, and pull requests. Please refer to this [beginner guide](https://guides.github.com/activities/hello-world/) to learn more.

The code review process for our team ensures that the code written fits the lab’s coding standards and does not introduce unwanted bugs. We don’t necessarily have formal code reviewers assigned as of right now, but generally speaking, you can assign any senior coding team member to review a branch pull request.

Popular Git GUIs: (You can use a GUI or just Git Bash whichever is most comfortable for you)

- [SourceTree](https://www.sourcetreeapp.com/)
- [GitKraken](https://www.gitkraken.com/)
- [GitHub Desktop](https://desktop.github.com/)

[Download Git](https://git-scm.com/downloads)

### JavaScript

We recommend understanding the basics of Javascript and HTML before attempting to understand the framework. Here are a few resources:

- [JavaScript](https://javascript.info/)
- [JavaScript Mozilla documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [HTML](https://www.w3schools.com/html/)

The comprehensive references are mainly useful when writing code and you might forget the language syntax.

### JsPsych

jsPsych is the backbone of our application and is the main reason why we transitioned from a Java framework to a JavaScript framework back in 2018.

JsPsych is the go-to JavaScript library for running psych experiments in a browser. The timeline array provides an intuitive way to design and structure experiments for both developers and researchers.

The jsPsych documentation provides a comprehensive guide for how to use the library. We recommend checking out their “Hello World” and “Simple Reaction Time Task” Tutorials:

- [Hello World Tutorial](https://www.jspsych.org/tutorials/hello-world/)
- [rt-task Tutorial](https://www.jspsych.org/tutorials/rt-task/)

### D3
D3 is a data visualization library for JavaScript. We use D3 to generate the plots for all of the experiments that we run. We recommend becoming familiar with [D3](https://github.com/d3/d3/wiki) if you are creating a new condition.

!!! Success
    Congrats on finishing the Technical Researcher section! You can continue to the concluding section now.

## Software Developer Onboarding

If you’ve chosen this route, you will be working with the framework as a whole to develop new features, fix bugs, and support researchers in developing new conditions and experiments. This section will provide some background on what we feel are the necessary skills to succeed in this role.

!!! Note "Prerequisite Knowledge"
    Please feel free to skip over the skills you are already experienced with.

### Github

Github is a hosting platform for Git version control, and it allows different users to remotely collaborate on the same project. We use Github to host our VCL web framework repository. The main skills you will need with regards to git are understanding branches, commits, and pull requests. Please refer to this [beginner guide](https://guides.github.com/activities/hello-world/) to learn more.

The code review process for our team ensures that the code written fits the lab’s coding standards and does not introduce unwanted bugs. We don’t necessarily have formal code reviewers assigned as of right now, but generally speaking, you can assign any senior coding team member to review a branch pull request.

Popular Git GUIs: (You can use a GUI or just Git Bash whichever is most comfortable for you)

- [SourceTree](https://www.sourcetreeapp.com/)
- [GitKraken](https://www.gitkraken.com/)
- [GitHub Desktop](https://desktop.github.com/)

[Download Git](https://git-scm.com/downloads)

### JavaScript

We recommend understanding the basics of Javascript and HTML before attempting to understand the framework. Here are a few resources:

- [JavaScript](https://javascript.info/)
- [JavaScript Mozilla documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [HTML](https://www.w3schools.com/html/)
- [CSS](https://www.w3schools.com/css/)
- [jQuery](https://api.jquery.com/)

The comprehensive references are mainly useful when writing code and you might forget the language syntax.

### Express.js + Node.js + NPM

Node.js is a JavaScript runtime built on the Chrome V8 engine. One of the primary ways it is used is to allow Javascript code to be run server-side. Think of Node.js as a way to run Javascript code similarly to how Java or Python code are run using their respective runtime environments. Node.js is just a way for us to run Javascript code outside of a browser environment.

Along with Node.js we use a tool called Node Package Manager (npm). npm is a package registry that contains Node.js code libraries which are useful for development. It is used to handle dependency management, version management, and package installation primarily through the CLI.

Express is a web application framework and standard server framework for Node.js, and it provides a bunch of features for building web-apps and APIs. We use express to handle routing (GET and POSTrequests), middleware functions (functions called when a request is received on the specified URL), and also start the localhost server for development testing.

- [Express Routing](https://expressjs.com/en/guide/routing.html )
- [Express Middleware](https://expressjs.com/en/guide/writing-middleware.html)
- [body-parser](https://stackoverflow.com/questions/38306569/what-does-body-parser-do-with-express) 

### Web APIs and HTTP

Application Programming Interfaces (APIs) are a way for a web client to interact with a web service and utilizes the Hypertext Transfer Protocol (HTTP) to perform queries. APIs written with ExpressJS are composed of many routes and middleware functions, and each route has one middleware function associated with it.

Routes are used to define the “endpoint” or specific URL in which the request is expected to occur. Middleware functions define the behaviour of the API when a certain request is made on a specified URL from the routing. Middleware functions also define expected information in a request, and it also specifies how the API responds to the request (either with information or error messages).

We primarily use our API written in app.js as a means to serve web pages.

In general, web APIs use four main HTTP methods to achieve a robust interface: GET, POST, PUT, and DELETE. For the purpose of our framework, you mainly need to understand GET and POST requests.

**GET**

When you perform a GET request on a specific URL, you retrieve information without modifying it in any way. The data that you receive in a GET request is specified by the response of the server. Think of it as getting information from a collection.

If for example, I want to get all users from an arbitrary API, I could make a GET request to “https://{example_API_root}.com/users/”. Where “{example_API_root}” is the root URL of the host server, and “/users/” is specified by the routing.

**POST**

A POST request is primarily used to create a new resource. Think of it as adding new information to a collection.

Note that this is an oversimplification of APIs and HTTP, and if you want to gain a better understanding of building APIs (such as with RESTful concepts), we recommend these links:

- [ELI5 for APIs](https://www.reddit.com/r/explainlikeimfive/comments/628y0c/eli5_what_is_an_api/)
- [HTTP Requests](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)
- [RESTful APIs](https://restfulapi.net/)

### JsPsych

jsPsych is the backbone of our application and is the main reason why we transitioned from a Java framework to a JavaScript framework back in 2018.

JsPsych is the go-to JavaScript library for running psych experiments in a browser. The timeline array provides an intuitive way to design and structure experiments for both developers and researchers.

The jsPsych documentation provides a comprehensive guide for how to use the library. We recommend checking out their “Hello World” and “Simple Reaction Time Task” Tutorials:

- [Hello World Tutorial](https://www.jspsych.org/tutorials/hello-world/)
- [rt-task Tutorial](https://www.jspsych.org/tutorials/rt-task/)

!!! Success
    Congrats on finishing the Software Developer section!

## Technical Debt and Writing “Good” Code

Writing good code is hard. It takes years of experience to learn best practices well, and even the most experienced programmers will write shitty code from time to time. Nonetheless, in a project with as many moving pieces as our codebase, it is important to try our best to write “good” code and minimize technical debt.

Technical debt is a concept in software development that reflects the implied cost of additional work caused by choosing an easy solution now instead of using a better approach that would take longer. Some examples are messy code formatting , duplications, unnecessarily large time complexity, architectural flaws, lacking documentation and other bad coding practices.

Note that our team isn’t large, and as a result, relatively significant amounts of technical debt will naturally accumulate over time. It’s important to assess the choices we make to minimize technical debt build-up while also balancing the time it takes to implement the ‘optimal solution’.

Some examples of technical debt present in our codebase right now (2021/02/07):

- Using jQuery over a more modern front-end library (such as React or Vue)
- Server-side architecture is nonoptimal, and basically, the only purpose of the express server is to serve static (mostly HTML) files to the client
- Not using best practices in coding. Ex.
    - Using `var` to instantiate variables where `let` or `const` would be better
    - Repetitive code in places such as experiment and trial display HTML files

It is important to note that these fundamental design choices were likely made very early on in the design process of our framework, but as a result, developers in the present and future will need to work around these decisions long after they were made.

This is not to say that those decisions were necessarily ‘wrong’ at the time. It is likely that they were developed with scope and stakeholders entirely considered, but as time went on, the stakeholder needs changed. But now, the design choices made early in development would require a massive refactor to change.

In essence, think about minimizing technical debt as you are implementing new features, but not at the expense of sanity. Abstract for when you think there will be a use case for in the future, but not just for the sake of doing it.

## Next Steps

Congrats on getting through our onboarding documentation! For your next steps please try to complete the following tasks:

1. Implement your own Express.js server in Node.js to display “hello world”. (Software Developer only)
2. Complete the jsPsych [Hello World Tutorial](https://www.jspsych.org/tutorials/hello-world/) and [rt-task Tutorial](https://www.jspsych.org/tutorials/rt-task/)
3. Make a new branch off of “master” and modify the codebase so that it can display large bullseyes instead of dots for JND foundational scatterplots.
    - Most of the coding that you will need to do can be found in the codebase already, and you will just need to modify some config files, the jnd data file, and the scatter plot file to produce those bullseye dots.
    - You may find that there is already a bullseye case for the point shape, you can base the new bullseye off of this previous case.
    - You can get creative with the actual bullseye dimensions and colours.
    - When you are done, make a merge pull request to “master” and senior members on the team can review your code.
