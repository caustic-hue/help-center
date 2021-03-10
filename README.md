# FalixNodes Help Center - Design Refresh
![image](https://i.imgur.com/YKRFCSL.png)

A new design of the help center is being worked on along with adding a few other things like filters, search, author, and options(Copy Link, Report, and Edit)

### File Structure
![image](https://i.imgur.com/suS9gIf.png)
If you plan to add or edit something and add extra files in the making, please follow the file structure to keep things neat and organized.

## Creating a New Article

NOTE: If you do not want to write down in HTML, you can write in Markdown instead and converted it to HTML using: https://markdowntohtml.com/

### ✍️ Creating the Article
By following the file structure above, create a `.html` file first in `/article-raw/` and into the proper category.
As an example, if you were to create an article that explains on how to install and use a plugin on Minecraft Java, the file would be created like `/article-raw/minecraft/plugins/plugin-name.html`.
Then start writing the article, the FalixNodes Help Center is completely written in HTML, so you'll need to use the HTML format.
Example:
```
<h1>Heading Title</h1>
<h2>Sub Heading Title</h2>
<p>Summary explaining how to do a certain task</p>
<img src="https://i.imgur.com/ABC123.png>
<pre>
name="demo"
<pre>
```
You can learn more this here: https://www.w3schools.com/html/html_elements.asp
### 🔗️ Creating the URL
Now to create a URL for your new article, which would be something like `https://help.falixnodes.net/article/minecraft/plugins/plugin-name/`
Remember to follow the file structure above, go ahead and create the folder then use `index.html`([Why?](https://www.namecheap.com/support/knowledgebase/article.aspx/183/27/what-is-an-index-page/)).
So, as an example, if we're creating an article under the plugin sub category under the Minecraft Java category, we would create a folder named something liked `plugin-name` in `/article/minecraft/plugins/`.
As for the code you need to use in the `index.html`, just copy the code directly from another article in `/article/`, not `/article-raw/`.

To display content to the article, make sure the URL is correct on line 60.

Also make sure to update the title name, date, and category name in the sidebar.

### 🗨️ Give Yourself Credit
In the help center, there is a sidebar in each article, which also displays the author. Please edit the sidebar area and put yourself down as the author, make sure to upload your avatar to `/src/img/author/`.
Also, when a user clicks on the author's name, it should direct users to their GitHub profile. We also allow you to put your Twitter or just put your Discord username(If you use Discord username instead, put `#` as the `href`).

### 📢️ Publishing 
Create a [pull request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests#:~:text=Pull%20requests%20let%20you%20tell,merged%20into%20the%20base%20branch.) on this repo and title it like this "New Post: Name of Article"
If you're editing an article, title it like "Edit: Name of Existing Article".

Your edit will be reviewed by [Korbs](https://github.com/KorbsStudio) along with your code to check for any [syntax error](https://developer.mozilla.org/en-US/docs/Glossary/Syntax_error).

GitHub does not host our help center, so when it is accepted, the code needs to be pushed to a VPS.
I would like to note that our help center is coded all from scratch and does not rely on any template but our own, so things may not be perfect.

*The FalixNodes Help Center was built thanks to Korbs Studio*
