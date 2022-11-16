# Introduction to javascript, html and CSS
## what did i learn

## Sass (Syntactically Awesome Style Sheets)

Sass is a language that allows us to write CSS more efficiently in several ways, one of which is by allowing us to have variables

When writing in Sass, we create a new file with the extension filename.scss. In this file, we can create a new variable by adding a $ before a name, then a colon, then a value. For example, we would write $color: red to set the variable color to the value red. We then access that variable using $color. Here’s an example of our variables.scss file:

```
$color: red;

ul {
    font-size: 14px;
    color: $color;
}

ol {
    font-size: 18px;
    color: $color;
}

```

- Web browsers only recognize .css files. To deal with this problem, we have to download a program called Sass onto our computers. Then, in our terminal, we write 

<code>sass variables.scss:variables.css</code>

- This command will compile a .scss file named variables.scss into a .css file named variables.css, to which you can add a link in your HTML page.

- To speed up this process use the command <code>sass --watch variables.scss:variables.css</code> which automatically changes the .css file every time a change is detected in the .scss file.
- While using Sass, we can also physically nest our styling rather than use the CSS selectors we talked about earlier. For example, if we want to apply some styling only to paragraphs and unordered lists within a div, we can write the following:


Sass also gives us **inheritance**. We do this by adding a % before a name of a class, adding some styling, and then later adding the line @extend %classname to the beginning of some styling

```
%message {
    font-family: sans-serif;
    font-size: 18px;
    font-weight: bold;
    border: 1px solid black;
    padding: 20px;
    margin: 20px;
}

.success {
    @extend %message;
    background-color: green;
}

.warning {
    @extend %message;
    background-color: orange;
}

.error {
    @extend %message;
    background-color: red;
}
```
## Git

Git is a command line tool that helps with version control in several different ways: 

- Allowing us to keep track of changes we make to our code by saving snapshots of our code at a given point in time.
- Allowing us to easily synchronize code between different people working on the same project by allowing multiple people to pull information from and push information to a repository stored on the web.
- Allowing us to make changes to and test out code on a different branch without altering our main code base, and then merging the two together.
- Allowing us to revert back to earlier versions of our code if we realize we’ve made a mistake.

### Commands

- <code>git clone <repository url>.</code> This will download the repository to your computer. 
- <code>ls</code> lists all files and folders in your current directory.
- <code>cd <repository name></code> change directory into that folder.
- <code> touch <new file name> </code> creates a new file in that folder. You can now make edits to that file.
