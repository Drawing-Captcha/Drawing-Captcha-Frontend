# Drawing-Captcha Frontend

Welcome to the Drawing-Captcha Frontend project! This repository provides the necessary frontend components to integrate the Drawing-Captcha system into your web forms. This README will guide you through the installation and implementation process.

## Installation

### Option 1: Usage with CDN

For a quick and easy integration, you can use the Drawing-Captcha frontend via our CDN. This eliminates the need to install the package locally via npm. Simply add the following script tag to your HTML file:

```html
<script src="https://cdn.drawing-captcha.com/captcha.js"></script>
```

### Option 2: Installation via npm

If you prefer to manage the Drawing-Captcha frontend locally within your project, you can install it via npm. Run the following command in your project console:

```bash
npm i @drawing-captcha/drawing-captcha-frontend
```

## Implementation Guide

### Step 1: Initialize Captcha

First, you need to call the initialize function from the package you just installed. Add the following script tag to your HTML:

```html
<script src="/js/captcha.js" onload="(function(){initializeCaptcha()})()"></script>
```

### Step 2: Configure Captcha with API Key

Generate an API key from your Drawing Captcha Instance in the back office. Then, add the API key and server details into the following script variables:

```html
<script>
    var CaptchaHiddenAPIKey = "YOURKEY";
    var CaptchaServerWithPort = "https://drawing.yourdomain.com";
</script> 
```

### Step 3: Add Drawing-Captcha Attribute to Your Form

To enable the captcha on your form, add the `drawing-captcha` attribute to the form element. Here is an example of what your form could look like:

```html
<form drawing-captcha class="app-form" id="contactForm" action="./success.html">
    <div class="app-form-group">
        <input class="app-form-control" type="text" id="name" placeholder="Your Name" required>
    </div>
    <div class="app-form-group">
        <input class="app-form-control" type="email" id="email" placeholder="EMAIL" required>
    </div>
    <div class="app-form-group message">
        <input class="app-form-control" type="text" id="message" placeholder="MESSAGE" required>
    </div>
    <div class="app-form-group buttons">
        <button type="reset" class="app-form-button">CANCEL</button>
        <button type="submit" class="app-form-button">SEND</button>
    </div>
</form>

<script>
    var CaptchaHiddenAPIKey = "bd494f45-fc75-4a58-a5ae-815d18c35f44";
    var CaptchaServerWithPort = "https://drawing.wpesic.dev";
</script> 
<script src="/js/captcha.js" onload="(function(){initializeCaptcha()})()"></script>
```

## Additional Resources

For further information and detailed documentation, please visit the official Drawing-Captcha documentation at [docs.drawing-captcha.com](https://docs.drawing-captcha.com).

## Demo

You can find a demo of the Drawing-Captcha implementation on GitHub: [Drawing-Captcha-Demo](https://github.com/Drawing-Captcha/Drawing-Captcha-Demo) or try it live at [demo.drawing-captcha.com](https://demo.drawing-captcha.com).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

