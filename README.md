# Export Deck to HTML

Export your Anki decks to standalone HTML files with custom styling and formatting.

![Export to HTML Screenshot](https://raw.githubusercontent.com/gschaden/ExportToHtml/master/image.png)

## Description

This addon allows you to export Anki cards to a single HTML file with full control over the layout and styling. Based on the original "Export cards to Html" addon, this version has been updated with modern features and support for newer Anki versions.

## Features

### Core Functionality
- **Export entire decks** to standalone HTML files with embedded images
- **Custom HTML templates** - Full control over card layout and structure
- **Custom CSS styling** - Style your exported cards exactly how you want
- **Flexible queries** - Use Anki's search syntax to filter which cards to export
- **Image support** - Images are automatically embedded as base64 data

### New Features
- **✨ Live Preview** - See how your cards will look before exporting
- **Adjustable preview count** - Choose how many sample cards to preview (1-100)
- **Modern UI** - Split-panel interface with controls on the left and preview on the right
- **Full CSS support** - Preview uses modern web engine for accurate rendering
- **Updated for modern Anki** - Compatible with current Anki versions

## Installation

1. Download the addon from AnkiWeb
2. Open Anki and go to Tools → Add-ons → Get Add-ons
3. Enter the addon code or install from file
4. Restart Anki

## Usage

### Basic Export

1. Go to **Tools → Export deck to html** (or press **Ctrl+M**)
2. Select your deck from the dropdown
3. Customize the query if you want to filter specific cards
4. Modify the CSS and HTML template as needed
5. Click **Preview** to see how your cards will look
6. Click **Export** to save the HTML file

### Template System

The addon uses a simple template system with placeholders:

#### HTML Template
Use `{{fieldName}}` to insert card fields:
```html
<li>
  <div class="id">{{id}}</div>
  <div class="field0">{{Front}}</div>
  <div class="field1">{{Back}}</div>
</li>
```

- `{{id}}` - Card number (1, 2, 3, etc.)
- `{{Front}}`, `{{Back}}`, etc. - Your card fields
- `{{Front//Text}}` - Fallback syntax for multiple card types

#### CSS Styling
Add any CSS to style your cards:
```css
.id { display: none; }
li { border-bottom: solid; height: 20px; }
ul { column-count: 3; }
```

### Query Syntax

Use Anki's search syntax to filter cards:
- `deck:"Deck Name"` - All cards in a deck
- `deck:"Deck Name" card:1` - Only specific card type
- `tag:important` - Cards with specific tag
- Combine with AND, OR, etc.

### Save and Reuse

Click **Save** to store your current template, CSS, and query for the selected deck. The next time you open the dialog, your settings will be restored.

## Preview Feature

The preview panel shows how your exported HTML will look:

1. Set the number of cards to preview (default: 10)
2. Click **Preview** to generate
3. The preview shows the first N cards with your CSS applied
4. Adjust your template/CSS and preview again until satisfied

## Tips

- Start with a small preview count (5-10) while designing your layout
- Use the preview to test your CSS before exporting large decks
- Save your templates for each deck to reuse them later
- Images are automatically embedded, so the HTML file is completely standalone
- The exported HTML file can be opened in any web browser

## Credits

Based on the original "Export cards to Html" addon. Updated and enhanced with modern features including live preview, better UI, and support for current Anki versions.

## Support

If you encounter any issues or have suggestions, please report them on the addon's GitHub page or AnkiWeb reviews.

## Keyboard Shortcut

- **Ctrl+M** - Open the Export deck to HTML dialog
