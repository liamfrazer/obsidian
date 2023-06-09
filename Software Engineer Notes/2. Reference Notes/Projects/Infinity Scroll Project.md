2023-04-27 16:19
Status: #Course #ZeroToMastery
Tags: [[JavaScript]] [[CSS]]

# Infinity Scroll Project

* https://loading.io/ can be used to create a custom icon
* [https://fonts.google.com](http://fonts.google.com) can be used for nice fonts
* @import url('https://fonts.googleapis.com/css2?family=Anonymous+Pro&display=swap');

```CSS
title: CSS
icon: css3-alt

```css
@import url('https://fonts.googleapis.com/css2?family=Anonymous+Pro&display=swap');

  

html {

    box-sizing: border-box;

}

  

body {

    margin: 0;

    min-height: 100vh;

    font-family: Anonymous Pro, sans-serif;

}
```


* Google fonts can be used and applied in the CSS
* `@import` is added to the top & then `font-family` with the backup of `sans-serif`

* Centering a H1 div
```CSS
title: CSS
icon: css3-alt


h1 {

    text-align: center;

    margin-top: 25px;

    margin-bottom: 15px;

    font-size: 40px;

    letter-spacing: 5px;

}

```
* Centering an image within the centre of a page
```css
.loader img {

    position: fixed;

    top: 50%;

    left: 50%;

    transform: translate(-50%, -50%);

}
```



* https://unsplash.com/ free images can be used


```css
/* Image container */

.image-container {

    margin: 10px 30%;

  

}

  

.image-container img {

    width: 100%;

}
```


* Unsplash API - [https://unsplash.com/documentation](https://unsplash.com/documentation#creating-a-developer-account)
* Scheme will tell us the location/version/verbs to use
* We're going to use the fetch API on the GET request
* We will need to pass an API key, we can pass the client ID as a query string

* A [[template string]] would be used for the API key, as we would need to pass through variables such as the client ID

```javascript
// Unsplash API

const apiUrl = `https://api.unsplash.com/photos/?client_id=YOUR_ACCESS_KEY`;
```

* https://unsplash.com/documentation#get-a-random-photo

```javascript
// Unsplash API
const count = 30;
const apiKey = '';
const apiUrl = `https://api.unsplash.com/photos/random/?client_id=${apiKey}&count=${count}`;
```


* We pass through random after /photos
* We pass through the `apiKey` and the `count` as mentioned in the documentation


## Simple Async function

```javascript
// Get photos from UnSplash API

async function getPhotos() {

    try {

        const response = await fetch(apiUrl);

        const data = await response.json();

        console.log(data);

    } catch (error) {

        // Catch error here

    }

}
```

* This is a simple async function to pull data back from the Unsplash API
* This includes a try/catch statement to ensure there are no errors
* We `await fetch` a response from the API
* We then save that response as json with `await response.json();`
* If there are any errors, this would come back into the catch statement

* [https://www.w3schools.com/jsref/jsref_foreach.asp](https://www.w3schools.com/jsref/jsref_foreach.asp)
* https://alligator.io/js/foreach-vs-for-loops/

## Creating elements for links and photos, then adding to [[DOM Manipulation|DOM]]

```javascript
// Create Elements for Links & Photos, then add to DOM

function displayPhotos() {

    // Run function for each object in photosArray

    photosArray.forEach((photo) => {

        // Create <a> to link to Unsplash

        const item = document.createElement('a');

        item.setAttribute('href', photo.links.html);

        item.setAttribute('target', '_blank');

        // Create <img> for photo

        const img = document.createElement('img');

        img.setAttribute('src', photo.urls.regular);

        img.setAttribute('alt', photo.alt_description);

        img.setAttribute('title', photo.alt_description);

        // Put <img> inside <a>, then put both inside imageContainer element

        item.appendChild(img);

        imageContainer.appendChild(item);

    });

}
```

* Creating DRY code
* Don't repeat yourself
* A helper function can be used instead of repeating setAtrributes

## Improved code above with a helper function

```javascript
// Helper function to Set Attributes on DOM Elements

function setAttributes(element, attributes) {

    for (const key in attributes) {

        element.setAttribute(key, attributes[key])

    }

}

  

// Create Elements for Links & Photos, then add to DOM

function displayPhotos() {

    // Run function for each object in photosArray

    photosArray.forEach((photo) => {

        // Create <a> to link to Unsplash

        const item = document.createElement('a');

        setAttributes(item, {

            href: photo.links.html,

            target: '_blank',

        });

        // Create <img> for photo

        const img = document.createElement('img');

        setAttributes(img, {

            src: photo.urls.regular,

            alt: photo.alt_description,

            title: photo.alt_description

        });

        // Put <img> inside <a>, then put both inside imageContainer element

        item.appendChild(img);

        imageContainer.appendChild(item);

    });

}
```


## HTML DOM Events
[https://www.w3schools.com/jsref/dom_obj_event.asp](https://www.w3schools.com/jsref/dom_obj_event.asp)

![[Infinite Scroll Functionality.png]]


* We will need two values from our window
* window.innerHeight
* window.scrollY
* We add the two numbers, then compare to the height of everything in the body, including what is not within view
* We will need to modify it by a pixel amount
* When the user scrolls to a certain point, that is where we load more photos to act seamless

```javascript
window.addEventListener('scroll', () => {

    if (window.innerHeight + window.scrollY >= document.body.offsetHeight - 1000) {

  

    }

})
```

```javascript
// Check to see if scrolling near bottom of page, load more photos

window.addEventListener('scroll', () => {

    if (window.innerHeight + window.scrollY >= document.body.offsetHeight - 1000) {

        getPhotos();

        console.log('loading more photos');

    }

})
```


* The issue with this code is that it can be hit multiple times at once, when in theory it should only be loading once the user reached the end of the next 30 photos, not instantly once they've reached the end for the first time

https://www.w3schools.com/jsref/event_onload.asp

* Setting the count to 5 on the initial load allows the page to load much quicker on the first time, once the 5 images have loaded, the count can then be set to 30 for the next load
  
```javascript
// Unsplash API

let count = 5;

const apiKey = 'UXk7dM2pTcQilECI5I9ZumGv3W_yXKJjuyAt-OTndqM';

const apiUrl = `https://api.unsplash.com/photos/random/?client_id=${apiKey}&count=${count}`;

  

// Check if all images were loaded

function imageLoaded() {

    imagesLoaded++;

    if (imagesLoaded === totalImages) {

        ready = true;

        loader.hidden = true;

        initialLoad = false;

        count = 30;

    }

}
```

---
# References
https://loading.io/
https://unsplash.com/
https://academy.zerotomastery.io/courses/1007166