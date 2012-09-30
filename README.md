# Justification

In the deep dark days of web development, long before Google and Facebook had dropped IE6 support (but not quite as old as Netscape), said browser sported terrible, awful support for alphatransparent PNG images and many workarounds were developed. AutoPNG is mine. It uses a combination of CSS [expressions](http://msdn.microsoft.com/en-us/library/ms537634.aspx) and [DirectX filters](http://msdn.microsoft.com/en-us/library/ie/hh801215.aspx), both IE-specific CSS extensions, to automatically display alphatransparent PNG background images properly, providing the background image is not positioned or resized in any way. The major advantage over other methods is its nature of having been implemented as IE6-specific CSS rules, meaning easy integration with other IE6 compatibility rules, and easy selection of the elements to which it should be applied. It is worth noting that due to its reliance on CSS expressions, it does not function when JavaScript is disabled.

# Components

AutoPNG is comprised of two different CSS rules: one for `<img>` tags, and one for background images. Either or both can be applied as desired, as they are implemented independently. It is worth noting that the rule for background images has recieved more love.

# Use

1. Get `autopng.css`.
2. Either inline it with, or load it in addition to, your other IE compatibility rules. IE6 only, please; it may work with IE5, but it's never been tested, and PNGs work properly in IE7 in the first place.
3. Modify the rule selectors as appropriate.
    * The selector for images should be correct in the first place.
    * In practice, I tend not to use the `autopng` class to indicate background image replacement; rather, I individually select elements requiring love.

Please see `demos/img.html` and `demos/background.html` for examples.

# License

This work is licensed under a [Creative Commons Attribution-ShareAlike 3.0 Unported License](http://creativecommons.org/licenses/by-sa/3.0/).