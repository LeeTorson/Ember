# Ember
A best practise email template to be used as a starter kit for new emails.

## Best Practice Techniques
**Don't** use `<br />` tags for spacing, create single cell rows with a `<td></td>` inside instead so you can control the spacing through border, padding-top or bottom etc.

```html
<tr>
	<td align="left" valign="top" style="padding-top: 10px; padding-bottom: 10px;">Example Text</td>
</tr>
```
---

Always add a `valign` attrbute on all `<td>` tags, for best pratice and consistency.

---

When we want two elements next to each other to stack on mobile, we use `<th></th>` tags instead of `<td></td>` to work acorss all devices, this is to fix the latest IOS versions. 

```html
<tr>
	<th align="left" valign="top" style="width: 300px; padding-bottom: 10px; padding-top: 10px; vertical-align: top; font-weight: normal;" class="fullWidth align-center"></th>
	<th align="right" valign="top" style="width: 300px; padding-bottom: 10px; padding-top: 10px; vertical-align: top; font-weight: normal;" class="fullWidth align-center"></th>
</tr>
```

---

Don't forget to change the `<title></title>` attribute value on each email to fit the campaign/client intended instead of leaving it to the default **Ember Template**

---

All `<img>` tags must look like the below example, missing these attributes out can cause issues across clients. i.e. Styling, alt tags etc. 

```html
<img src="http://placehold.it/200x200" width="100" height="100" alt="placeholder" style="border: none; outline: none;" />
```

Images are always 2x there size also, so if you have an image that is both 200px width and height. You would set the width to be `width="100" height="100"` so that it's retina friendly/mobile proof.
