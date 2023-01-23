# Kindle EPUB Fix

Amazon Send-to-Kindle service has accepted EPUB, however, for historical reason
it still assumes ISO-8859-1 encoding if no encoding is specified. This creates weird formatting errors for special characters.

This tool will try to fix your EPUB by adding the UTF-8 specification to your EPUB. It currently does
not fix other errors.

You can access this tools at https://kindle-epub-fix.netlify.app

**Warning:** This tool come at no warranty. Please still keep your original EPUB.
We don't guarantee the resulting file will be valid EPUB file, but it should.

# Version History
- **1.3 - Jan 4, 2023**
	- Batch processing
	- Language detection is now case-insensitive
	- XML encoding regex is more forgiving
- **1.2 - September 13, 2022**
	- Detect invalid language tag and prompt user for new language.
	- Detect stray image tags and remove them.
	- Fix bug in body ID tag replacement.
- **1.1.1 - September 10, 2022**
	- User experience improvements.
	- Add prefix to filenames of EPUBs that were fixed.
- **1.1 - August 24, 2022**
	- Restructure the code to be able to handle other error types.
	- Fix cannot detect existing encoding declaration if the declaration is using single quote.
	- Add new fix for invalid hyperlink to body tag with ID.
	- Also show the list of what has been fixed.
- **1.0.1 - August 14, 2022**
	- Fix CRC problem in generated EPUB file caused by ZIP library.
- **1.0 - July 14, 2022**
	- Initial release.