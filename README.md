TextformatterMakeLinks for ProcessWire
======================================

This Textformatter module is just a wrapper around the method fHTML::makeLinks from flourishlib (http://flourishlib.com/api/fHTML#makeLinks)

The following description is basically just slightly modified copy from the official flourishlib documentation (http://flourishlib.com/docs/fHTML):

The Textformatter will parse through a string and create HTML links out of anything that resembles a URL or email address, as long as it is not already part of an <a> tag.

Here is an example of it in action:

If you put this text into a textarea inputfield which uses this textformatter

```PHP
Example 1: www.example.com.
Example 2: https://example.com.
Example 3: john@example.com.
Example 4: ftp://john:password@example.com.
Example 5: www.example.co.uk.
Example 6: john@example.co.uk.
Example 7: <a href="http://example.com">http://example.com</a>.
```

The output would be:

```HTML
Example 1: <a href="http://www.example.com">www.example.com</a>.
Example 2: <a href="https://example.com">https://example.com</a>.
Example 3: <a href="mailto:john@example.com">john@example.com</a>.
Example 4: <a href="ftp://john:password@example.com">ftp://john:password@example.com</a>.
Example 5: <a href="http://www.example.co.uk">www.example.co.uk</a>.
Example 6: <a href="mailto:john@example.co.uk">john@example.co.uk</a>.
Example 7: <a href="http://example.com">http://example.com</a>.
```
