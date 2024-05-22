# Micro_CMS_V2 ( LEVEL 3 )

## Flag 1

- Try creating a new page. It redirects you to login page.

- Add ' after the username field in the login form.

- Bypass login using this sqli script `' UNION SELECT '123' AS password#` and enter 123 as password.

- You will be logged in.

- Go to the private page to get the flag.

## Flag 2

- Try editting a page with the normal user.

- You will get redirected to login page.

- Intercept the edit request and change its method to post.

- You will get the flag in the response.

## Flag 3

- Hint: Credentials are secret, flags are secret. Coincidence ?

- We have to find the username and password for the login profile.

- Capture the POST login request in burp and send it to the intruder.

- Write the poisioned query : `' AND LENGTH(USERNAME)=$_$&password=pwd` and use 1 - 10 as the payload of the sniper attack.

- Do same query for the passwrd. There queries will give you the length of the username and password.

- Use the query `'username LIKE ($_$)` use variable only the no. of times the length of the username

- Use the same query to get the password using sniper attack.

- Login using the credentials, get the flag.
