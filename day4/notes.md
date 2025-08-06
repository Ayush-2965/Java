# Session Management

## What is session management

A network protocol can be classified into mainly two types:-
stateless statefull

- statefull protocol server always remember its client even after sending the response 
FTP 
- stateless protocol server does not remembers its client after sending the response.
ex- Http 
---- in order to make a server remember its client in a stateless protocol we have to perform certain mechanism
and this is termed as session management

- ## Session management can be achieved in 4 words-
1. Cookies
2. Http session
3. Url rewriting
4. Hidden Field Format

## Cookies

Cookie is a small file which is created by the server.Every Cookie contains a name and value as a pair.This name value pair is unique for each cookie.

Cookie is stored in the client side
In java there is class called **Cookie** using which we can create a particular cookie.

HTTP Session
in case of HTTP SEssion a file is created by the server amd that file is stored in server side.

### Get Request
Get will show everything(all contents) in th url with params because data and req go side by side so only use get to fetch or never send any sensitive data.Get is faster to interact with server.

### Post Request
Post request are sent after req with encrypted form so data is not shown in the url.Hence, Post method is safer than get.

## URL Rewriting
Url rewriting is the mechanism by which session is managed through hyperlinking

## Hidden Field Format

Here the Values are transfered from source page to the destination page through hiding the data.

***Among this four ways of session management which one is the best and why?***

> If we perform session management using url rewriting and hidden field format then in order to tranfer the values from source to destination,We have to pass the values through all the in between pages and that is a hectic task. In this case session management using cookie or http session is betteras compared to url rewriting or hidden field format.In case of cookies and httpsession httpsession is best because the data is stored in the serverd side.