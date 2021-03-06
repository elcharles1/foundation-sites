---
title: Responsive Embed
description: Wrap embedded content like videos, maps, and calendars in a responsive embed container to maintain the correct aspect ratio regardless of screen size.
sass: scss/components/_responsive-embed.scss
tags: flex video 'flex video'
video: GxUsloI_qnQ
---

To make sure embedded content maintains its aspect ratio as the width of the screen changes, wrap the `iframe`, `object`, `embed`, or `video` in a container with the `.responsive-embed` class.

<p>
  <a class="" data-open-video="0:56"><img src="{{root}}assets/img/icons/watch-video-icon.svg" class="video-icon" height="30" width="30" alt=""> Watch this part in video</a>
</p>

<div class="docs-codepen-container">
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/MmGEbb?editors=1100" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="edit on codepen button"></a>
</div>

```html_example
<div class="responsive-embed">
  <iframe width="420" height="315" src="https://www.youtube.com/embed/mM5_T-F1Yn4" frameborder="0" allowfullscreen></iframe>
</div>
```

---

## Aspect Ratios

Add ratio classes to change the aspect ratio of responsive embeds. The default ratio is 4:3. The `.widescreen` class will change the container's aspect ratio to 16:9.

<p>
  <a class="" data-open-video="2:17"><img src="{{root}}assets/img/icons/watch-video-icon.svg" class="video-icon" height="30" width="30" alt=""> Watch this part in video</a>
</p>

<div class="docs-codepen-container">
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/MmXxpO?editors=1100" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="edit on codepen button"></a>
</div>

```html_example
<div class="responsive-embed widescreen">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/WUgvvPRH7Oc" frameborder="0" allowfullscreen></iframe>
</div>
```

The ratio classes are generated by the keys in the `$responsive-embed-ratios` map in your settings file. Only the `default` key is required. You can, for example, make your default ratio 16:9, remove widescreen, and add other aspect ratios.

```scss
$responsive-embed-ratios: (
  default: 16 by 9,
  vertical: 9 by 16,
  panorama: 256 by 81,
  square: 1 by 1,
);
```

<p>
  <a class="" data-open-video="3:18"><img src="{{root}}assets/img/icons/watch-video-icon.svg" class="video-icon" height="30" width="30" alt=""> Watch this part in video</a>
</p>

<div class="docs-codepen-container">
  <a class="codepen-logo-link" href="https://codepen.io/IamManchanda/pen/OmEqgM?editors=1100" target="_blank"><img src="{{root}}assets/img/logos/edit-in-browser.svg" class="" height="" width="" alt="edit on codepen button"></a>
</div>

```html_example
<div class="responsive-embed panorama">
  <iframe width="1024" height="315" src="https://www.youtube.com/embed/bnD9I24EL_4" frameborder="0" allowfullscreen></iframe>
</div>
```
