# textarea_MaxCharacterLimit()
A jQuery function that allows you to limit the amount of characters within a html `textarea` field and display characters used and remaining.

The function will display the following three results:
1. The amount of characters available.
2. The percentage of characters used.
3. The amount of characters used.

Example of display: 

```css
500 (0% used :: 0 characters used)
```


## Usage

Here is how you use the `textarea_MaxCharacterLimit()` function:

1. Include the function in your global `.js` file, or add it inline, or place the function in a new `.js` file that you link to via `<script src="/path/to/textarea_MaxCharacterLimit.js"></script>`.

2. You do not have to modify your existing `<textarea>` at all, unless it does not have an `id="someUniqueValue"`, in which case you will need to add that.

3. Define the `textarea_MaxCharacterLimit()` function at the bottom of your page, after your jQuery.

## Example:

```html
<textarea name="Content" id="Content"></textarea>
Characters remaining: <span id="ContentCountPercentLeft"></span>
```
And at the bottom of your page, use this JavaScript:

```javascript
<script>
textarea_MaxCharacterLimit(500, 'Content', 'ContentCountPercentLeft');
</script>
```

## Bootstrap _(4)_ Form Usage Example

```html
<div class="card">
	<div class="card-header">Contact Us</div>
    <div class="card-body">
        <label for="Content">How can we help?</label>
        <textarea class="form-control" rows="5" name="Content" id="Content" placeholder="How can we help?" tabindex="1" minlength="1" maxlength="500" required></textarea>
    </div>
    <div class="card-body text-muted small">
        Characters remaining: <span id="ContentCountPercentLeft"></span>
    </div>
    <div class="card-footer">
        <button type="submit" class="btn btn-primary" tabindex="2">Contact us</button>
    </div>
</div>
```


## Function Variables

The `textarea_MaxCharacterLimit()` requires three variables be passed to it.

1. The `maximum` amount of characters you want to be allowed within the `<textarea>`
2. The `id="someUniqueValue"` that you have assigned to your `<textarea>`
3. The `id="ContentCountPercentLeft"` _(based on above example)_ of your `<span id="ContentCountPercentLeft"></span>` for displaying results

## Requirements

This function requires the [jQuery JavaScript Library](https://github.com/jquery/jquery) be loaded _before_ calling this function.

## Versions

July 25, 2019 - Version `1.0.0` is available in both [.min.js](https://github.com/4cm/textarea_MaxCharacterLimit/blob/master/textarea_MaxCharacterLimit.min.js) format and in a [.js](https://github.com/4cm/textarea_MaxCharacterLimit/blob/master/textarea_MaxCharacterLimit.js) format.

## Notice

It should go without being said, but we still need to, that you will still need to do processing on the server side, when a user submits the form, to enforce a maxlength. JavaScript can be disabled in all browsers these days, thereby making this function not load/work.

## License

The MIT License (MIT). Please see [License File](LICENSE) for more information.
