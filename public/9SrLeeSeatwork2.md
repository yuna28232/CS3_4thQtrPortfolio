# Seatwork #2 - Getting to know CSS Position and z-index.
### This seatwork will ask you to implement the different CSS position on a given code.
### short link to this .md file is: https://bit.ly/4c61P9K
#### Resources (also found in Khub week 5)
- [4 Minute Youtube Video on CSS Position](https://www.youtube.com/watch?v=YEmdHbQBCSQ)
- [CSS Position Tutorial](https://roycan.github.io/CssPositioningZIndexLab/)

### Instructions: 
1. This is individual submission in khub, but you can work with a partner.  When you submit in khub please place both your names in the submission bin.
2. Guided Activity (30 minutes), please follow what is being required.  

    - Make a copy of this .md file to your Q4 repository and name it as **SectionLNseatwork2.md** example **9LiCruzSeatwork2.md**. Place it in your q4 repository vscode local computer. Committing frequently to your Github repository.  
    - Copy the code below and paste it inside a new file (name it as SectionLNseatwork2.html). Place this file in the same location where the .md file is saved. 
    - Change the content values of the meta tags to your names for author/s and the date today for revised.
    - Please do the following tasks that will ask you to reposition HTML elements then answer the guided question for each task on the .md file. Commit changes to the .md file and to the .html file as well.
    **- This seatwork is worth 20pts and should be submitted by the end of the period** The link to [KHub submission bin](https://khub.mc.pshs.edu.ph/mod/assign/view.php?id=15481).
      - Submit the links to your .md file and .html file.

```html
<!DOCTYPE html>
<html>
<head>
  <meta name="author" content="<Yuna Lee/Kleo Foronda>" />
  <meta name="revised" content="<04/05>" />
  <style>
    body { font-family: Arial, sans-serif; }
    .header, .footer {
      background: lightblue;
      padding: 10px;
    }
    .footer {
       opacity: 0.5;
    }
    .sidebar {
      background: lightgreen;
      width: 150px;
      height: 200px;
    }
    .content {
      background: lightyellow;
      width: 300px;
      height: 200px;
    }    
  </style>
</head>
<body>
  <div class="header">Header</div>
  <div class="sidebar">Sidebar</div>
  <div class="content">Main Content</div>
  <div class="footer">Footer</div>
</body>
</html>
```
### Step 1 (Static vs Relative):

- Add in css ```position: relative; top: 20px; left: 20px;``` to .sidebar.

- Guided Question: What changed compared to the default static positioning? Try to give different values to top and left or you can change it to bottom, right.
- The sidebar moves away from the top/left as the value increases. From the css, it is relative 20px away from the top and 20px away from the left.

### Step 2 (Fixed):

- Add in css ```position: fixed; bottom: 0; width: 100%;``` to .footer.

- Guided Question: What happens when you scroll the page? Why does the footer behave differently from position relative?
- The footer stays fixed at the bottom because it is relative to the viewport of the screen unlike position relative which is relative to the page layout.

### Step 3 (Absolute):

- Add in css ```position: absolute; top: 66px; left: 200px;``` to .content.

- Guided Question: What is the effect of position: absolute on an element? How is it different from fixed?
- When scrolling through the page, the fixed element will go with it. For example, if the fixed element is at the middle of the screen, and the user scrolls throught the website, the fixed element will stay in the middle. However, if we try the same thing with absolute, it actually goes out of the screen because its position is relative to the page  .  

### Step 4 : (Absolute)

- Add in html ```<div class="notice">Notice!</div>``` and include the css below:

```css
.notice {
    position: absolute;
    top: 60px;
    left: 400px;
    background: orange;
    padding: 10px;
    z-index: 2;
}
```

- Give .content a z-index: 1.

- Guided Question: Why does the notice appear on top of the content? What happens if you swap the z‑index values? 
-It is because notice has a higher z index value. When we switch the z value of the 2, then theyre order will also swap.  

- Challenge: 
    * What changes that you have to do on the code that will position .notice box on the top right corner of the .content box? Please write the code on paper as well (both html and css on the part of .notice and .content).
    * Try to change the position of .content to relative then to fixed. What do you observed each time?
    - Scrolling with a relative, goes with the screen while scrolling with a fixed, stays stuck to the position it is set to.
    * What do you observe on about the effect of z-index on .notice and .content boxes?
    - The z index allows stacking. The one with the higher z index will be the one whose on top.

3. Please answer the following reflection questions (15 minutes)

    a. Could you summarize the differences between the CSS position values (static, relative, absolute, fixed)? 
    -Static : follows normal page flow
    -Relative : moves the element without affecting others
    -Absolute : relative to the nearest "positioned parents"
    -Fixed : relative to the browser

    b. How does absolute positioning depend on its parent element?
    -Its relative to its parent so if the parent is on the bottom left and the child element is top: 0 it would be on top of the parent element. If there is no parent, it will become relative to the <body>.

    c. How do you differentiate sticky from fixed (you can research on sticky)?
    - Sticky is a relative element but it will only act like one if its parent container is on teh screen. 

    d. If you were designing a webpage for a school event, how might you use positioning to highlight important information? Please give concrete examples.
    We could use fixed for a header that includes the navigation buttons to make the webpage more accessible.