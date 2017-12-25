Making a Super Simple Registration System With PHP and MySQL

Writing a registration system is a lot of work. You have to write code that validates email addresses, sends confirmation emails, provides forgotten password functionality, stores passwords securely, validates input forms and a lot more. Even when you do all of this, users will still be reluctant to register as it involves a lot of effort on their part as well.

In this tutorial, we will make a very simple registration system that doesn't require or store passwords at all! The result will be easy to modify and embed into an existing PHP website. Read on to find out how it works.

The Idea
Here is how our super simple registration system will work:
There will be a combined login/registration form, where users will fill in their emails and hit submit;
Upon submission, if an email address is not found in the database, a new user record is created. A random token is generated and sent to the user via email as a clickable link that is only valid for 10 minutes;
Clicking the link in their inbox will take them to our site. The system will detect the presence of the token and will log the person in.
Here are the advantages of this approach:
No need to store and validate passwords;
No need for a password restoration feature, secret questions etc;
You can be certain that a person can be reached on the given email address from the first time they login;
The registration process is very simple and inviting.
Here are the disadvantages:
It is as secure as the user's email account. If somebody has access to the person's email, they can login. This is the case with any forgotten password feature, but is a thing to consider;
Email is not secure and can be intercepted. Keep in mind that this is also the case with any forgotten password feature or any regular login system that doesn't use HTTPS to transfer username/password info;
Unless you take the time to configure your outgoing email properly, there is a chance that the messages with the login links will hit the spam box;
Given the advantages/disadvantages above, our login system is high on usability but not very high on security, so you should only use it for things like forum registrations, site memberships and services that don't deal with sensitive information.


