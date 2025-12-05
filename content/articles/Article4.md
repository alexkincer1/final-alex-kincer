---
title: "Website Enhancement"
date: "2025-12-04"
description: ""
omit_header_text: true
featured_image: images/7b6b442822c8ba56fb6ff82f7bf04f1f.jpg
summary: "How I enhanced my Website Assignment for CSC 324 in the Fall of 2025."
type: page
weight: 2
---

## My Small Enhancement

The smaller enhancement I made to my website was when I was creating it was the effect of the titles of my Article posts and Blog posts to turn pink when the mouse hovers over it. 

## How To:

To make this enhancement, I add these lines of code to my custom.ss file in my static/css folder:

```
.blog-card-title a {
  color: #ff1493; /* default pink */
  text-decoration: none;
  transition: color 0.2s;
}

.blog-card-title a:hover {
  color: #ff69b4; /* brighter pink on hover */
}
```

The key points of this code for the enhancement is the numbers used to determine which colors/shades of pink are to be used in the hovering process. In addition, the "transtion: color 0.2s;" is put in place to make it a smooth change from the black color to pink. Finally, and most importantly, "a:hover" is used to indicate when the ".blog-card-title" is supposed to transition to the color given. This enhancement could easily be replicated in other websites using the basic ananke theme.

## My Major Enhancement

For this website, my major enhancement in the small navigation bar on the right hand side of the directory pages for the Blogs and Articles posts. 

## How To:

To begin this process, I headed to ChatGPT to get some assistance. If you are interested in how I approaches this goal, [here is my conversation](https://chatgpt.com/share/69326476-fed0-8002-98fe-def00be2bab4). 

I began with a side bar for Blogs, which lead me to create a "sidebar.html" file within my partials folder inside of my layouts folder. This is what the inside of this file looked like to achieve the navigation bar:

```
<div id="right-sidebar">
  <ul>
    <li><a class="sidebar-btn" href="/blog/Blog1/">REL341</a></li>
    <li><a class="sidebar-btn" href="/blog/Blog2/">PHI201</a></li>
    <li><a class="sidebar-btn" href="/blog/Filler1/">Blog 3</a></li>
    <li><a class="sidebar-btn" href="/blog/Filler2/">Blog 4</a></li>
    <li><a class="sidebar-btn" href="/blog/Filler3/">Blog 5</a></li>
  </ul>
</div>

<style>
#right-sidebar {
  position: fixed;
  right: 20px;
  top: 120px;
  width: 200px;
  background: #ffdee9; /* soft pink background */
  padding: 15px;
  border-radius: 10px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.15);
  z-index: 999;
}

#right-sidebar ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

#right-sidebar li {
  margin-bottom: 12px;
}

.sidebar-btn {
  display: block;
  padding: 10px 14px;
  background: #ff69b4; /* hot pink */
  color: white;
  text-decoration: none;
  border-radius: 6px;
  text-align: center;
  font-weight: bold;
  transition: 0.2s;
}

.sidebar-btn:hover {
  background: #ff1493; /* deeper pink */
}
</style>
```
When doing this, it was very important to accurately name each button I was wanting to be shown while also using the correct tracking of the files that I want the buttons to lead to. Another important factor was the coloring, size, and another "hover" action like mentioned in my smaller enhancement to make the buttons seem transitional and more interactive for the readers. 

Once my navigation bar was complete for my Blogs, I then wanted to do the same for my Articles page. I went through the same process of creating a new file within my partials folder inside my layouts folder titled "sidebar-articles.html". The inside of this file looked like this:

```
<div id="right-sidebar-articles">
  <ul>
    <li><a class="sidebar-btn" href="/articles/Article1/">SOC111</a></li>
    <li><a class="sidebar-btn" href="/articles/Article2/">KHS347</a></li>
    <li><a class="sidebar-btn" href="/articles/Article3/">AI Usage</a></li>
    <li><a class="sidebar-btn" href="/articles/Article4/">Website Enhancement</a></li>
  </ul>
</div>

<style>
#right-sidebar-articles {
  position: fixed;
  right: 20px;
  top: 120px;
  width: 200px;
  background: #ffdee9;
  padding: 15px;
  border-radius: 10px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.15);
  z-index: 999;
}

#right-sidebar-articles ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

#right-sidebar-articles li {
  margin-bottom: 12px;
}

.sidebar-btn {
  display: block;
  padding: 10px 14px;
  background: #ff69b4;
  color: white;
  text-decoration: none;
  border-radius: 6px;
  text-align: center;
  font-weight: bold;
  transition: 0.2s;
}

.sidebar-btn:hover {
  background: #ff1493;
}
</style>
```
This was a repeated process with little edits to make is specific to my articles page. 