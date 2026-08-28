---
layout: post
title: About
permalink: /about/
comments: true
---

## As a conversation Starter

Here are some places I have lived and visited.

<comment>
Flags are made using Wikipedia images
</comment>

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"flag": "0/01/Flag_of_California.svg", "greeting": "Hey", "description": "California - forever"},
        {"flag": "5/54/Flag_of_Washington.svg", "greeting": "Hello", "description": "Washington - lived 6 years"},
        {"flag": "b/b9/Flag_of_Oregon.svg", "greeting": "Hi", "description": "Oregon - visited"},
        {"flag": "1/1a/Flag_of_New_York.svg", "greeting": "Whats up", "description": "New York - visited"},
        {"flag": "f/f2/Flag_of_Massachusetts.svg", "greeting": "How's it going", "description": "Boston - visited"},
        {"flag": "0/09/Flag_of_South_Korea.svg", "greeting": "Annyeonghaseyo", "description": "South Korea - visited"},
    ];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = http_source + location.flag; // concatenate the source and flag
        img.alt = location.flag + " Flag"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

### Journey through Life

Here is what I did in those places:

- 🏫 Went to Fisher's Landing Elementary School in Vancouver, Washington
- 🚗 Moved to San Diego when I was in kindergarten
- 🏫 Went to Turtleback Elementary School, and Monterey Ridge Elementary School in San Diego
- 🏫 Oak Valley Middle School, promoted 2025 (in San Diego)
- 🏫 Currently in Del Norte High school, will graduate in 2029
- 🎾 Playing 2 years of JV tennis, team captain 1 year at Del Norte
- ✈️ I've visited South Korea 3 times to visit family
- 🏢 I visited New York and Boston in 2021

### Culture, Family, and Fun

My lifef mainly revolves around family, friends, and faith.

- I am fully Korean, my parents met at church and got married after
- My family is pretty big, I have 3 other siblings, and each of my parents have 3 other siblings as well. I have lots of aunts and uncles and a couple of cousins.
- I have an older sister, older brother, and a younger sister, and both of my older siblings are in UCLA
- I go to San Diego Calvary Korean Church with my family
- The gallery of pics has some of my family, fun, culture and faith memories.

<comment>
Gallery of Pics, scroll to the right for more ...
</comment>
<div class="image-gallery">
  <img src="https://lh3.googleusercontent.com/d/1kz3_hSb9dEZ-jwqW7zK29QpdW9-efcyL" alt="Image 1">
  <img src="https://lh3.googleusercontent.com/d/1C2dlsg7I9S3kl9HSm3dCYWaorbQc6mzW" alt="Image 2">
  <img src="https://lh3.googleusercontent.com/d/16g39Mldl1eZxtOYTgFMVOR8CDmMsbiDA" alt="Image 3">
  <img src="https://lh3.googleusercontent.com/d/12dV1NY1B1PDRAl-PpDmCI9AhKnJxhvr6" alt="Image 4">
  <img src="https://lh3.googleusercontent.com/d/1L8X-D5aloVZ1wM92V87SL7BcCEEYfNI5" alt="Image 5">
</div>
