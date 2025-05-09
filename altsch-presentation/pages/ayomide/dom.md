


<h2><span style="color: #D2B48C;">TABLE</span> <span style="color: #D2B48C;">OF CONTENT</span></h2>

* Dom definition                        
* Dom manipulation
* Dom tree(visual representation)
* Dom navigation
* Dom searching(code example)
* Dom modificaton(code example)

<br><h3><span style="color:maroon ;">DOM </span></h3>
 DOM(Document Object Model): is used to interact with elements and contents in the webpage. It represents all webpage content that can be modified.


<br><h3><span style="color: purple;">DOM MANIPULATION</span></h3>
This is the process of using javascript to modify,edit, and delete elements and attributes in a webpage.


---

<h3><span style="color: green;">DOM TREE</span></h3>
A dom tree is a ranking that represents the dom.The document is the root of the dom and it represents the html. A literal tree has different parts, so does the dom tree.
To access the dom tree, open your webpage, inspect, and check the element section.
(Display a video)

<br><video width="450" controls>
    <source src="./Signup form and 2 more pages - Personal - Microsoft​ Edge 2025-05-08 04-34-50.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

---



<h3><span style="color: deeppink;">DOM NAVIGATION</span></h3>
 Usage of javascript to detect or pick elements in the dom and edit them.

 

 <br><h3><span style="color: teal;">DOM SEARCHING</span></h3>
  This is the process of using javascript to search for elements in the webpage.
  
  code example- 
  ```html
  <h1 id="text">Hello family</h1>
    <script>
               let h1 = document.getElementById("text")
               Console.log (h1)
                h1.style.fontSize = “30px”
                 </script>


---

<h3><span style="color: goldenrod;">DOM MODIFICATION</span></h3>

   The use of javascript to edit the webpage content after it has been uploaded.


code example-
```html
<p class="message">Here is the message</p>
<button id="changeBtn">Change the message!</button>
<script>
    let message = document.querySelector(".message");
    let button = document.getElementById("changeBtn");
    button.addEventListener("click", function () {
        message.textContent = "The message has been changed!";
    });
</script>



```




  










