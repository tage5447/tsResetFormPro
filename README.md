
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

Automatic (recommended):

The script detects RSForm forms and works out-of-the-box.

Manual trigger example:

```javascript
window.tsResetFormPro();
```

---

## License

MIT License
