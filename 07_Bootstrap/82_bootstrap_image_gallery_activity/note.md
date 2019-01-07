## Note about Bootstrap Image Gallery Pt. 1
In the next lecture, titled "Bootstrap Image Gallery Pt. 1", Colt will show you how to get hi-resolution stock images from a website called unsplash. 

The method of getting the image url has changed since this video was created. 

If you find an image you like then you'll need to click on the image to make it full screen at which point the url will change to give you the photo's ID. 
It's the alphanumeric combination that comes after ?photo=.

Once you copy the photo's ID then you can add it to the source.unsplash address like so: 

`<img src="https://source.unsplash.com/cPF2nlWcMY4">`

## Note about Font-awesome
In the next video we will be using a font/icon library called Font Awesome. Font Awesome can now be found at http://fontawesome.io/

It should also be noted that Font Awesome has released a newer version than the one being used in this course. The syntax has changed ever so slightly. For example, to insert a retro camera icon you would use the following markup:

<i class="fas fa-camera-retro"></i> 

You'll notice that instead of the class name "fa", which we'll be using in this course, we have "fas". The "s" at the end stands for "solid". The changes are backwards compatible though, you can write it how Colt does in the video and that should also work.

I recommend using the following CDN script for the latest version:

<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.3.1/css/all.css" integrity="sha384-mzrmE5qonljUremFsqc01SB46JvROS7bZs3IO2EmfFsd15uHvIt+Y8vEf7N7fWAU" crossorigin="anonymous">
