# OWASP Juice shop 4 star challanges

1. Poison Null Byte Challange (**4 Star**)

- Go to /ftp route to see all ftp services of the server.
- Try to download package.json.bak file.
- We will get a 403 error, which says that we can download only .md and .pdf files.
- To overcome this problem, we will use a character bypass called **Poison Null Byte**.
- %00 is the poison null byte.
- We have to encode it into url.
- Add %2500.md at the end of the url.
- It bypasses the 403 error and downloads the file.

- **Explanation** :
  - A poison Null byte is actually a NULL terminator.
  - By placing a NULL character in the string at a certain byte, the string will tell the server to terminate at the point nulling the rest of the string.

2. Perform Persistant XSS attack (**4 Star**)

- Login as admin and go to last login section.
- We see that a last login is always logged sending the last login IP to the server.
- Logout from the account and capture the logout request.
- See the request headers.
- Add a new header to the request, **True-client-IP** : `` <iframe src="javascript:alert(`xss`)" > ``

3. Access backup files (**4 star**)

- Go to **http://localhost:3000/#/ftp**.
- Try to download any non .md or .pdf file.
- Perform a Null byte attack to download the file.

4.
