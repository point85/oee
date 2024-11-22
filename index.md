---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Point85 Rev. 14
---

<h1>GeeksforGeeks</h1>
<h2>GeeksforGeeks</h2>
<h3>GeeksforGeeks</h3>
<h4>GeeksforGeeks</h4>
<h5>GeeksforGeeks</h5>
<h6>GeeksforGeeks</h6>

# PDF Reference Example

<a href="https://github.com/point85/OEE-Designer/blob/master/docs/Point85 OEE Getting Started Guide.pdf" target="_blank">Download Getting Started Guide</a>

<a href="resources/files/Santa Margarita.zip">Download Santa Margarita</a>

# My Images

<img src="resources/images/FactoryEquipment.jpg" alt="Image" style="width:25%;">

# Font Size Example

<p style="font-size: 20px;">This is a paragraph with a larger font size.</p>

<span style="font-size: 14px;">This is a smaller text.</span>

## With Div

<div style="font-size: 20px;">
  This text is larger.
</div>

<div style="font-size: 14px;">
  This text is smaller.
</div>

# Table with Different Font Sizes

<table>
  <tr>
    <th>Item</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><span style="font-size: 20px;">Large Text</span></td>
    <td>This text is larger.</td>
  </tr>
  <tr>
    <td><span style="font-size: 14px;">Small Text</span></td>
    <td>This text is smaller.</td>
  </tr>
  <tr>
    <td><span style="font-size: 16px;">Medium Text</span></td>
    <td>This text is medium-sized.</td>
  </tr>
</table>



# Image Gallery

| System |  |
|-------|-------------|
| ![Image 1](resources/images/FactoryEquipment.jpg) | **Overall Equipment Effectiveness** <br> Overall Equipment Effectiveness (OEE) is a key performance indicator for quantifying the utilization of manufacturing equipment. OEE is the product of availability, performance rate and quality rate for materials produced by that equipment. For more information, see the Introduction.|
| ![Image 2](https://www.markdownguide.org/resources/images/tux.png) | Description for Image 2 |

<p style="font-size: 20px;">Overall Equipment Effectiveness</p> 
![Image 3](https://www.markdownguide.org/resources/images/tux.png) Overall Equipment Effectiveness (OEE) is a key performance indicator for quantifying the utilization of manufacturing equipment. OEE is the product of availability, performance rate and quality rate for materials produced by that equipment. For more information, see the Introduction.|

---

# Image with Text Overlay

<div style="position: relative; text-align: center; color: black;">
  <img src="resources/images/clouds4-cropped.jpg" alt="cloud image" style="width:100%; height: 60px;">
  <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%);">
    <h1>Point85</h1>
  </div>
</div>


# Dropdown Menu Example

<div class="dropdown">
  <button class="dropbtn">Menu</button>
  <div class="dropdown-content">
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
    <a href="blog.html">Blog</a>
    <a href="contact.html">Contact</a>
  </div>
</div>

<style>
  .dropdown {
    position: relative;
    display: inline-block;
  }

  .dropbtn {
    background-color: #4CAF50;
    color: white;
    padding: 16px;
    font-size: 16px;
    border: none;
    cursor: pointer;
  }

  .dropdown-content {
    display: none;
    position: absolute;
    background-color: #f9f9f9;
    min-width: 160px;
    box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
    z-index: 1;
  }

  .dropdown-content a {
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
  }

  .dropdown-content a:hover {
    background-color: #f1f1f1;
  }

  .dropdown:hover .dropdown-content {
    display: block;
  }

  .dropdown:hover .dropbtn {
    background-color: #3e8e41;
  }
</style>


