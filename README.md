# UI-exercise
Angular exercise for UI interview candidates

# Instructions
This repository contains instructions and wireframe diagrams for the assignment  that we are asking front-end candidates to complete.

You can either download the [PDF Instruction](https://github.com/arif-mf/UI-exercise/blob/master/MicroFocus-UI-exercise-specifications.pdf?raw=true) and 2 images([#1](https://github.com/arif-mf/UI-exercise/blob/master/MF-UI-exercise-wireframes-1-of-2.png?raw=true), [#2](https://github.com/arif-mf/UI-exercise/blob/master/MF-UI-exercise-wireframes-2-of-2.png?raw=true)) locally for easier viewing or continue reading this README.
> you'll need to enlarge the images to see the wireframes clearly 

# Objective
Build an Angular application which does the following:
1. Displays a list of message posts
2. Enables a user to log in and submit new posts or edit existing posts

# General Requirements
1. Must be an Angular project generated with the Angular CLI
2. Uses standard Bootstrap styles
3. Conforms to the page layouts as shown in the attached wireframes
4. Must not use 3rd party libraries, e.g. underscore
5. Uses the following REST API to obtain user and post data:
  > https://jsonplaceholder.typicode.com/posts
 https://jsonplaceholder.typicode.com/users




# Application Requirements

## Home page
1. When launching the application, the user is sent to the Home page by default
2. If the user is not logged in, show "Log In" button
3. If the user is logged in, show a “Welcome” message with the user's full name
4. Keep the user logged in (across browser sessions) until the user logs out
5. Display a table with the following details.
    <ol type="a">
      <li>a User column containing the user’s full name and company name</li>
      <li>a Post column containing the post title and post body</li>
      <li>show 10 rows per page</li>
      <li>a "New Post" button, which is visible after user logs in</li>
      <li>a Log Out button, which is visible after the user logs in</li>
      <li>a set of left/right arrows (buttons) for paging</li>
    </ol>
6. The Home page should support the following actions:
    <ol type="a">
      <li>pressing the Log In button sends the user to the Log In page</li>
      <li>clicking on the company name in the User column goes to the company web site</li>
      <li>clicking on the right arrow displays the next 10 posts (disabled if no more posts)</li>
      <li>clicking on the left arrow displays the previous 10 posts (disabled if no previous posts)</li>
      <li>
        <div>in logged in state, New Post and Log Out buttons are shown</div>
        <ol type="i">
          <li>New Post button navigates to Post Edit page in empty state</li>
          <li>Log Out button kills user session and refreshes Home page</li>
        </ol>
      </li>
    </ol>
7. in logged in state, clicking on post title navigates to Post Edit page in edit state
    <ol type="a">
      <li>The user should only be able to edit their own posts</li>
    </ol>

## Login page 
1. Contains the following fields:
    <ol type="a">
      <li>User Name field</li>
      <li>Log In button</li>
    </ol>

2. Log In button should be disabled until the user name is entered
3. If the user name does not match a user from the /users endpoint, display an error
message
4. If the user name matches a user from the /users endpoint, send user back to Home
page in logged in state
## Post Edit page
1. The same form should be used for submitting new posts, as well as editing existing
posts
2. The form contains the following elements:
    <ol type="a">
      <li>Title and Message fields</li>
      <li>Delete button (in edit state only)</li>
      <li>Save/Cancel button</li>
      <li>“Go back to Home page” link (displayed in header)</li>
    </ol>
3. The form should enforce the following validation rules:
    <ol type="a">
      <li>the Title and Message fields cannot be empty</li>
      <li>title cannot be longer than 200 characters</li>
      <li>message cannot be longer than 2000 characters</li>
      <li>validation errors should appear below the field that is in error</li>
      <li>Save and Cancel buttons should be enabled only when form has been modified and has no validation errors</li>
      <li>if the user attempts to navigate away from the page with unsaved data (for example, when clicking on “Go back to home page” header), display a confirmation dialog and allow the user to remain on the page</li>
    </ol>

4. The form should support the following actions (NOTE: the REST endpoint does not actually post or update a resource, so the data must be managed locally, i.e. faked):


    <ol type="a">
      <li>when a new post is saved, the user should be sent back to the Home page, with the newest post shown first in the table</li>
      <li>when an existing post is updated, the user should be sent back to the Home page, with a message indicating that the post was saved</li>
      <li>when a post is deleted, show a confirmation window, e.g. “Are you sure you want to delete this post?”</li>
    </ol>

## Build the application according to the specifications detailed in this readme or PDF document. Refer to the wireframes for UI layout.

Submit your completed assignment by doing either of the following:
1. Publish on your own Github public repository
2. zip up the project (excluding the node_modules folder) and send to your Microfocus recruiter contact

# Wireframes

Refer to the attached wireframes ([#1](https://github.com/arif-mf/UI-exercise/blob/master/MF-UI-exercise-wireframes-1-of-2.png?raw=true), [#2](https://github.com/arif-mf/UI-exercise/blob/master/MF-UI-exercise-wireframes-2-of-2.png?raw=true)) for guidance.
