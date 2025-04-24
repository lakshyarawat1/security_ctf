# Brute Force 

## Security level : Low

- Set security level to low in DVWA
- Go to Brute Force page in DVWA
- Enter username and password in the form and click on login button
- It shows invalid credentials.

## Solution

- Turn on burpsuite and intercept the login request using burpsuite proxy.
- Send the request to intruder.
- Add the payload positions in the request.
- Add the payloads in the payloads tab.
- Set the attack type as cluster bomb.
- Start the attack.
- It will go through all the combinations of the payload and will give the responses.
- Check for a different length of response or any other response code.
- It will show the valid credentials in the response.
- Use the valid credentials to login to the DVWA application.

