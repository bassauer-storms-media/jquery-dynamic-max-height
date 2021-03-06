Dynamic max height plugin for jQuery - MOD
========================================

  - Now allows reinit of the plugin (by recalling it)

Original
-----------
[DEMO](http://joanclaret.github.io/jquery-dynamic-max-height)

How to use?
-----------

### Javascript
Include the ```jquery.dynamicmaxheight.min.js``` before your ```</body>``` tag and initialise it:

```html
 <script src="path/to/file/jquery.dynamicmaxheight.min"></script>
 <script>
    $('.dynamic-max-height').dynamicMaxHeight();
 </script>
```


### HTML
The plugin depends on the following HTML structure:

```html
<div class="js-dynamic-height" data-maxheight="70">
    <div class="dynamic-height-wrap">
      <p> My life fades. The vision dims. All that remains are memories. I remember a time of chaos... ruined dreams... this wasted land. But most of all, I remember The Road Warrior. The man we called "Max." To understand who he was, you have to go back to another time... when the world was powered by the black fuel... and the desert sprouted great cities of pipe and steel. Gone now... swept away. For reasons long forgotten, two mighty warrior tribes went to war, and touched off a blaze which engulfed them all. Without fuel they were nothing. They'd built a house of straw. The thundering machines sputtered and stopped. Their leaders talked and talked and talked. But nothing could stem the avalanche. Their world crumbled. </p>
    </div>
    <button class="js-dynamic-show-hide button" title="Show more" data-replace-text="Show less">Show more</button>
</div>
```

### CSS
Minimal CSS Rules for the plugin:

```css
.dynamic-height-wrap {
  overflow: hidden;
  position: relative;
  transition: max-height 0.25s ease-in-out;
  width: 100%;
}

/* Bottom gradient (optional, but recommended)*/
.dynamic-height-active .dynamic-height-wrap:before {
  background: linear-gradient(to bottom,  rgba(240,249,255,0) 0%,rgba(255,255,255,1) 100%);
  bottom: 0;
  content:'';
  height: 30px;
  left: 0;
  position: absolute;
  right: 0;
  z-index: 1;
}

.dynamic-height-active .dynamic-show-more {
  display: inline-block;
}

.dynamic-show-more {
  display: none;
}
```

### Options

| Value|Description|
| ------- |:---------------------|
| **data-maxheight** | Change "data-maxheight" in each item to set a different max height value |
| **data-replace-text** | Change "data-maxheight" in each button to set a custom "show less" message |

