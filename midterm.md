
Portland Code School
Front End Development
Midterm exam

The point of this exam is:

1. to see what you remember or are able to look up and, 
2. through the clarity of your explanation, whether you both understand the answer and can articulate it clearly. 

Please do not collaborate on these answers. Also, when you look up an answer, please do not copy and paste the answer -- rewrite it in your own words. You will need to be able to answer these questions in an oral exam without notes later. You will not be given a letter grade. This test is part of a conversation about how to help you get the most out of this class.


Instructions:

1. If you need clarification about any of these questions, ask it in the Slack channel. I will answer it for everybody.

2. This is a open-book test. However, please don't collaborate on the answers. Also, for each answer, indicate either "I knew this from memory" or "I looked this up."

3. Copy this text into a text file and add your answer after each question.

4. When this exam asks you for working code that combines HTML, CSS, and Javascript, please put that code in a codepen.io "pen", save it, and put the URL in your response. That way, you can test it and I can verify that it works. If it justs asks for a snippet or a particular tag, just include the code in your answer.

5. When you are done, put the text file in a github "gist" and email me the URL.


HTML
----------------------------------------
Q01. What what does the "separation of concerns" concept mean in computer science?
Breaking up the problems into modules at different levels. In web design it can be separating structure, style and interactivity, or parts whiting a project that build up the website as modules. (knew it but looked up to confirm)

Q02. What is the primary "concern" of HTML? That is, what is it for?

Structure, organizing content, that can later be styled and made interactive with JS.

Q03. In an HTML page, the <html> element has two child elements. What are they? It has one sibling. What is it?

- children: Head and body
- sibling: document window

Q04. What is the difference between structural markup and semantic markup? Give an example of each. (Looked it up)
> “Structural markup is when elements are used to describe the structure of a document (webpage).” ([http://www.motive.co.nz/glossary/markup.php](http://www.motive.co.nz/glossary/markup.php))
> 
Semantic HTML is the use of HTML markup to reinforce the semantics, or meaning, of the information in webpages rather than merely to define its presentation or look. ([http://en.wikipedia.org/wiki/Semantic_HTML](http://en.wikipedia.org/wiki/Semantic_HTML))

Structural markup has every information in the html document that browsers need to render the page together for the user, while semantic markup separates the structure and styles: styling is in a separate CSS file, linked to the html.

structural markup, in html file:


    <p style="color:blue; font-size:36px">some big, blue text</p>
 
semantic markup in html file:

    <p class=“big-blue”>some big, blue text</p>
in css:

    .big-blue {
      color: blue;
      font-size: 36px; 
    }

Q05. What does the DOCTYPE directive do? When would you ever use something other than "html" for its value?

Doctype tells the browser what kind of document it should expect and how to read it. There are different types of HTMLs, like XHTML or XML.

Q06. In the context of HTML markup, define the following terms and give an example of each:

- "tag name":  defines the name of a tag `<h1></h1>`
- "tag": the tags are the elements within an html document that contain the name/type and formatting information, with an opening and a closing tag (`<form>, <table>`) some are self closing, like `<br/> or <hr/>`
(“mark a section of a document with a formatting command”; webopedia.com)
- "container":
- "element": Html elements are the building blocks of html `<textarea>`
- "attribute": attributes describe what value the element will have, like `align, type, href`

Q07. What are character entities?  (looked up, didn’t remember they were called character entities.) Give your favorite three examples both in HTML format and as descriptions.

Character entities are special characters and symbols described with regular letters (&name;) that should be used in html instead of symbols

    &nbsp; - non breaking space
    &quot; - quote “
    &Eacute; - É (And all the other characters in the Hungarian alphabet)

Q08. There are four "core" HTML attributes. These are attributes that can be used in any element. Two are "class" and "id". What are the other two? What are they for?

looked it up: [http://www.w3.org/TR/html-markup/global-attributes.html](http://www.w3.org/TR/html-markup/global-attributes.html)

- class: classification(s) that the element belongs to
- id: unique identifier for an element
- style; specifies css styling that applies to an element
- title: additional (optional) information 

Q09. What is the purpose of the `<head>` element? Give three examples of elements that can only appear in the head element along with what their purpose is.
	
 The head element contains information that are not visible for the user, like meta tags, stylesheet links and scripts

Q10. Give three examples of how the `<meta>` element can be used, including both the syntax of the tag for each example and a comment about what it does.

This is an html document, using utf-8 charset coding

	`<meta http-equiv="Content-Type" content="text/html; charset=utf-8"> `

This meta tag contains the keywords that search engines can use.

`<meta name="keywords" content=“these, are, keywords"> `

This one tells the googlebot to follow the page so it will be indexed and listed in google searches

`<meta name="Googlebot" Content="index,follow"> `

Q11. What is the purpose of the `<body>` element? How many body elements can there be on a responsive web page?

The body element contains all the visible elements of the webpage.
There is only one `<body>` element, on a responsive webpage the media queries can make it appear in different styling

Q12. What is the value of a `<div>` element in semantic markup? In HTML5, the `<div>` element has been replaced in certain circumstances with several specialized elements. Give an example of three.

The value is all the information stored between a specific opening and closing (`<div></div>` element, that can have an unique identifier or a more generic classification. For example: `<header>, <nav>, <footer>`

CSS
----------------------------------------
Q13. What is CSS for?

To create a website, there are 3 components: html for structure, css for style and design and JavaSript for interactivity with the user ’s actions.

Q14. What are the three places you can place CSS style information? In which files? Give a simple code example of each.

Css can be inline style, within the html or in a separate file.
	[http://codepen.io/glanzb/pen/tGsxn](http://codepen.io/glanzb/pen/tGsxn)


Q15. Give the general syntax for a CSS rule. Include the selector, the body, properties and values. Give an example of a rule with several properties.
.example-class {
  		color: #E8770C;
  		font-size: 1.5em;
 		margin: 0 5px;
		padding: 1%;
    		}

Q16. Give an example of a descendant selector. Include two code snippets, one for the HTML and one for the CSS, that will turn a target element, say a cell in a row in a table, red. This is where a codepen.io URL would be sweet.
	[http://codepen.io/glanzb/pen/tGsxn](http://codepen.io/glanzb/pen/tGsxn)


Q17. Give an example of an attribute selector. Again, include code snippets to demonstrate how to turn the target element, say a field in a form, red.
	[http://codepen.io/glanzb/pen/tGsxn](http://codepen.io/glanzb/pen/tGsxn)


Q18. There are two aspects of "the cascade" -- "proximity" and "specificity". Describe these two dimensions and give examples of each. 


Cascading generally means that the order of specifications build on each other, so if the same element is styled twice, the one described later will be applied  - if they are the same depth of specificity. Some selectors are more specific than others, in this case the order doesn’t matter.

    table th, td{
      text-align: center;
      font-variant: titling-caps;
      background-color: #FF3D31;
      color: #360D0A;
      font-size: 1.25em
    }
    
    th {
    font-variant: small-caps;
    }

more specific: form with 3 textfields (see code pen /* Q17. attribute selector */)

    [type="text"] {
      background-color: red;
    }
    
    #name2 {
      background-color: blue;
    }
    
Here are some specific (no pun intended) questions: (had to try it in code pen)

Q19. Which is more specific, a tag selector or a class selector?

The class selector

Q20. How about a class selector or an attribute selector?

Class selector is more specific than the attribute selector

Q21. Examine this code snippet: (i had to try it in code pen)

    <style>
    .warning { color:red;}
    </style>
    <p class="warning" style"color:blue;">This is the text.</p>

What color is the text? Why?

red, because the class selector is more specific.

Q22. How do you replace the default bullets of an unordered list with small icon images? Show both the HTML and the CSS.

[http://codepen.io/glanzb/pen/tGsxn](http://codepen.io/glanzb/pen/tGsxn)

Q23. Part 1: Here's some HTML of a paragraph with five words:

    <p class="wordy">A small bit of text</p>

Write the CSS to make this appear as follows:

* Centered on the page. text-align: center
* 12 point Helvetica font. font-family: Helvetica, sans-serif; font-size: 12pt
* Some sort of ivory or cream background color. background-color: #FFFFE9
* No less than 500 pixels wide and 300 tall. min-width: 500px; min-height: 300px;
* No more than 500 pixels wide and 500 pixels tall. max-width: 500px; max-height: 500px
* Inside shadow to make it appear inset in the page. box-shadow: inset 0px 0px 15px 5px rgba(0,0,0,0.25); (had to look up “inset”)

Part 2. Replace the contents with 1000 words of "lorem ipsum" gibberish. Modify your CSS so that, without making the box any bigger, and without the text spilling out of the box, the user can somehow see all the words

[http://codepen.io/glanzb/pen/cbyDa](http://codepen.io/glanzb/pen/cbyDa)

Q24. What is the difference between the following two CSS properties?

	display: none;

and 

	visibility:hidden;

[http://www.w3schools.com/css/css_display_visibility.asp](http://www.w3schools.com/css/css_display_visibility.asp)
visibility:hidden hides an element, but it will still take up the same space as before. The element will be hidden, but still affect the layout.
display:none hides an element, and it will not take up any space. The element will be hidden, and the page will be displayed as if the element is not there:

JavaScript
----------------------------------------
Q25. What is the role of JavaScript in a web page?

JavaScript adds the functionality to webpages, making them interactive.

Q26. What are the two forms of the `<script>` element? (looked it up)

[http://www.w3.org/TR/html401/interact/scripts.html](http://www.w3.org/TR/html401/interact/scripts.html)
	
> There are two types of scripts authors may attach to an HTML document:
> 
> Those that are executed one time when the document is loaded by the user agent. Scripts that appear within a SCRIPT element are executed when the document is loaded. For user agents that cannot or will not handle scripts, authors may include alternate content via the NOSCRIPT element.
> Those that are executed every time a specific event occurs. These scripts may be assigned to a number of elements via the intrinsic event attributes.

Q27. Where should you place the `<script>` element in your HTML file?

At the bottom of the page, before the closing body tag.

Q28. As the browser loads the HTML file, when does it execute any JavaScript it finds?

The javascript should be placed to the end of the page, so all html DOM elements that it has to interact with are loaded, but the script will execute when the events that are set in it happen.

Q29. What is the difference between a statement and an expression? (looked it up to clarify)

An expression is a phrase that defines a value.
A statement is a section where some code is being executed, ends with a semicolon.
As: expressions are words, statements are sentences.

Q30. Are semicolons required?

No, but makes the code more readable.

Q31. In your own words, what is an object? What are two predefined objects you have used in your code so far?

Objects are like variables, but they can contain many values, defined in pairs. (looked up predefined objects)

    var arr = new Array(element0, element1, ..., elementN);
    var x = Math.floor((Math.random() * 10) + 1);

Q32. Declare a function named “plus” that takes two parameters and returns their sum. Test that function with the following values by calling the function four times and writing the result to the console:

- 0 and 0
- 2 and 2
- -1 and 1
- -1 and -1

js: [http://codepen.io/glanzb/pen/cbyDa](http://codepen.io/glanzb/pen/cbyDa)

----------

    function plus(a, b){
      console.log(a+b);
    };
    
    plus(0,0);
    plus(2,2);
    plus(-1,1);
    plus(-1,-1);

Q33. What is the JavaScript DOM API?

The objects that javaScript can interact with, like the document itself.

Q34. What is an event listener?

An event listener is the "action" that has to happen in order to start a function (page loading, user clicking etc.)

Q34. Given a button:

	<button id="sayHello">

We want to run the following JavaScript statement when the user clicks the button: alert("Hello.");

Put this statement in a function and attach it as an event listener to the button.

Write a function named "attachEventListener" twice:

A. Attach an event listener with the DOM API

[http://codepen.io/glanzb/pen/iFulL](http://codepen.io/glanzb/pen/iFulL) (not there yet)

B. Attach an event listener with jQuery

[http://codepen.io/glanzb/pen/GErpf](http://codepen.io/glanzb/pen/GErpf)

Git
----------------------------------------
Q35. What is the working directory?

- The working directory is the directory on the local hard drive that contains the project files

Q36. Using the command line, how do you add a new file to the working directory?
	`git add <filename>`

Q37. What is the staging area?

The staging area is where the modified files and committed files are put locally, waiting to be pushed to the remote repository. 

Q38. Using the command line, how do you add a new file to the staging area

    git commit <filename> -m “commit message”
Q39. What is a repository?

It is a remote container that holds the project files.

Q40. Using the command line, how do you add a new file to the repository?

    git push

Q41. This is a developer’s workflow. You normally work on the branch “developer”. Your team shares all working code to “master”. Everybody is authorized to commit to master.  Assume that there are no merge conflicts.
Enter the git commands for the appropriate steps:

* Go to the correct branch for the next step: `git checkout master` 
* Get your team’s changes from github: 		`git pull`
* Go to the correct branch for the next step: 	`git checkout developer` 
* Combine the team’s work with yours: 		`git merge master`	
* Go to the correct branch for the next step: 	`git checkout master`
* Share your work with the team (two steps): `git merge developer, git push` 

General coding
----------------------------------------
Q42. Give two examples of delimiters in each of these three languages: HTML, CSS, and JavaScript. (6 total)

    <img src="img.jpg" alt="image" width="20px" height="30px">
    <input type="text" id="text" name="text">

	p {		
		color: red;
    	background-color: blue;				
    	}
    
    div {
    	padding: 0 10px;
    	margin: 5px 0 10px;
    	}

	var myCars = ["Renault", "Mazda", "Jeep"];
	var kidsAge = (4 + 8)
    
    

Q43. Give two examples of name/value pairs in each of these three languages: HTML, CSS, and JavaScript.  (6 total)

	id=“fun-stuff”
	type=“submit”
	
	border: 1px solid #000;
	background: #fff;
	
	var fruit = "apple";
	var string = (1, "exhausting", "test");
	
	



