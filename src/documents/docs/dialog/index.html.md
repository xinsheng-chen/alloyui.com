---
layout: single-doc
title: Dialog
tags: 'dialog'
---

# Dialog

The Dialog component displays information to a user in an inline dialog that can be dragged, stacked, or presented as a modal.

---

#### Getting Started

First load the seed file, if you haven't yet.

``` html
<script src="http://cdn.alloyui.com/3.2.8/aui.min.js"></script>
```

Then initialize AlloyUI and load the Dialog module.

``` javascript
AUI().use('aui-dialog', function(A) {
  // code goes here
});
```

---

#### Using Dialog

Let's create a new instance of Dialog component, then write some content into `bodyContent` and define a `title` for this dialog box. Finally, let's render it!

``` javascript
AUI().use('aui-dialog', function(A) {

  var dialog = new A.Dialog({
    bodyContent: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
    title: 'Dialog title'
 }).render();

});
```

---

#### Configuring Dialog

There are some other options that you can pass to your Dialog instance.

For example, you can align the component on the center of your screen by defining `centered` to `true`. You can even change the `width` and `height` of the dialog box.

``` javascript
AUI().use('aui-dialog', function(A) {

  var dialog = new A.Dialog({
    bodyContent: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
    title: 'Dialog title',
    centered: true,
    width: 500,
    height: 150
 }).render();

});
```

Also, you can turn off the ability to drag or resize your dialog, you just have to change `draggable` or `resizable` options to `false`.

``` javascript
AUI().use('aui-dialog', function(A) {

  var dialog = new A.Dialog({
    bodyContent: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
    title: 'Dialog title',
    draggable: false,
    resizable: false
 }).render();

});
```

Another cool thing is that you can add buttons to your dialog component. Just create an array with a `label`, that will be the text of your button, and a `handler`, that will be the function executed after you click on it.

Then go to your `A.Dialog` and define the `buttons` option with your previously array.

``` javascript
AUI().use('aui-dialog', function(A) {

  var myButtons = [
    {
      label: 'Change title',
      handler: function() {
        this.set('title', 'New dialog title');
      }
    },
    {
      label: 'Change body',
      handler: function() {
        this.set('bodyContent', 'New body content');
      }
    }
  ];

  var dialog = new A.Dialog({
    bodyContent: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
    title: 'Dialog title',
    buttons: myButtons,
    centered: true
 }).render();

});
```

For more information about configuration, check the <a href="#">API Docs</a>.