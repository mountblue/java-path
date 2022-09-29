# Spring

## Resources

1. Udemy: Spring & Hibernate for Beginners (includes Spring Boot)
[https://www.udemy.com/course/spring-hibernate-tutorial](https://www.udemy.com/course/spring-hibernate-tutorial)
2. [https://hackr.io/tutorials/learn-java-spring-framework](https://hackr.io/tutorials/learn-java-spring-framework)

## SpringBoot basics

1. Library vs Framework
2. J2EE vs Spring vs Spring Boot
3. Spring Initializr - http://start.spring.io
4. Inversion of Control (IoC) & Dependency Injection
5. Application Context
6. Application Component
7. Beans
8. Annotation Based Configuration of Components
9. Onion Architecture - Controllers, Services, Data access objects
10. Server-Wide Configuration with Properties File
11. Edge Case: XML Configuration
12. Spring Core

## Spring MVC & Thymeleaf

1. Model
2. View
3. Controller
4. HTML Templates with ThymeLeaf

## Data Persistence & Security

1. Spring Data JPA
2. Hibernate
3. Spring Security

## Project: Blog Application

### Part 1: CRUD

Blog application using Spring Boot, Thymeleaf and Spring Data JPA: CRUD

(This project contains **pagination**, **search**, **filtering** and **sorting**)

In project we make is a basic blog with features of posts and comments. We are skipping authentication for now. However all unauthorized actions or use cases below will be replaced with authentication in next project using spring boot.

This project uses following technologies

- Spring MVC as MVC framework
- Spring Data JPA for Database Connectivity
- Thymeleaf for theming and templates

#### Use Cases:

- Non logged in user should be able to read a list of blog posts that has title, excerpt, author, published DateTime and tags.
- Non logged in user should be able to read full blog post that has title, content, author, published DateTime and tags.
- Non logged in user should be able to filter blog posts using author, published DateTime and tags
- Non logged in user should be able to sort blog posts using the **published DateTime**
- Non logged in user should be able to search blog posts using full text search on title, content, author and tags
- Non logged in user should be able to navigate to different pages on blog list where each page lists maximum 10 blog posts.
- Non logged in user should be able to create blog post that has title, content, author, published DateTime and tags
- Non logged in user should be able to update a blog post that has title, content, author, published DateTime  and tags
- Non logged in user should be able to delete a blog post that has title, content, author, published DateTime  and tags
- Non logged in user should be able to comment on blog posts using comment form that contains name, email and comment
- Non logged in user should be able to read, update and delete comments.

#### Database Schema:

- User
    - id
    - name
    - email
    - password
- Posts
    - id
    - title
    - excerpt
    - content
    - author
    - published_at
    - is_published
    - created_at
    - updated_at
- tags
    - id
    - name
    - created_at
    - updated_at
- post_tags
    - post_id
    - tag_id
    - created_at
    - updated_at
- comments
    - id
    - name
    - email
    - comment
    - post_id
    - created_at
    - updated_at

#### Steps to make:

1. Make the HTML and CSS
2. Create database schema / Make database ready
3. Start replacing HTML & CSS with thymeleaf
4. and connect data with frontend using Spring MVC and Spring Data JPA

#### Steps M2:

1. Finish author and tags
2. Comments
3. Pagination on `/` in this format for for
    1. page 1: `http://abc.com/?start=1&limit=10`
    2. page 2: `http://abc.com/?start=11&limit=10`
    3. page 3: `http://abc.com/?start=21&limit=10`
4. Filters on `/`  in this fomat `http://abc.com/?authorId="1"&tagId="1"&tagId="2"`
5. Sorting on `/` in this format `http://abc.com/?sortField="publishedAt"&order="asc"`
6. Searching on `/` in this format `http://abc.com/?search="mountblue"` search should pick the union of all matches in title, content, tags, author and excerpt.

#### Steps M3:

- Authentication
- Authorization

`<input type="hidden" name="postId" value="1" />`

[[Abc]](/?tagId="1")

### Part 2: Authentication & Authorization

Blog application using Spring Boot, Spring Data JPA, Spring Security: Authentication & Authorization

- Thymeleaf
- pagination
- search
- filtering
- sorting
- Authentication and Authorization

In this project we make the same blog that has features like posts and commenting. Additionally we are adding authentication using Spring Security. All unauthorized actions or use cases below will have spring security's authorization feature using various roles.

This project using Spring Boot and uses following technologies of spring boot

- Spring MVC (Spring Boots configuration without XML)
- Spring Data JPA
- Spring Security
- Thymeleaf for theming and templates

#### Use Cases:

- Non logged in user and logged in user should be able to read a list of blog posts that has title, excerpt, author, published date & Time and tags.
- Non logged and logged in user in user should be able to read full blog post that has title, content, author, published date & Time  and tags.
- Non logged and logged in user in user should be able to filter blog posts that using author, published date & Time  and tags
- Non logged and logged in user should be able to sort blog posts using the published date
- Non logged and logged in user should be able to search blog posts using full text search on title, content, author and tags
- Non logged and logged in user should be able to navigate to different pages on blog list where each page lists maximum 10 blog posts.
- Logged in user with a role of **author** should be able to create blog post that has title, content, author (**disabled and contains his own name**), published date & Time  and tags.
- Logged user with a role of **author** should be able to update his own blog posts that has title, content, author  (**disabled and contains his own name**), published date & Time  and tags
- Logged in user with a role of **author** should be able to delete his own blog posts that has title, content, author (**disabled and contains his own name**), published date & Time  and tags
- Non logged and logged in user in user should be able to comment on blog posts using comment form that contains name, email and comment
- Logged in user should be able to update and delete comments made on his own blog posts.
- Logged in user with a role of **admin** should be able to create blog post that has title, content, author (**can be any author**), published date & Time  and tags.
- Logged in user with a role of **admin** should be able to update blog post that has title, content, author (**can be any author**), published date & Time  and tags.
- Logged in user with a role of **admin** should be able to delete blog post that has title, content, author (**can be any author**), published date & Time  and tags.

### Part 3: Deployment on Heroku & AWS

### Part 4: REST APIs for all features

REST APIs:

* All CRUD operations
* Pagination
* Search
* Filtering
* Sorting
* Authentication and Authorization

