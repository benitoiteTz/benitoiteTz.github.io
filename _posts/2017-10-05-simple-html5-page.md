---
layout: post
title: Simple Html5 Page
---

### What is HTML?
the acrnym HTML stands for Hypertext Markup Language, the authorizing language used to create pages on the world wide web(www). HTML is a set of codes or HTML tags that provide a web browser with directions on how to structure a web page's information and features.
  
### Write HTML5 Using Notepad or TextEdit
 Web pages can be created and modified by using professional HTML5 Editors. However for learning HTML5 we recommend a simple text editor like Notepad(PC) or TextEdit(Mac). We believe using a simple text editor is a good way to learn HTML5. 
 
 Follow four steps below to create your first web page with Notepad or TextEdit
 
### Step 1&#58; Open NotePad(PC)
 **Windows 8 or later&#58;**
 
 Open Start Screen (the window symbol at the bottom left on your screen). Type **Notepad**.
 
 **Windows 7 or Earlier&#58;**
 
 Open **Start** > **Programs** > **Accessories** > **Notepad**
 
### Step 1&#58; Open NotePad(Mac)
Open **Finder** > **Applications** > **TextEdit**

Also Change some preferences to get the application save files correctly. In **Preferences** > **Format** choose **"Plain Text"** , then under "Open and Save", Check the box that says "Ignore rich text commands in HTML files". **Then open a new document to place the code**

### Step 2&#58; Write Some Html
Write or Copy some HTML into NotePad.

{% highlight html %}
<!DOCTYPE html>

<html>

<body>

<h1>My First Heading</h1>

<p>My first paragraph.</p>

</body>

</html>

{% endhighlight %}

![]({{ "/images/notepad-web.png" }})

### Step 3&#58; Save The HTML5 Page
Save the file on your computer. Select **File**  > **Save As** in the Notepad menu.
Name the file **index.html** and set the encoding to **UTF-8** (which is the prefered encoding for HTML5 files).

![]({{ "/images/notepad-save.png" }})

**You can either use .htm or .html as file extension. There is no difference, it is up to you**

### Step 4&#58; View the HTML5 Page in Your Browser
Open the saved HTML file in your favorite browser (double click on the file, or right-click - and choose "Open with").

The result will look much like this&#58;

![]({{ "/images/browser-view.png" }})

The purpose of the web browser (Chrome,IE,FireFox,Safari) is to read HTML5 documents and display them.

The browser does not display the HTML5 tags, but uses them to determine to display the document

### Explaining Some HTML5 Writen&#58;
{% highlight html %}
1. The <!DOCTYPE html> declaration defines this document to be HTML5
2. The <html> element is the root element of an HTML5 page 
3. The <body> element contains the visible page content
4. The <h1> element defines the large heading 
5. The <p> element defines a paragraph
{% endhighlight %}

#### HTML5 tags
HTML5 tags are element names surrounded by angle brackets&#58;

{% highlight html %}
<tagname> content goes here ... </tagname>
{% endhighlight %}
* HTML5 tags normally come **in pairs** like <p> and </p>
* The first tag in pair is the **start tag** the second tag is **end tag**
* The end tag is written like the start tag, but with a **forward slash** inserted before the tag name
