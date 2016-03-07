# xs3p XSD documentation generator

This is a fork of version 1.1.5 of the xs3p doc tool from:

  http://xml.fiforms.org/xs3p/

See the [original README](README_ORIG.txt) for more information.

Added features include:

 - Complete re-design using [Bootstrap](https://getbootstrap.com "Bootstrap homepage").
 - Output of UTF-8 encoded files
 - Output of HTML5
 - Support [Markdown](https://daringfireball.net/projects/markdown/ "Markdown homepage")
   formatting in `<documentation>` elements.

The markdown support is implement with the [Pagedown
library](https://code.google.com/archive/p/pagedown/).

You can see a nice example result here:

 * http://bitfehler.net/xs3p/address_annotated.xsd.html

which is the result of [one of the examples](examples/address_annotation.xsd.)
that I added specifically to demonstrate the new features of this fork.

Another interesting example is the result for the XML Schema .xsd itself:

 * http://bitfehler.net/xs3p/XMLSchema.xsd.html

This one pushes the system to its limits, but it's still useful in my opinion.

### Known issues

 * There is currently no way to inline the Bootstrap and jQuery sources, thus
   those files must be fetched when viewing the documentation. Their URLs can
   be set, though, so you could serve them locally if offline viewing is a
   requirement.
 * While I even added some features (e.g. linking to the `source` attribute of
   the `<documentation>` element, if present), some feature that have
   previously may have gone missing. Quite some refactoring was involved and
   it is quite hard to test some of the more esoteric features of XSD.
 * There are some minor display issues, but as far as I can tell none of them
   impact the usability.
