# Software Requirements

Software Requirements is a *VAST* field of study. It has many methodologies and takes years to master.

In this section, we cover a tiny fraction of the field, Just enough to write requirements for very small projects.

1. User Personas - [How to define a User Persona](https://careerfoundry.com/en/blog/ux-design/how-to-define-a-user-persona/)
2. User Stories - [Writing User Stories](https://www.mountaingoatsoftware.com/agile/user-stories)
3. Wireframes - [Website Wireframes](https://en.wikipedia.org/wiki/Website_wireframe)

In this section, you will **only write the software requirements** for the toy project. The actual code will come in the next section.

## User Stories

Before you start coding your project, you will define the requirements for the project. For this project, we will use User Stories. [User Stories](https://en.wikipedia.org/wiki/User_story) are a lightweight way to capture software requirements, it is popular with proponents of Agile Development.

Objective:

* To build a fully functional modern website.
* Ability to break a product into user stories.
* Ability to complete a single user story and make it available to the user.
* Ability to implement authentication, strategies for image upload, video upload.
* Ability to add complex relationships in tables to develop features - likes, threaded comments.

Pick a social network of your choice. Popular choices in the past have included:

* Facebook
* Youtube
* Instagram
* Reddit
* Pinterest

### Step 1:

Determine your user.
[Defining the User](https://careerfoundry.com/en/blog/ux-design/how-to-define-a-user-persona/)

### Step 2:

Come up with user stories for your user persona.
[User Stories](https://www.mountaingoatsoftware.com/agile/user-stories)

### Step 3:

Deploy your code to Heroku ( optionally to AWS) (Yes before starting your project)

### Step 4:

Prioritize stories. Can you make a feature available to your user on Day 1?

Build user stories 1 by 1. Push each story when done.

### Dummy User Stories

Blogging Engine with Authentication

* As a reader I should be able to (henceforth ISBAT) see all blogs.
* As a reader ISBAT register and register myself as a blogger. (Sign Up)
* As a reader ISBAT login and become blogger. (Authentication)
* As a blogger ISBAT create a blog post.
* As a blogger ISBAT delete my own blog post.
* As a blogger ISBAT update my blog post.
* As a reader ISBAT see an error page if I enter wrong URL. (Error Handling)

Bonus:
* As a reader ISBAT search any text. (Full text Search)
* As a reader ISBAT export blogpost as text file. (Use Celery for background jobs)

### Tasks

1. Choose a domain for your project.
2. Limit your requirements to
      * CRUD (Create, Read, Update and Delete) operations
      * Authentication
      * Authorization
      * Registration
      * Error Handling
3. Have a proper .gitignore file, README.md file with instructions to run development environment and deploy.
