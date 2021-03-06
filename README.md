web-dev
=======

I created this application while taking the Udacity intermediate web development course, 
and it is deployed here: http://created-by-rachel.appspot.com/

It uses the webapp2 framework and google app engine, including the google app engine query language and memcache.
Jinja2 is used for templating, and bootstrap for styling.

Nifty features include:
- input validation
- passwords are salted and hashed before they are stored
- cookies are set once a user is logged in with a hashed version of their user id and are necessary to access any site pages  
- users' ip addresses are used to look up geographic coordinates to plot on a map
- responsive navigation bar
- queries from the database are cached with memcache
- password reset sends email with a link to reset password, link expires after 12 hours or after it is used once

To Run:
appcfg.py --oauth2 -A created-by-rachel update app/

To Test:
dev_appserver.py app --enable_sendmail

To Do:
- allow incoming email
