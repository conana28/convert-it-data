# convert-it-data

## External Data

# Convert-It Data Management Guide

This guide explains how to manage the external data files used by the Convert-It app.

## Overview

The app uses two main data files hosted on GitHub:
- `common-values.json` - Common conversion values and measurements
- `temperature-references.json` - Temperature reference points with categories

## Updating Data Files

### 1. Access Your GitHub Repository

1. Go to your GitHub repository: `https://github.com/yourusername/convert-it-data`
2. Navigate to the file you want to update

### 2. Edit a File

#### Option 1: Edit directly on GitHub
1. Click on the file you want to edit
2. Click the pencil icon (Edit this file)
3. Make your changes in the editor
4. Scroll down to "Commit changes"
5. Add a descriptive commit message
6. Click "Commit changes"

#### Option 2: Upload a new version
1. Create and edit the file locally
2. In your repository, click "Add file" → "Upload files"
3. Drag and drop or select your updated JSON file
4. Add a commit message
5. Click "Commit changes"

### 3. Data File Structure

#### Common Values (`common-values.json`)
```json
[
  {
    "item": "Item name",
    "value": "Converted value",
    "category": "Category name"
  },
  ...
]
```

#### Temperature References (`temperature-references.json`)
```json
[
  {
    "description": "Description",
    "celsius": 100,
    "fahrenheit": 212,
    "category": "Category name",
    "cookingTime": "Optional cooking time"
  },
  ...
]
```

## Adding New Categories

To add a new category:
1. Edit the appropriate JSON file
2. Add new items with the new category name
3. The app will automatically display the new category

## Testing Changes

After updating the data files:
1. Open the app on your device
2. The app will fetch the latest data when launched
3. If you're testing locally, you may need to clear the app's cache

## Troubleshooting

If your changes aren't appearing:
1. Check that you committed the changes to the correct branch (usually `main`)
2. Verify the JSON syntax is valid
3. The app caches data locally - try force closing and reopening the app
4. Check your network connection

## GitHub Raw URLs

The app uses these URLs to fetch data:
- Common Values: `https://raw.githubusercontent.com/yourusername/convert-it-data/main/common-values.json`
- Temperature References: `https://raw.githubusercontent.com/yourusername/convert-it-data/main/temperature-references.json`

Remember to replace `yourusername` with your actual GitHub username in the app's code.

