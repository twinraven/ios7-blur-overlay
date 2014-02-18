iOS7 Blur Overlay
=================

One way of recreating the iOS7-style blurred overlay, using CSS.

![iOS7-style blurred overlay panels][https://raw2.github.com/twinraven/ios7-blur-overlay/master/img/screenshot.jpg]

## Notes

* The main 'trick' here is to use `background-attachment: fixed;` for the background on the list items. This fixes the background's position to the top-level containing element
* The blur is actually a second image, with a photoshop blur filter applied. This could applied as a CSS filter, but a) this would lower the browser support for the effect (~44% as of 02/14) and b) require schenanegans with pseudo elements
* `background-size: cover;` is used on both the body tag and list items

## Limitations

* You can't force hardware acceleration on the list items: it locks the background position, ruining the effect
* Transitions aren't possible, as this enables hardware acceleration (see above).