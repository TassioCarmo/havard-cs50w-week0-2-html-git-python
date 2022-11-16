# Introduction to javascript, html and CSS
## what did i learn

# Sass (Syntactically Awesome Style Sheets)

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
# Git

Git is a command line tool that helps with version control in several different ways: 

- Allowing us to keep track of changes we make to our code by saving snapshots of our code at a given point in time.
- Allowing us to easily synchronize code between different people working on the same project by allowing multiple people to pull information from and push information to a repository stored on the web.
- Allowing us to make changes to and test out code on a different branch without altering our main code base, and then merging the two together.
- Allowing us to revert back to earlier versions of our code if we realize we’ve made a mistake.

## Commands

- <code>git clone <repository url>.</code> This will download the repository to your computer. 
- <code>ls</code> lists all files and folders in your current directory.
- <code>cd <repository name></code> change directory into that folder.
- <code> touch <new file name> </code> creates a new file in that folder. You can now make edits to that file.
- <code>git add <new file name></code> to tracks that specific file, 
- <code>git add .</code> tracks all files within that directory.
- <code>git commit -m "some message"</code> message describes the changes you just made.
- <code>git status</code> See how the code compares to the code on the remote repository
- <code>git push</code> Send to github all the changes.
- <code>git log</code> Gives the history of all of your commits on that repository.
- <codeO>git reset --hard <commit></code> reverts your code to exactly how it was after the specified commit. To specify the commit, use the commit hash associated with a commit which can be found using git log as shown above.
- <code>git reset --hard origin/master</code> reverts your code to the version currently stored online on Github.
- <code>git branch</code>  see which branch you’re currently working on, which will have an asterisk to the left of its name.
- <code>git checkout -b <new branch name></code> Make a new branch
- <code>git checkout <branch name></code> Switch between branches
- <code>git merge <other branch name></code>. This will be treated similarly to a push or pull, and merge conflicts may appear.

If you’ve only changed existing files and not created new ones, instead of using **git add** . and then **git commit**..., we can condense this into one command: <code>git commit -am "some message"</code>. This command will commit all the changes that you made.

Sometimes, the remote repository on GitHub will be more up to date than the local version. In this case, you want to first commit any changes, and then run <code>git pull</code> to pull any remote changes to your repository.
    

### Commit
    
Save points in other words "i want to save the current state of all the files in the repository"
    
Making lots of commits as you make lots of changes to your program. You'll commit and commit again after each new addition you make to the project. And you might want to refer back to a previous commit, but it's only valuable to do so if you can identify in which commit you made a particular change
    
## Merge Conflicts

 One problem that can emerge when working with Git, especially when you’re collaborating with other people, is something called a merge conflict. A merge conflict occurs when two people attempt to change a file in ways that conflict with each other.
    This will typically occur when you either git push or git pull. When this happens, Git will automatically change the file into a format that clearly outlines what the conflict is. Here’s an example where the same line was added in two different ways:
    
    ![image](https://user-images.githubusercontent.com/31789624/202058208-ebbeb43d-3bb2-4b95-94bf-fd6e397315d1.png)


## Branching
    
Branching is a method of moving into a new direction when creating a new feature, and only combining this new feature with the main part of your code, or the main branch, once you’re finished. This workflow will look more like the below graphic:

![image](https://user-images.githubusercontent.com/31789624/202058303-aae81d72-626a-43cb-87f5-9a31b2ecc757.png)
    
###  More GitHub Features

- Forking: As a GitHub user, you have the ability to fork any repository that you have access to, which creates a copy of the repository that you are the owner of. We do this by clicking the “Fork” button in the top-right.
-  Pull Requests: Once you’ve forked a repository and made some changes to your version, you may want to request that those changes be added to the main version of the repository. 

# Python
    
### Strings

- Ordered: Yes
- Mutable: No
    
### Lists

- Ordered: Yes
- Mutable: Yes

### Tuples

- Ordered: Yes
- Mutable: No


## Functional Programming

In addition to supporting Object-Oriented Programming, Python also supports the Functional Programming Paradigm, in which functions are treated as values just like any other variable.

### Decorators

One thing made possible by functional programming is the idea of a decorator, which is a higher-order function that can modify another function. For example, let’s write a decorator that announces when a function is about to begin, and when it ends. We can then apply this decorator using an @ symbol.

```
def announce(f):
    def wrapper():
        print("About to run the function")
        f()
        print("Done with the function")
    return wrapper

@announce
def hello():
    print("Hello, world!")

hello()

""" Output:
About to run the function
Hello, world!
Done with the function
"""
```
### Lambda Functions

Lambda functions provide another way to create functions in python. For example, if we want to define the same square function we did earlier, we can write:

    <code>square = lambda x: x * x</code>

