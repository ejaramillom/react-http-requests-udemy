# react-http-requests-udemy
How to handle http requests in react

# how not to connect to databases

Frontend should never directly talk to a database

- React app => Database (we will never see this because credentials will be exposed)
- React app <=> Backend app <=> Database (whatever language)

MUST READ:

In the next lecture, you will be introduced to our demo backend that will be used in this course section: The Star Wars API.

I will use this page: https://swapi.dev/

Loading this page (and hence accessing this backend) might fail - if that is the case for you, you can use this alternative: https://swapi.py4e.com/

https://academind.com/learn/web-dev/rest-vs-graphql/

https://academind.com/learn/javascript/hide-javascript-code/

# REST API VS graphQL API

- Rest uses URL driven technology, while graphQL is based on query language
- Rest has serveral endpoints, graph has only one post endpoint
- Both are stateless (they dont use token based authentication technologies)
- Both respond with JSON