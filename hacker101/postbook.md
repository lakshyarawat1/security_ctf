# PostBook

## Flag 1

- Go to signIn page and try using simple weak passwords

- Use `user` and `password` respectively to sign in and get the flag.

## Flag 2

- After signing in view a page.

- Change the pageID in the url to see other pages.

- You will get a flag in index 2.

## Flag 3

- Try IDOR.

- Go to write a new post page and fill the form.

- Notice a hidden field called user ID.

- Capture the post request in burp and change is user Id to 1

- The post will be written as author admin and you will get the flag.

## Flag 4

- Go to view page and change the pageId to a very large number.

- Try 945 and you will get a flag.

## Flag 5

- Try to edit the page and change the page Id in the url to any other Id.

- You will be able to edit the posts of other users.

- You will get the flag after changing the post.

## Flag 6

- Inspect the home page and its cookies while getting logged in as a user.

- Check the session cookie

- It has an id, decode the id as MD5 and it is the userId.

- Encode a new id with userId as 1 and set the id in the cookie.

- Refresh the page to get logged in as the admin.

- Get the flag in the home page.

## Flag 7

- Click delete a post button and capture the request.

- See that the post Id is just an MD5 hash of the real postId.

- Change the postId to the hash of other users POst ID.

- Once other user's post is deleted you will get the flag.

# Happy hacking !
