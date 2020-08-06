## Emoji picker

Add a emoji to textarea on your web page.

<img src="https://raw.githubusercontent.com/takopom/emoji-picker-textarea/master/demo.png" alt="Demo screen shot" width="250px">

## Emoji list

Its emoji list was created based on the [Unicode Emoji data files](https://unicode.org/Public/emoji/13.0/).
The order is same the [emoji-test.txt](https://unicode.org/Public/emoji/13.0/emoji-test.txt).

### Excludes

- v13.0
- Skin tones
- Unqualified emoji

## Usage

1. Install a `emoji-picker-textarea` with npm.

```
$ npm install emoji-picker-textarea
```

2. Add the stylesheet link in your `<head>` section.

```
<link rel="stylesheet" type="text/css" href="node_modules/emoji-picker-textarea/css/emoji-picker-textarea.css" />
```

3. Add the JavaScript link before the end of your `<body>` section.

```
<script type="text/javascript" src="node_modules/emoji-picker-textarea/index.js"></script>
```

4. Add some JavaScript codes are creating `EmojiPicker`, showing the picker and hiding it.

```
let emojiPicker;
let isOpen = false;

function createEmojiPicker() {
  // Add a emoji to this textarea.
  let textarea = document.getElementById("textarea");
  // Show the picker to this element. The element would be parent of the picker.
  let picker_area = document.getElementById("emoji-picker-area");
  // Create the picker by specifying the width and height of it.
  emojiPicker = new EmojiPicker(textarea, picker_area, "250px", "200px");
}

function toggleEmojiPicker() {
  if (isOpen) {
    // Hide the picker.
    emojiPicker.hide();
   else {
    // Show the picker.
    emojiPicker.show();
  }
  isOpen = !isOpen;
}
```
