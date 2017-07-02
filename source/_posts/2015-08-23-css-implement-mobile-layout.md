title: Use CSS to implement the mobile navigation layout
date: 2015-08-23 17:01:18
tags: [css,mobile]
---

### Requirement

When doing development for HTML which can adapt to mobile/pad, we need to have a way to let user access the web content easily, below is one of the most common UX design:

1. There is a menu icon to open the navigation menu
2. When click on the navigation menu item, the corresponding panel page will be loaded

### Implementation

* HTML

	It's very comprehensive, _i_ is the menu icon, _navigator_ is the navigation bar, _panel_ is the content page

	``` html
<body>

  <i class="menu fa fa-bars"></i>

  <div class="navigator">
    <ul>
      <li>
        <a href="#panel_1">Panel 1</a>
      </li>
      <li>
        <a href="#panel_2">Panel 2</a>
      </li>
      <li>
        <a href="#panel_3">Panel 3</a>
      </li>
    </ul>
  </div>

  <div class="container">

    <div class="panel" id="panel_1">
      <h1>This is Panel 1</h1>
    </div>

    <div class="panel" id="panel_2">
      <h1>This is Panel 2</h1>
    </div>

    <div class="panel" id="panel_3">
      <h1>This is Panel 3</h1>
    </div>
  </div>

</body>

	```

* CSS

	``` css
* {
  margin: 0;
  padding: 0;
}

.menu {
  display: block;
  position: absolute;
  top: 40px;
  right: 20px;
}

.showNavigator .navigator {
  left: 0px;
}

.navigator {
  position: absolute;
  width: 150px;
  left: -150px;
  background: lightgrey;
  z-index: 100;
  transition: all .5s ease;
}

.navigator li {
  line-height: 30px;
  padding: 3px 10px;
  border-top: solid 1px;
  text-align: center;
}

.navigator li:first-child {
  border-top: none;
}

.navigator li:hover {
  background: lightblue;
}

.navigator ul a {
  text-decoration: none;
}

.container {
  width: 100%;
  left: 0px;
  position: relative;
  transition: all .5s ease;
}

.container .panel {
  position: absolute;
  background: lightblue;
  width: 100%;
  left: -100%;
  transition: all .5s ease;
}

.container .panel:target {
  left: 0px;
}		
	```

* JS

	``` javascript
$(document).ready(function() {
  
  $('.menu').bind('click', function () {
    $('body').toggleClass('showNavigator');  
  });
  
  $('.navigator a').bind('click', function () {
    $('body').toggleClass('showNavigator');  
  })
  
});
	```
### Demo

[Plunker demo](http://embed.plnkr.co/3ff8RgZ6LWZAE4Ktl3V4/preview)
