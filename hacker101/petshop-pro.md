# Petshop Pro

## Flag 1

- Add a product to cart and checkout.

- Capture the checkout request and change the price to zero.

- You will get the flag when checked out.

## Flag 2

- We will have to brute force both username and password for the login.

- The login page is at the /login route of the app.

- We will use a burpsuite extension called turbo intruder for faster brute force.

- Add %s as the injection spaces and first brute force the username using the list of seclists as names.txt

- Then use the same request but add space to password field and change the payload to 10k-most-common.txt from seclists.

- You will get the credentials and the flag when you login using them.

## Flag 3

- The last flag can be taken using the xss attack.

- Click on the edit option for any product and add the xss payload to the form input `<script>alert("hello")</script>`

- When adding this product to cart, you will get the flag.

# Happy Hacking
