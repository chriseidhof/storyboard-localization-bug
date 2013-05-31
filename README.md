When having custom subclasses of UIViews (even empty ones) localisations don't get picked up.
===

Steps to reproduce

1. Create new Project based on Storyboards
1. Added a label with the text "Hello"
1. Enable Base localization, added Dutch as a second language
1. Made sure the StoryBoard got translated as a .strings file
1. Translated the text to "Hallo"
1. Set simulator to Dutch ("Nederlands") language
1. Everything works as expected (so far), label got translated
1. Create an (empty) subclass of UILabel named CBELabel
1. Changed the class of the label in the storyboard to CBELabel
1. No more translation.

See also: http://www.openradar.me/14021389
