# Hacking Panda the Bear's Resume
___

1. Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.
```
document.querySelector('img.profile-image').src = 'https://placebear.com/400/400';
```
  PROTIP: use the inspector to learn the dimensions of the current profile image and use a placeholder image service such as Place Bear to get an image of the same size.

2. Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.
```
document.querySelector('img.photography').src = 'https://placebear.com/325/225';
```

3. Select the heading that says "Panda the Bear" and change it to your own name.
```
document.querySelector('h1.highlight').innerHTML = 'John Lopez';
```
4. Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)
```
document.querySelector('div.info-inner-container:nth-child(2) .info-title').innerHTML = "<i class=\"icon-suitcase\"></i> &nbsp; Job History";
```
5. Change the colour of the body.
```
document.querySelector('body').style.backgroundColor = 'grey';
```
6. Change the colour of each element using the highlight class. Use a for loop to do this.
```
nodeHighlightClass = document.querySelectorAll('.highlight');
for (var i = 0; i < nodeHighlightClass.length; i++) {
  nodeHighlightClass[i].style.color = 'purple';
}
```
7. Change the font family of the h1 to 'monospace'.
```
nodeH1 = document.querySelectorAll('h1');
for (var i = 0; i < nodeH1.length; i++) {
  nodeH1[i].style.fontFamily = 'monospace';
}
```
8. Find a way to select the round icons in the sidebar and then change their colour.
```
nodeSideButton = document.querySelectorAll('a.action-icon-bg');
for (var i = 0; i < nodeSideButton.length; i++) {
  nodeSideButton[i].style.backgroundColor = 'orange';
}
```
9. Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".
```
document.querySelector('input#name').placeholder = 'identify yourself';
```
10. Change the placeholder attribute of the message field to "state your business".
```
document.querySelector('textarea#message').placeholder = 'state your business';
```
11. Give the name field a "value" attribute of "your nemesis".
```
document.querySelector('input#name').value = 'your nemesis';
```
12. Change the value attribute of the email field to "koalathebear@gmail.com".
```
document.querySelector('input#email').value = 'koalathebear@gmail.com';
```
13. Change the value of the submit button on the contact form to "En garde!".
```
document.querySelector('input#submit').value = 'En garde!';
```
14. We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).
```
document.querySelector('input#submit').disabled = true;
```
15. We should help Panda protect their privacy by erasing their personal details from the sidebar.
```
var nodeBioInfo = document.querySelectorAll('span.bio-info-value');
for (var i = 0; i < nodeBioInfo.length; i++) {
  nodeBioInfo[i].innerHTML = '';
}
```
