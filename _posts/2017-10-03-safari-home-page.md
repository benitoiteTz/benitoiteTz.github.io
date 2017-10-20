---
layout: post
title: Safari Home Page
---

### Safari Home Page
The following video below shows how the homepage will look like at the end of this tutorial


<iframe width="420" height="315"
src="https://www.youtube.com/embed/ey4GCm3OyKE?playlist=PLpmkUSCWRiIWHG6Z8YPkBgXcnNxE6udcX&loop=1">
</iframe>


#### Creating the Header section
Header is the top part, that contains navigation links for the site
in crating the header section we will reuse the simple page template
we crated eariler.
    
{% highlight html %}
<!DOCTYPE html>
<html>
<body>
<header>
    <div>
        <h1>Safari</h1>
        <p>Explore the beauty of Tanzania</p>
    </div>
    <nav>
        <ul>
            <li><a href="index.html">home</a></li>
            <li><a href="nation_parks.html">nation parks</a></li>
            <li><a href="game_reserve.html">game reserve</a></li>
        </ul>
    </nav>
</header>
</body>
</html>
{% endhighlight %}

##### Explaining Some HTML5 Writen&#58;
{% highlight html %}
1. The <header> tag represents a container for introductory
  content or a set of navigational links
2. The <div> tags defines a division or a section in an
  HTML document
3. The <ul>  together with <li> tags are used to create
  unordered (bulleted) list
4. The <a> tag defines a hyperlink, which is used to link
 from one page to another.
 The most important attribute of the <a> tag is the href attribute,
 which indicates the links' destination
{% endhighlight %}

##### The Output&#58;

![]({{ "/images/plain-header.png" }})

This is how the header will look like now.

##### Adding CSS3 to Our html file to make It look beautiful
CSS describes how HTML5 elements are to be displayed on screen, html was create to describe
the content a web page and css comes to make the content look beautiful

##### How CSS3 Works on HTML5
a. CSS3 Syntax
CSS3 styles HTML tags by using css rule-sets. A CSS3 rule-set consists of a selector
and a declaration block

![]({{ "/images/css-rule-set.png" }})

The selector points to the HTML5 tag you want to style.

The declaration contains one or more declarations separated by semicolons.

Each declaration includes a CSS3 property name and value, separated by colon

A CSS3 declaration always ends with a semicolon, and declaration blocks are surrounded by curly braces.


##### Understanding CSS3 Selector
CSS selectors are used to "find" (or select) HTML elements based on their element name, id, class, attribute, and more.

###### 1. The element(tag) Selector
The element selector selects elements based on the element name.

You can select all <p> elements on a page like this (in this case, all <p> elements will be center-aligned, with a red text color)&#58;

{% highlight css %}
p {
    text-align: center;
    color: red;
}
{% endhighlight %}


###### 2. The id Selector
The id selector uses the id attribute of an HTML element to select a specific element.

The id of an element should be unique within a page, so the id selector is used to select one unique element!

To select an element with a specific id, write a hash (#) character, followed by the id of the element.

The style rule below will be applied to the HTML element with id="para1"&#58;

{% highlight css %}
#para1 {
    text-align: center;
    color: red;
}
{% endhighlight %}

###### 3. The class Selector
The class selector selects elements with a specific class attribute.

To select elements with a specific class, write a period (.) character, followed by the name of the class.

In the example below, all HTML elements with class="center" will be red and center-aligned&#58;

{% highlight css %}
.center {
    text-align: center;
    color: red;
}
{% endhighlight %}


###### 4. Grouping Selectors
If you have elements with the same style definitions,It will be better to group the selectors, to minimize the code.

To group selectors, separate each selector with a comma.

In the example below we have grouped the selectors&#58;

{% highlight css %}
h1, h2, p {
    text-align: center;
    color: red;
}
{% endhighlight %}

#### Let finish up our header
Continue with code we wrote in creating header section, we are going to embed css within
the same file to style our header


{% highlight html %}
<!DOCTYPE html>
<html>
<head>
    <style>

        body {
            margin: 0;
            font-family: "Times New Roman", Times, serif;
            overflow-x: hidden;
        }

        .safari{
            background-color: black;
            color: white;
            position: relative;
            height: 90px;
        }
        #logo-words{
            color: #F39C12;
            padding-left: 30px;
        }
        header, nav {
            display: block;
        }

        html,body,div, h1, p, ul, li, nav {
            margin: 0;
            padding: 0;
            border: 0;
            vertical-align: baseline;
        }

        /*navbar*/
        #nav ul li {
            float: left;
            display: inline-block;
            text-transform: capitalize;
            padding-top: 40px;
        }

        #nav {
            position: absolute;
            right: 0;
            top: 0;
        }

        #nav ul li a, #nav ul li span {
            -moz-transition: background-color .25s ease-in-out;
            -webkit-transition: background-color .25s ease-in-out;
            -ms-transition: background-color .25s ease-in-out;
            transition: background-color .25s ease-in-out;
            font-weight: 800;
            letter-spacing: 0.025em;
            color: #fff;
            text-decoration: none;
            padding: 0.5em 1em 0.5em 1em;
        }

        #nav ul li > ul {
            display: none;
        }

        #nav ul li:hover a, #nav ul li:hover span {
            background: #F8C471;
        }

        #nav ul li a.active {
            color: #F39C12;
        }

    </style>

</head>
<body>
<header class="safari">
    <div class="logo-safari">
        <h1>Safari</h1>
        <p id="logo-words">Explore the beauty of Tanzania</p>
    </div>
    <div>
    </div>
    <nav id="nav">
        <ul>
            <li id="current"><a class="active" href="index.html">home</a></li>
            <li><a href="nation_parks.html">nation parks</a></li>
            <li><a href="game_reserve.html">game reserve</a></li>
        </ul>
    </nav>
</header>
</body>
</html>
{% endhighlight %}


##### The Output&#58;

![]({{ "/images/final-header.png" }})

This is how the header will look like finally.


#### Creating the Contents Section

The content section is the part that contains all the important content we want to show to the people

Below the HTML5 we wrote for the header lets add some HTML5 for displaying our contents

{% highlight html %}
<!DOCTYPE html>
<html>
<head>
    <style>

        body {
            margin: 0;
            font-family: "Times New Roman", Times, serif;
            overflow-x: hidden;
        }

        .safari{
            background-color: black;
            color: white;
            position: relative;
            height: 90px;
        }
        #logo-words{
            color: #F39C12;
            padding-left: 30px;
        }
        header, nav {
            display: block;
        }

        html,body,div, h1, p, ul, li, nav {
            margin: 0;
            padding: 0;
            border: 0;
            vertical-align: baseline;
        }

        #nav ul li {
            float: left;
            display: inline-block;
            text-transform: capitalize;
            padding-top: 40px;
        }

        #nav {
            position: absolute;
            right: 0;
            top: 0;
        }

        #nav ul li a, #nav ul li span {
            -moz-transition: background-color .25s ease-in-out;
            -webkit-transition: background-color .25s ease-in-out;
            -ms-transition: background-color .25s ease-in-out;
            transition: background-color .25s ease-in-out;
            font-weight: 800;
            letter-spacing: 0.025em;
            color: #fff;
            text-decoration: none;
            padding: 0.5em 1em 0.5em 1em;
        }

        #nav ul li > ul {
            display: none;
        }

        #nav ul li:hover a, #nav ul li:hover span {
            background: #F8C471;
        }

        #nav ul li a.active {
            color: #F39C12;
        }

    </style>

</head>
<body>
<header class="safari">
    <div class="logo-safari">
        <h1>Safari</h1>
        <p id="logo-words">Explore the beauty of Tanzania</p>
    </div>
    <div>
    </div>
    <nav id="nav">
        <ul>
            <li id="current"><a class="active" href="index.html">home</a></li>
            <li><a href="nation_parks.html">nation parks</a></li>
            <li><a href="game_reserve.html">game reserve</a></li>
        </ul>
    </nav>
</header>
<section>
    <div>
        <div>
            <img src="images/safari-zoo.jpg" width="1100" height="550">
        </div>
    </div>
</section>
<div>
    <div>
        <aside>
            <h2>Welcome to our site let's begin our safari</h2>
            <hr>
            <p>A safari is a journey. This is the meaning of the word in Swahili, the language of East Africa. Your
                journey into Africa starts with Tanzania-Experience. When you join us on safari you will be met at the
                airport, taken to a hotel or a central meeting point and briefed before you set off. You will be
                transported in a well-maintained, clean Toyota 4×4 safari vehicle, driven by a professional local guide
                in areas that will leave you breathless with wonder and excitement. You will search for the ‘Big Five’ –
                buffalo, elephant, leopard, lion and rhino – and will be amazed by the sheer beauty of grass-covered
                savannas, extinct volcanoes and rare birds. You will see animals, landscapes and flowers and you will
                meet the local people and taste local food.</p>
            <h3>Adventure camping safari</h3>
            <p>On our adventure camping safaris you will be immersed in the East African wilderness. You will travel on
                rough adventurous roads, pass tiny rural settlements and see fascinating landscapes and abundant
                wildlife. All your senses will be involved; from smelling early morning coffee, experiencing the thrill
                of a kill to the chill of a morning game drive. Falling asleep to the hooting of an owl or waking up
                with the roaring of a lion is what you will experience. The safari experience is all the more intense as
                you are ‘right in the middle’ of it all. The nearness to the nature, especially at night with its
                nocturnal sounds, compensates for the luxury of a lodge. Our camping safaris in Tanzania offer all of
                this and are therefore perfect for nature lovers and those who are looking for a break from civilisation
                and its comforts. Camping is to experience East Africa’s nature, animals and cultures in an affordable
                way.</p>
        </aside>
        <section>
            <article>
                <header>
                    <h2>Most visited</h2>
                </header>
                <aside>
                    <div><img src="images/giraf.jpg" alt=""/></div>
                    <div><img src="images/zebra.jpg" alt=""/></div>
                    <div><img src="images/g2.jpg" alt=""/></div>
                    <div><img src="images/twiga.jpg" alt=""/></div>
                </aside>
                <section>
                    <h5>Serengeti</h5>
                    <p>Serengeti has come to symbolize paradise to many of us.Meet the Maasai, who had grazed their
                        cattle on the vast grassy plains.</p>
                    <h5>Ngorongoro</h5>
                    <p>The jewel in Ngorongoro's crown is a deep, volcanic crater, the largest un flooded and unbroken
                        caldera in the world. The Ngorongoro Crater is a breathtaking natural wonder.</p>
                    <h5>Manyara</h5>
                    <p>Located beneath the cliffs of the Manyara Escarpment, on the edge of the Rift Valley, Lake
                        Manyara National Park offers varied ecosystems, incredible bird life, and awesome views.</p>
                    <h5>Mikumi</h5>
                    <p>Located between the Uluguru Mountains and the Lumango range, the park has a wide variety of
                        wildlife that can be easy spotted and also well acclimatized to game viewing.</p>
                </section>
            </article>
        </section>
    </div>
</div>
</body>
</html>
{% endhighlight %}

### Explaining Some HTML5 Writen&#58;
{% highlight html %}
1. The <section> tag defines sections in a document, such as chapters,
 headers, footers, or any other sections of the document.
2. The <article> tag specifies independent, self-contained content.
   An article should make sense on its own and it should be possible 
   to distribute it independently from the rest of the site. 
3. The <aside> tag defines some content aside from the content it is placed in.
   The aside content should be related to the surrounding content.
4. The <img> tag defines an image in an HTML page.
   The <img> tag has two required attributes: src and alt. 
{% endhighlight %}


##### The Output&#58;

<iframe width="420" height="315"
src="https://www.youtube.com/embed/Lj-nMBXnnDY?playlist=PLpmkUSCWRiIWHG6Z8YPkBgXcnNxE6udcX&loop=1">
</iframe>

This is how the our home page looks like now.

##### Adding CSS3 to Our html file to make It look beautiful

{% highlight html %}
<!DOCTYPE html>
<html>
<head>
    <style>

body {
    margin: 0;
    font-family: "Times New Roman", Times, serif;
    overflow-x: hidden;
}

html, body, div, span, h1, h2, h3, h4, h5, h6, p, a, ul, li, article, aside, footer, header, menu, nav {
    margin: 0;
    padding: 0;
    border: 0;
    vertical-align: baseline;
}

article, aside, footer, header, nav, section {
    display: block;
}

/*css for header*/

.safari {
    background-color: black;
    color: white;
    position: relative;
    height: 90px;
}

.logo-safari {
    margin-left: 15px;
}

.logo-safari h1 {
    color: #fff;
    font-weight: 500;
    font-size: 46px;
    padding: 10px 0 0 24px;
    letter-spacing: 0.05em;
    display: inline-block;
    vertical-align: middle;
}

#logo-words {
    color: #F39C12;
    padding-left: 30px;
}

/*navbar*/
#nav ul li {
    float: left;
    display: inline-block;
    text-transform: capitalize;
    padding-top: 40px;
}

#nav {
    position: absolute;
    right: 0;
    top: 0;
}

#nav ul li a, #nav ul li span {
    -moz-transition: background-color .25s ease-in-out;
    -webkit-transition: background-color .25s ease-in-out;
    -ms-transition: background-color .25s ease-in-out;
    transition: background-color .25s ease-in-out;
    font-weight: 800;
    letter-spacing: 0.025em;
    color: #fff;
    text-decoration: none;
    padding: 0.5em 1em 0.5em 1em;
}

#nav ul li > ul {
    display: none;
}

#nav ul li:hover a, #nav ul li:hover span {
    background: #F8C471;
}

#nav ul li a.active {
    color: #F39C12;
}

/*container section*/
section {
    margin-top: 20px;
}

section .container {
    min-width: 800px;
    background-color: #CCD1D1;
    margin-right: 55px;
    margin-left: 55px;
}

.container {
    min-width: 800px;
    margin-right: 55px;
    margin-left: 55px;
    margin-top: 30px;
}

.page-wrapper {
    margin-right: 15px;
    margin-left: 35px;
}

/*page-contantens*/

.page-contents {
    height: 520px;
}

.page-contents aside,
.page-contents section {
    height: 500px;
}

.page-contents aside {
    float: left;
    width: 760px;
}

.page-contents section {
    float: right;
    width: 360px;

}

hr {
    color: #F39C12;
    border: 0;
    border-top: solid 1px #F39C12;
    margin-left: 20px;
}

aside h2 {
    font-weight: 500;
    font-size: 43px;
    padding-left: 20px;
    color: #273746;
}

aside h3 {
    font-weight: 600;
    font-size: 18px;
    padding-top: 10PX;
    padding-left: 20px;
    color: #273746;
    line-height: 1.25em;
    font-family: cursive;
}

aside p {
    padding-left: 40px;
    padding-top: 15px;
    color: #34495E;
    font-family: cursive;
    opacity: 0.7;

}

section h2 {
    font: 14pt Helvetica, "Helvetica neue", Arial, sans-serif;
    font-weight: lighter;
    text-transform: uppercase;
    color: #493831;
    padding-bottom: 10px;
    margin: 0;
}

/*css for the most visited part*/
article header {
    height: 60px;
    background-color: grey;

}

header h2 {
    font-weight: 600;
    font-size: 24px;
    text-align: center;
    padding-top: 18px;
    color: white;
    text-transform: capitalize;
}

.visited {
    background-color: #FDEBD0;
    opacity: 0.7;
    width: 360px;
}

.info {
    margin: 0px 0 5px 0px;

}

.visited aside {
    float: left;
    width: 180px;
}

.visited section {
    float: right;
    width: 180px;
}

.info h5 {
    text-transform: capitalize;
    padding: 12px 0 0 0;
}

.info p {
    font-size: 12px;
}

/* Image */

.image {
    display: inline-block;
    outline: 0;
}

.image img {
    width: 78%;
    border-radius: 2px;
}

.image.fit {
    width: 80%;
    float: left;
    padding: 22px 0 7px 25px;
}

/*footer*/
footer {
    padding: 1em;
    color: white;
    background-color: black;
    clear: left;
    margin-top: 20px;
    text-align: center;
}

footer span {
    color: #F39C12;
}

    </style>

</head>
<body>
<header class="safari">
    <div class="logo-safari">
        <h1>Safari</h1>
        <p id="logo-words">Explore the beauty of Tanzania</p>
    </div>
    <div>
    </div>
    <nav id="nav">
        <ul>
            <li id="current"><a class="active" href="index.html">home</a></li>
            <li><a href="nation_parks.html">nation parks</a></li>
            <li><a href="game_reserve.html">game reserve</a></li>
        </ul>
    </nav>
</header>
<section>
    <div class="container">
        <div class="page-wrapper">
            <img src="images/safari-zoo.jpg" width="1100" height="550">
        </div>
    </div>
</section>
<div class="container">
    <div class="page-contents">
        <aside>
            <h2>Welcome to our site let's begin our safari</h2>
            <hr>
            <p>A safari is a journey. This is the meaning of the word in Swahili, the language of East Africa. Your
                journey into Africa starts with Tanzania-Experience. When you join us on safari you will be met at the
                airport, taken to a hotel or a central meeting point and briefed before you set off. You will be
                transported in a well-maintained, clean Toyota 4×4 safari vehicle, driven by a professional local guide
                in areas that will leave you breathless with wonder and excitement. You will search for the ‘Big Five’ –
                buffalo, elephant, leopard, lion and rhino – and will be amazed by the sheer beauty of grass-covered
                savannas, extinct volcanoes and rare birds. You will see animals, landscapes and flowers and you will
                meet the local people and taste local food.</p>

            <h3>Adventure camping safari</h3>
            <p>On our adventure camping safaris you will be immersed in the East African wilderness. You will travel on
                rough adventurous roads, pass tiny rural settlements and see fascinating landscapes and abundant
                wildlife. All your senses will be involved; from smelling early morning coffee, experiencing the thrill
                of a kill to the chill of a morning game drive. Falling asleep to the hooting of an owl or waking up
                with the roaring of a lion is what you will experience. The safari experience is all the more intense as
                you are ‘right in the middle’ of it all. The nearness to the nature, especially at night with its
                nocturnal sounds, compensates for the luxury of a lodge. Our camping safaris in Tanzania offer all of
                this and are therefore perfect for nature lovers and those who are looking for a break from civilisation
                and its comforts. Camping is to experience East Africa’s nature, animals and cultures in an affordable
                way.</p>
        </aside>
        <section class="visited">
            <article>
                <header>
                    <h2>Most visited</h2>
                </header>
                <aside>
                    <div class="image fit"><img src="images/giraf.jpg" alt=""/></div>
                    <div class="image fit"><img src="images/zebra.jpg" alt=""/></div>
                    <div class="image fit"><img src="images/g2.jpg" alt=""/></div>
                    <div class="image fit"><img src="images/twiga.jpg" alt=""/></div>
                </aside>
                <section class="info">
                    <h5>Serengeti</h5>
                    <p>Serengeti has come to symbolize paradise to many of us.Meet the Maasai, who had grazed their
                        cattle on the vast grassy plains.</p>
                    <h5>Ngorongoro</h5>
                    <p>The jewel in Ngorongoro's crown is a deep, volcanic crater, the largest un flooded and unbroken
                        caldera in the world. The Ngorongoro Crater is a breathtaking natural wonder.</p>
                    <h5>Manyara</h5>
                    <p>Located beneath the cliffs of the Manyara Escarpment, on the edge of the Rift Valley, Lake
                        Manyara National Park offers varied ecosystems, incredible bird life, and awesome views.</p>
                    <h5>Mikumi</h5>
                    <p>Located between the Uluguru Mountains and the Lumango range, the park has a wide variety of
                        wildlife that can be easy spotted and also well acclimatized to game viewing.</p>
                </section>
            </article>
        </section>
    </div>
</div>
</body>
</html>
{% endhighlight %}

##### The Output&#58;

<iframe width="420" height="315"
src="https://www.youtube.com/embed/-zErAgl7FUA?playlist=PLpmkUSCWRiIWHG6Z8YPkBgXcnNxE6udcX&loop=1">
</iframe>

This is how our home page looks like after adding contents