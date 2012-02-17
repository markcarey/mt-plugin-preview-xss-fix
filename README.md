Preview XSS Fix for Movable Type
==========

This plugin fixes an issue introduced with Google Chrome v17 that causes admin entry previews to display a blank screen.

This seems to happen only when the entry contains img tags with fully qualified src URLs from the same domain as the MT install.  For some reason, Chrome now suspects this to be an XSS attack and will not render the iframe with he entry preview.

This plugin adds a response header that tells Chrome to skip its XSS checking for this request.  It only adds this for admin Entry Previews.
