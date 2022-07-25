# What is HTTP? (HyperText Transfer Protocol)

HTTP is what's used whenever you view a website, developed by Tim Berners-Lee and his team between 1989-1991. HTTP is the set of rules used for communicating with web servers for the transmitting of webpage data, whether that is HTML, Images, Videos, etc.

# What is HTTPS? (HyperText Transfer Protocol Secure)
HTTPS is the secure version of HTTP. HTTPS data is encrypted so it not only stops people from seeing the data you are receiving and sending, but it also gives you assurances that you're talking to the correct web server and not something impersonating it.


- [] What does HTTP stand for?

		HyperText Transfer Protocol

- [] What does the S in HTTPS stand for?

		Secure

- [] On the mock webpage on the right there is an issue, once you've found it, click on it. What is the challenge flag?

		THM{INVALID_HTTP_CERT}

# task 2 : 

- []  What HTTP protocol is being used in the above example?

		HTTP/1.1

- []  What response header tells the browser how much data to expect?

		Content-length

# task 3  :



HTTP methods are a way for the client to show their intended action when making an HTTP request. There are a lot of HTTP methods but we'll cover the most common ones, although mostly you'll deal with the GET and POST method.

GET Request

This is used for getting information from a web server.

POST Request

This is used for submitting data to the web server and potentially creating new records

PUT Request

This is used for submitting data to a web server to update information

DELETE Request

This is used for deleting information/records from a web server.

Answer the questions below

- [] What method would be used to create a new user account?

		Post
- [] What method would be used to update your email address?

		Put

- [] What method would be used to remove a picture you've uploaded to your account?

		Delete

- [] What method would be used to view a news article?

		Get

# task 4 :



- [] What response code might you receive if you've created a new user or blog post article?

		201

- [] What response code might you receive if you've tried to access a page that doesn't exist?

		404

- [] What response code might you receive if the web server cannot access its database and the application crashes?

		503

- [] What response code might you receive if you try to edit your profile without logging in first? 

		401

# task 5 :



- [] What header tells the web server what browser is being used?

		User-Agent

- [] What header tells the browser what type of data is being returned?

		Content-type

- [] What header tells the web server which website is being requested?

		Host

# task 6 :
- []  Which header is used to save cookies to your computer? 

		Set-Cookie 

# task 7 : 



Make a GET request to /room

	http://tryhackme.com/room
	THM{YOU'RE_IN_THE_ROOM}

Make a GET request to /blog and using the gear icon set the id parameter to 1 in the URL field
	
	http://tryhackme.com/blog
	key= id / value = 1
	THM{YOU_FOUND_THE_BLOG}
	
Make a DELETE request to /user/1
	
	http://tryhackme.com/user/1 (delete)
	THM{USER_IS_DELETED}

Make a PUT request to /user/2 with the username parameter set to admin

	http://tryhackme.com/user/2 (put)
	key= username / value = admin
	THM{USER_HAS_UPDATED}

POST the username of thm and a password of letmein to /login

	http://tryhackme.com/login (post)
	key= username / value = thm
	key = password / value = letmein
	THM{HTTP_REQUEST_MASTER}