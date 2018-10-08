# SlackTheme

For Windows:
1) go to AppData\Local\slack\app-3.3.1\resources\app.asar.unpacked\src\static   ( if you open a folder and paste that link after your username it will take you straight there )
2) Right click and edit ssb-interop.js file
3) Paste the following code at the bottom:

```
document.addEventListener('DOMContentLoaded', function() {
  $.ajax({
    url: 'https://cdn.rawgit.com/TheSpitefulOctopus/SlackTheme/9903b00f/customDark.css',
           success: function(css) {
       $("<style></style>").appendTo('head').html(css);
     }
   });
});
```
