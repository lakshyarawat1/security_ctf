# Micro_CMS_V1 ( LEVEL 1 )


## Flag 1

- Home page is the index with some links.

- Create a new page

- See in the url, this page is indexed 9.

- Check other pages using the url, `:url/edit/page/1`.

- Page no. 7 is showing 403 forbidden.

- Try to edit the page using edit url.

- Get the flag in the form field.


## Flag 2

- Go to page 1

- Try to SQLi this page using `/page/1'`

- Now try to SQLi the edit url of this page `/page/edit/1'`

- The flag will be displayed.

## Flag 3

- Go to index page and to page 1

- Click the edit page option.

- Set the title of the page as ``<script>alert`xss`</script>``

- Save the edit of the page.

- Go to home page.

- You will get the flag.

# Flag 4

- Go to the markdown page and edit the page.

- Enter the value as `<button onclick=alert(1)>Click me!</button>`

- Save it and go to the markdown page.

- Click on the button and get the flag from the HTML code .