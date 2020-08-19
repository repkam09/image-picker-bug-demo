## Google Photos Image Multiselection Bug

Reproduced on 
* Chrome Version 84.0.4147.125
* Phone: OnePlus 7 Pro
* Google Photos version 5.6.0.326295331
* OS: Android 10


Issue:

    When using the normal file picker, selecting multiple images works as expected. But when navigating to another app, like Google Photos, from the file picker side menu, selecting multiple images results in only one of them actually being returned to Chrome/webpage.

I created a very simple webpage that simply requests jpeg and png images from the OS in a file picker. It specifies that 'multiple' images are allowed. 

```
<input accept="image/jpeg,image/png" id="add-photos" multiple type="file" onchange="handleUpload()">
```

In the video 'image-picker.mp4' I run through two normal image selections using the built in file picker. Both of those work as expected and you can see on the webpage that the number of images selected matches the number displayed by the webpage.

In the third attempt, I use the 'browse' option to navigate to Google Photos as my selection app. I select a number of images there, but when clicking 'done' and returning to the webpage only 1 image is actually returned.

The second video 'google-photos.mp4' is just testing this 'browse' and select another app flow. In this case, again, Google Photos only returns one image to the browser, but my normal OnePlus Gallery (v3.12.28) seems to work as expected. 