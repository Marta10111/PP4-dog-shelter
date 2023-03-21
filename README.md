# Dog Shelter

## Purpose of this site

This site has been created so that users can see informations about dogs for adoption. Unregistered Users can view a summary of the posts, and see number of likes and comments.
Registered Users can comments and like doggies' profiles.

## User Experience

### User Goals

#### First Time User would like to:
- find out the purpose of the site and how to use it
- be able to easily navigate throughout the site
- see the list of posts to see if the site is something they would be interested in
- be able to register for a user account

#### Registered User would like to:
- be able to sign into their user account
- view posts, leave comments and likes
be able to log out to keep their account safe

#### Site Admin would like to:
- restrict access to non-registered users
- control users comments for inappropriate content. Approve comments before adding them to the site.

### User Stories

I used Github issues to add following user stories:

- Approve comments: As a Site Admin I can approve or disapprove comments so that I can filter out any inappropriate comments.
- Create drafts: As a Site Admin I can create draft posts so that I can finish writing the content later.
- Manage Posts: As a Site Admin I can create, read, update, and delete posts so that I can manage my blog content.
- Like/unlike: As a Site User I can like or unlike a post so that I can interact with the content.
- Comment on post: As a Site User I can leave comments on a post so that I can be involved in the conversation.
- Account registration: As a Site User I can register an account so that I can comment and like posts.
- View comments: As a Site User or Admin I can view comments on an individual post so that I can read the conversation.
- View likes: As a Site User or Admin I can view the number of likes on each post so that I can see which is the most popular.
- Open a Post: As a Site User I can click on a post so that I can read the full text.
- View Post List: As a Site User I can list of posts so that I can select one to read.
- Site Pagination: As a Site User I can view a list of posts so that easily select a post to view.

### Agile Development Tool

For this project I was using an Agile Software Development tool in the development of this website.  I am using Github Projects, using a basic Kanban Template.  I added automation so that as each new issue is added, it adds it to the 'To Do' list for my project.  As I start working on each issue I move it to the 'In progress' column.  When the coding for each issue has been completed, the issue is then moved to the 'done' column.

![kanban board in progres](/documentation/images/kanban1.jpg)
![kanban board done](/documentation/images/kanbanDone.jpg)

### Wireframes

I have used Balsamiq to create the following wireframes for both desktop and mobile devices.

![Balsamiq wireframe](/documentation/images/Balsamiq.jpg)

## Existing Features

### Navbar and Footer

#### Navbar

The navbar is plain and simple so that it is very easy for the user to read.  The name of the website is clear in the top left-hand corner - Dog Shelter. There are links to Home, Register and Login pages for all users. If the user is not signed in, the sign in and register links are visible on the navbar. 

![Navbar](/documentation/images/Navbar.jpg)

If the user is signed in, then there is a Logout link visible.  Also on the right-hand corner there is a short message showed.

![Navbar](/documentation/images/Navbar1.jpg)

In mobile view the navbar is collapsed into a hamburger icon, which when clicked shows the same information as in desktop view.

![Navbar](/documentation/images/navPhone.jpg)

#### Footer

The footer is very simple with minimal information, just displaying social media options.  When the icons are clicked, they open in a new tab so that the user still has my web site open.

![Footer](/documentation/images/footer.jpg)


### Register Page

I have used Allauth for register, login and logout.

When a user clicks the register button they are brought to the register page where they have to fill in their username, an email address but this is optional and their password, which they then have to confirm. Then the user can click the button to sign up. If the user has come to register instead of login, there is text to say if you have already an account click login. If the registration is successful the user is redirected back to the home page and a message just below the navbar will appear for 2 seconds to say successfully signed in as 'username'.

![SignUp](/documentation/images/signup.jpg)

### Login Page

If a user has already registered they can log into the site in the login page.  The user is asked for their username and password. If correct the user is redirected back to the home page to begin their viewing. A message will appear under the navbar for 2 seconds to say successfully signed in as 'username'.

![SignIn](/documentation/images/signin.jpg)

### Logout Page

The user is asked are they sure they want to logout and then they can click the sign out button. The user is redirected back to the home page. A message will appear for 2 seconds under the navbar to say you have signed out.

![SignOut](/documentation/images/signout.jpg)

### Home page

The simple home page consists informations about web page purpose and contact details.

![Home page](/documentation/images/homePage.jpg)

Under these short intro there's a post list section. 

### Posts Section

 This section can be seen by both logged in and unlogged in users. I wanted the unlogged user to get a look at what the page offered so that they might then register and login. This page shows dog name, age, gender, breed, date and time when post was created and number of likes under eacg photo. 
In mobile view each post is the full width of the screen and the user can scroll down to see the other posts.

![Posts on mobile](/documentation/images/mobilePosts.jpg)

In desktop there are 6 posts per page, with 3 on the top row and 3 underneath.  If there are more than 6 posts there is a next button to look at the next page of posts and also a previous button to navigate back to the previous pages.

![Posts on screen](/documentation/images/PCPosts.jpg)
![Nexi,Prev button](/documentation/images/nextButton.jpg)

I have added the alt attribute on images for screen readers to make the site more accessible. I have also capitalized the title so the page looks more uniform.

For logged in users only,they can click on the choosen dog name to view all the doggo details( about me and type of home needed).

### Post Detail page

This page can only be accessed by logged in users. I have added alt atributes for the images for accessibility.
On mobile view the image is not displayed as it takes up too much room. There is a header banner which includes the dog name,author time and date when post was created.  Then under the banner is the content from the post.  Under the content there is a heart icon which acts as a button to allow the user to like or unlike the post.  If the heart is filled in red it means that this user has liked the post.  If the heart was just an outline in red it means this user has not liked this post.  There is logic in place that if a user has liked the post if they then click the heart again it will unlike the post. There is also a number beside the heart to show how many likes this post has. Also there is a comment icon again with a number to show how many comments was made.

![Post on mobile](/documentation/images/mobilePost1.jpg)

This user has not liked this post as the heart is just an outline.

![Post not liked](/documentation/images/postNotLiked.jpg)

This user has liked this post as the heart is filled in with
 red.

![Post liked](/documentation/images/postLiked.jpg)

Under this is the comments section, so it displays any comments that have been left on this post with the commenters name and date they left the comment.  Under this there is a simple form for the user to add a comment and submit it. When the submit button is clicked the user is redirected back to the detail post and the post now is waiting for an Admin approval before it can be posted on page.

![comments](/documentation/images/comments.jpg)

### Admin

I created a superuser so only he can add page content(create,edit and delete posts).

### Data Model

I needed two data models to make this website work.  The first data model is the Post. This contains the information for the post.  I have a second data model for the comments which are linked to a post.

#### Dog post model

| Key | Name | Type
|-----|----------------|------------------|
| | title (unique) | Char(200)
|foreign key | author | User Model
| | created_date | DateTime
| | updated_date | DateTime
| | content | TextField
| | featured_image | Cloudinary_image
| | excerpt | TextField
|many-to-many | likes | User Model

#### Comment model

| Key | Name | Type
|--------|----------------|-------------------|
|foreign key | post | Post Model
| | name | Char(80)
| | body | TextField
| | created_on | DateTime
| | approved | Boolean

### Typography

The fonts I have selected are : Sans-serif for the text and Lato for the page name. These have been selected as they are clear and simple.

### Languages

- HTML
- CSS
- Python

### Frameworks, libraries and programs

- Django
- Bootstrap 
- Google Fonts
- Font Awesome for icons
- Github/Gitpod
- Cloudinary for store images
- Gunicorn as server for Heroku
- Heroku used for deployment
- Summernote as editor
- postgreSQL for database
- balsamiq for wireframes
- Allauth for account registration

## Code VAlidation

### HTML validation

To validate each of my html pages I inspected the page through devtools and viewed the page source and copied and pasted this into the W3C markup validation service.

![Base checker](/documentation/testing/baseChecker.jpg)

![Index checker](/documentation/testing/indexchecker.jpg)

![Post checker](/documentation/testing/postchecker.jpg)

### CSS Validation

I copied my style.css file into the W3C CSS validation service.

![CSS checker](/documentation/testing/cssChecker.jpg)

### Extendclass

I copied and pasted my python files into the Python Code Checker

blog>views.py

![blog.views.py](/documentation/validation/viewsChecker.jpg)

blog>models.py

![blog.models.py](/documentation/validation/modelsChecker.jpg)

blog>forms.py

![blog.forms.py](/documentation/validation/formsChecker.jpg)

blog>urls.py

![blog.urls.py](/documentation/validation/urlsChecker.jpg)

dogShelter>settings.py

![dogShelter.settings.py](/documentation/validation/settingsChecker.jpg)

dogShelter>urls.py

![dogShelter.urls.py](/documentation/validation/urlsChecker1.jpg)

## Testing

### Manual testing

I checked each page to make sure everything look correct at all screen sizes using devtools. 

I have used the user stories as a structure to manually test my project. This testing was on fully deployed site on Heroku.

- as Admin I can create a post

If I do not enter data in the required fields it gives a warning to add data to the required fields. It is ok not to have data in the excerpt field. It is also ok not to include an image. 

![showing warnings for required fields](/documentation/testing/manual/admin_add_post_required.jpg)

When all required fields are filled and the post is saved, we get a success message and can see the new post.

![show success message](/documentation/testing/manual/admin_add_post_success.jpg)

- as Admin I can update a post

Similar to create post in update if any of the required fields are not filled a warning is shown and fields that need to be filled are highlighted. When all required fields are filled a success message is given and I can see the updated post.

![show message post changed successfully](/documentation/testing/manual/admin_updating_post.jpg)

- as admin I can delete a post

When the admin selects the post they want to delete, select action - delete and then clicks go, the admin is asked are they sure they want to delete this post. They have the option of going back or deleting the post.

![show post for delete](/documentation/testing/manual/admin_delete_post.jpg)

- as Admin I can delete a comment

Similar to delete a post I can also delete a comment if its necessary. The steps are same as when deleting a post.

![admin delete comment](/documentation/testing/manual/admin_delete_comment.jpg)

![admin delete comment](/documentation/testing/manual/admin_delete_comment1.jpg)

![admin delete comment](/documentation/testing/manual/admin_delete_comment2.jpg)

- as a site user I can view the number of likes under each post - both logged in and not logged in users can see the number of likes on the main page.

![number of likes](/documentation/testing/manual/likes.jpg)

- as a logged in user I can view a list of posts so i can select one to view by clicking on a dog name. Post details are showed (dog,info, number of comments, comments and add comment window)

![post details](/documentation/testing/manual/post_info.jpg)
![comment form](/documentation/testing/manual/comment_form.jpg)

I can also like and unlike post.

![post liked](/documentation/testing/manual/post_liked.jpg)
![post unliked](/documentation/testing/manual/post_unliked.jpg)

- as a new user I can register so that I can comment and like posts

For register, checks with user if they already have an account and if so they can click login which redirects them to the login page.

Allauth checks if the username has been used before.

![user already exist](/documentation/testing/manual/user_exist.jpg)

Checks that a username has been entered.

![empty username window](/documentation/testing/manual/no_username.jpg)

Checks that a password must be entered.

![empty password window](/documentation/testing/manual/no_password.jpg)

For login, checks that the user has an account and if not redirects them to register page.

Warning if username not entered.

![login no username](/documentation/testing/manual/login_no_user.jpg)

Warning if password not entered

![login no password](/documentation/testing/manual/login_no_password.jpg)

Warning if the user isn't a registered user

![user not registered](/documentation/testing/manual/not_registered.jpg)

### Lighthouse

![lighthouse results](/documentation/testing/manual/lighthouse.jpg)

### Bugs

- blank line contains whitespace - fixed
- no new line at the end of file - fixed
- ms.toolsai.vscode- jupyter- slideshow extention is not synced, but not added in gitpod.yml - not fixed

### Deployment to Heroku

Initial deployment:

I followed the 'I think therefore I blog' walkthrough to create a basic django project.  I used the code institute template. 
- I installed django and supporting libraries:
I installed django, gunicorn, psycopg2, cloudinary with pip3 install django gunicorn dj_database_url psycopg2 dj-3-cloudinary-storage
I created the requirements.txt file with pip3 freeze > requirements.txt

- I created a new django project called 'dogShelter' and a django app called 'blog'.
python3 manage.py startapp blog
I need to add blog to installed apps in settings.py.
After adding new app we need to migrate the changes to the database.
python3 manage.py migrate

- I set the project to use Cloudinary and PostgreSQL database.
I created a heroku app called pp4dogshelter.
I attached it to the database, in resource tab searched for postgres and attached. Then in config vars copy the text beside DATABASE_URL

-I created an env.py file - this contains all the secret environmental variables. I need to reference this in settings.py file. Added env.py to the .gitignore file.
In the env.py file import os library.
add os.environ["DATABASE_URL"] = copied string from heroku
add os.environ["SECRET_KEY"] = make up randon key -add this secret key to heroku config vars
I connected to cloudinary and tell django to use cloudinary to store media and static files.
add os.environ["CLOUDINARY_URL"] = "cloudinary://<insert-your-url>" - add this to heroku config vars
in heroku config vars add DISABLE_COLLECTSTATIC with value 1 - this has to be removed before final deployment
I set up for static and media at the bottom of settings.py file.
I needed to tell django where our templates will be stored.
I needed to add heroku host name into allowed hosts in settings.py file.
I needed to create 3 directories at the same level as manage.py file for media, static and templates.
I needed to create a Procfile this tells heroku how to run our project.

- I deployed the empty project to Heroku.
In Heroku in the deploy tab,
I click GitHub,
I search for my repo,
Then scroll down and deploy branch.
I watched the build to check it was successful and
then opened the app.
I have included a env.sample file which is a copy of my env.py file without the secret information.  This is to show what secret keys are required.

-When I had completed my testing in development, in the settings.py file I set DEBUG = False and added X_FRAME_OPTION = 'SAMEORIGIN'.
I git add ., then git commit and git push.
In Heroku I went into config vars and deleted the DISABLE_COLLECTSTATIC = 1
In the deploy tab in Heroku, I deployed branch and watched the build to check it was successful. Then I opened the app and repeated all my testing to ensure this worked the same as my local testing.

## Credits 

- I used 'I think therefore I blog' to set up files, Heroku app, Cloudinary, environmental variables and GitHub Projects.
- I used GitHub Projects and Kanban for user stories like 'I think therefore I blog'
- I used card system from 'I think therefore I blog' for displaying posts.
- I used the messages from 'I think therefore I blog'
- To help with crud functionality I used Dennis Ivy Youtube video for to do list app.
- I got help for showing active page on navbar from 'Favoureats' by Siobhan Gorman.
- I followed structure of readme from JoGorska_alumni_lead.
- I used bootstrap links from 'I think therefore I blog'.
- I used 'I think therefore I blog' for the bases of my footer.
- I used Dog Trust Ireland for doggos stories.
- I got the post pictures from - fansshare.com -Cash, zinfos974.com/-Butch, agxii.com -Coco, dogtrust.ie -Tasha, shop21307.babieseverywhere.org -Ben, adobe.com - Tobby.
- I use You Tube tutorials to help me make what I was planning:
<br><a href="https://youtu.be/m3hhLE1KR5Q" rel="nofollow">
https://youtu.be/m3hhLE1KR5Q
</a>
<br><a href="https://youtu.be/bPQfd5x_G84" rel="nofollow">
https://youtu.be/bPQfd5x_G84
</a>
<br><a href="https://youtu.be/dPSST_3jyJ0>" rel="nofollow">
https://youtu.be/dPSST_3jyJ0</a>

## Acknowledgements

- I would like to thank my classmates from Code Institute who supported me in these project: Ivette -cohort and Iris.
- Help and support from my mentor Martina.