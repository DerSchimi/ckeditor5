# CKEditor 5 Example

This package contains a complete working example of CKEditor 5 built from the repository source code.

## Contents

- `index.html` - Main example file demonstrating CKEditor 5 functionality
- `dist/` - Contains the bundled CKEditor 5 files
  - `browser/ckeditor5.umd.js` - UMD build of CKEditor 5 (main bundle)
  - `browser/ckeditor5.css` - Complete CSS styles for the editor
  - `ckeditor5.js` - ESM build of CKEditor 5 (alternative)
  - `ckeditor5.css` - CSS styles (alternative)
  - Additional CSS files for specific use cases
  - `translations/` - UI translations for different languages

## How to Use

1. **Extract the files** to your web server directory
2. **Start a local web server** (required for security reasons)
   - Using Python: `python -m http.server 8080`
   - Using Node.js: `npx http-server -p 8080`
   - Using PHP: `php -S localhost:8080`
3. **Open your browser** and navigate to `http://localhost:8080`

## Features Demonstrated

The example includes:

- ✅ Rich text editing with formatting options
- ✅ Headings and paragraph styles
- ✅ Bold, italic, underline, strikethrough
- ✅ Font family and size selection
- ✅ Text and background colors
- ✅ Bulleted and numbered lists
- ✅ Links and link editing
- ✅ Tables with full editing capabilities
- ✅ Block quotes
- ✅ Code blocks
- ✅ Image insertion and editing
- ✅ Text alignment
- ✅ Undo/redo functionality
- ✅ Source editing mode
- ✅ Interactive buttons to test editor API

## License

This build uses CKEditor 5 with GPL license. For commercial use, please visit [CKEditor.com](https://ckeditor.com) to obtain a commercial license.

## Version

Built from CKEditor 5 v46.0.0

## Support

For questions and support, please refer to the [CKEditor 5 documentation](https://ckeditor.com/docs/ckeditor5/) or [GitHub repository](https://github.com/ckeditor/ckeditor5).