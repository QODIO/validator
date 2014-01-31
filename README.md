validator
=========

Validator is a JQuery validation plugin for forms. It can validate text, textarea, password, checkbox and select elements.
With these different elements Validator supports: required, dependency on checkbox, min/max length, email, number, digits and some positioning of error messages.
[You can see a demo here](http://opensource.faroemedia.com/validator).


Usage
-----
###### include in head:
```html
<script src="jquery-1.10.2.min.js"></script>
<script src="fm.validator.jquery.js"></script>
```

###### plugin activation:
By default when initialized, the plugin will look for any form that contain the class validator, add itself to the submit event of the form, and then look for validator html5 data attributes that indicate what and how it the elements in the form should be validated.
But you can also validate a form manually, by running the Validator.validate function. Here is an example:
```javascript
if (Validator.validate('#someForm')) {
	alert('The form is valid, awesome!');
	return true;
} else {
	alert('The form is NOT valid!');
}
```

###### html5 data attributes:
Here is an example of an textbox being required and the content being required to be between 3 and 12 characters.
```html
<form method="post" class="validator">
  <input type="text" data-required data-min="3" data-max="12">
</form>
```

Supported validations
-----

#### Text inputs:
| Attribute				| Valid values											| Description
|-----------------------|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| data-require			| no value												| If this is set, then the input will require some content 																																		|
| data-required-if		| element id											| If set to an id of a checkbox, then it will only validate if said checkbox is checked																											|
| data-min=0-9			| `0-9`													| The minimum length of the input																																								|
| data-max=0-9			| `0-9`													| The maximum length of the input																																								|
| data-type				| `email`, `url`, `number`, `digits`					| **email** are **url** are self explanatory, **number** are the characters `0-9` `+` `-` `.` `,`, **digits** are the characters `0-9` only														|
| data-error-position	| `before`, `after`, `before-`tagname, `after-`tagname	| By default the error messages will appear before the input element in the DOM, but you can also set it to appear `after`, and `before` and `after` the closest parent matching the tagname	|
<br>

#### Password inputs:
| Attribute				| Valid values											| Description
|-----------------------|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| data-require			| no value												| If this is set, then the input will require some content 																										|
| data-required-if		| element id											| If set to an id of a checkbox, then it will only validate if said checkbox is checked																			|
| data-min=0-9			| `0-9`													| The minimum length of the input																																|
| data-max=0-9			| `0-9`													| The maximum length of the input																																|
| data-match			| element id											| If set to an id of another input element, it will match the contents against that element.																	|
| data-error-position	| `before`, `after`, `before-parent`, `after-parent`	| by default the error messages will appear before the input element in the DOM, but you can also set it to appear `after`, `before-parent`, and `after-parent`	|
<br>

#### Checkbox inputs:
| Attribute				| Valid values											| Description
|-----------------------|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| data-require			| no value												| If this is set, then the input will require some content 																										|
| data-required-if		| element id											| If set to an id of a checkbox, then it will only validate if said checkbox is checked																			|
| data-error-position	| `before`, `after`, `before-parent`, `after-parent`	| by default the error messages will appear before the input element in the DOM, but you can also set it to appear `after`, `before-parent`, and `after-parent`	|
<br>

#### Select inputs:
| Attribute				| Valid values											| Description
|-----------------------|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| data-require			| no value												| If this is set, then the input will require some content 																										|
| data-required-if		| element id											| If set to an id of a checkbox, then it will only validate if said checkbox is checked																			|
| data-error-position	| `before`, `after`, `before-parent`, `after-parent`	| by default the error messages will appear before the input element in the DOM, but you can also set it to appear `after`, `before-parent`, and `after-parent`	|
<br>

#### Textareas:
| Attribute				| Valid values											| Description
|-----------------------|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| data-require			| no value												| If this is set, then the textarea will require some content 																										|
| data-required-if		| element id											| If set to an id of a checkbox, then it will only validate if said checkbox is checked																				|
| data-min=0-9			| `0-9`													| The minimum length of the textarea																																|
| data-max=0-9			| `0-9`													| The maximum length of the textarea																																|
| data-type				| `url`													| If type is set to `url`, then a valid url is required 																											|
| data-error-position	| `before`, `after`, `before-parent`, `after-parent`	| by default the error messages will appear before the textarea element in the DOM, but you can also set it to appear `after`, `before-parent`, and `after-parent`	|
<br>



Browser compatibility
---------------------
* IE ???
* Chrome ???
* Firefox ???
* Safari ???
* Opera ???



Copyright and license
---------------------
The MIT License (MIT)

Copyright (c) 2014 Faroe Media

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
