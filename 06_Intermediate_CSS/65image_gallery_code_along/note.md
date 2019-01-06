## Note about Image Gallery Code Along

Hi Everyone!
Just so you don't get confused, around the 8 minute mark in the next video, Colt goes over the image sizing calculation. He mistakenly says "..each one of these [images] is 10%..", when he should have said "each one of these is 30%, making 90% total, plus 1.66% times 6 for the margins, which equals 99.96%" (nearly 100%).

Also, if you use images of varying dimensions then you may encounter some odd behavior in your grid. See here for a solution.

Solution: 

In your html file, instead of placing image elements like Colt does in the video, you can put div elements that have a class of image, and another class of the image number. Like this:

`<div class="image image1"></div>`
`<div class="image image2"></div>`
`<div class="image image3"></div>`
 
`<div class="image image4"></div>`
`<div class="image image5"></div>`
`<div class="image image6"></div>`
 
`<div class="image image7"></div>`
`<div class="image image8"></div>`
`<div class="image image9"></div>`
Next we manipulate the image class of the div element in CSS:

.image {
    height: 300px;
    width: 30%;
    float: left;
    margin: 1.66%;
    background-size: cover;
    background-position: center center;
}
You can notice there are some properties that Colt used for the img elements in this lecture's video. This basically makes the 9 divs we defined have fixed height and proper size so we can 'fill' them in with images. The trick is that we make our images literally the backgrounds of the div elements. We do this in CSS too, using the other class we added to our div elements (image1, image2, image3, etc).

.image1 {
    background-image: url(https://images.unsplash.com/photo-1451976426598-a7593bd6d0b2?dpr=2&auto=format&fit=crop&w=1500&h=1000&q=80&cs=tinysrgb&crop=);
}
 
.image2 {
    background-image: url(https://images.unsplash.com/photo-1465405092061-4db6005a2be0?dpr=2&auto=format&fit=crop&w=1500&h=2250&q=80&cs=tinysrgb&crop=);
}
 
.image3 {
    background-image: url(./images/localimage.jpg);    /* this is how you would link local images */
}
... and so forth until image9. Replace the link between the parentheses for each image with the locations of your pictures.
By having images appear as div element backgrounds, we can make them somewhat responsive and preserve their aspect ratio. If we tried to have a fixed height in img elements, the images would just squeeze in width when we make our browser window smaller.


_________________________________________________________________

 If custom images are used, we either need to simply resize them to fixed same dimensions using CSS width/height (may distort them), or use approaches like the one above to prevent distortion.

Also, CSS object-fit property can be utilized in that scenario:

img {
    object-fit: cover;
    height: 400px;
    width: 30%;
    float: left;
    margin: 1.66%;
}
You can read more about object-fit here: https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit

