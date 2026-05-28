
# tsResetFormPro

## Introduction

**tsResetFormPro** is a lightweight JavaScript utility designed to provide a reliable reset mechanism for RSForm Pro forms in Joomla 5/6.

---

## What it does

### Solves
- RSForm reset failure after POST
- Conditional fields not resetting correctly
- reCAPTCHA reinitialization issues

### Approach
- Forces GET reload instead of DOM reset
- Intercepts native reset buttons

### Language Support
- English / Swedish (configurable)

---

## Installation

1. Copy `tsResetFormPro.js` to your template or media folder
2. Include it in your Joomla template or custom script loader
3. Ensure it loads after your form

---

## Usage

### Automatic behavior (recommended)

The script works automatically **when using native reset buttons**:

```html
<button type="reset">Reset</button>
```

or

```html
<input type="reset" value="Reset">
```

In these cases:

- The script automatically detects RSForm forms  
- Reset buttons are intercepted  
- A safe reset is performed using a forced GET request  

✅ No additional configuration or `onclick` is required  

---

### Important

The automatic behavior ONLY applies to elements with:

```
type="reset"
```

The following will **NOT** trigger the script automatically:

```html
<button type="button">Reset</button>
<button>Reset</button> <!-- defaults to type="submit" -->
```

Note:  
`<button>` defaults to `type="submit"` if no type is specified.

---

### Manual trigger (optional)

You can manually trigger the reset function when needed:

```javascript
tsResetFormPro();
```

---

### Example: custom reset button

```html
<button type="button" onclick="tsResetFormPro()">
    Reset form
</button>
```

---

## License

MIT License
