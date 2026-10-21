<h1>
  <span class="headline">Intro to CSS</span>
  <span class="subhead">Setup</span>
</h1>

Open your Terminal application and navigate to your `~/code/ga/lectures` directory:

```bash
cd ~/code/ga/lectures
```

Make a new directory called `intro-to-css`, then enter this directory:

```bash
mkdir intro-to-css
cd intro-to-css
```


Then, create an `index.html` file, and a `style.css` file. These files will hold your work for this lecture:

```bash
touch index.html style.css
```

With the files created, open the contents of the directory in VS Code:

```bash
code .
```

Open the `index.html` file and add HTML boilerplate by typing `!` and then hitting the `Tab` key. Then make use of the `style.css` file by adding this line inside the `<head>` tag:

```html
<link rel="stylesheet" href="style.css">
```

Replace the existing `<body>` tag with the following:

```html
<body>
    
<!-- THIS IS A COMMENT -->
<header>
     <h1 id="title">HTML Content!</h1>
     <br />

     <h1>Some other title</h1>
</header>
<main>
    <section></section>
    <figure></figure>
</main>
<footer></footer>

<h2>This is smaller</h2>
<p>This is a paragraph</p>
<strong>This is bold text.</strong>
<h6>This is the smallest header</h6>
<i><strong>This is bold text.</strong></i>
<!-- <br /> -->
<strong>This is <i>italic</i> text.</strong>

<ul>
    <li class="banana">this is a bullet point</li>
    <li class="banana">this is a bullet point</li>
    <li class="banana">this is a bullet point</li>
    <li class="banana">this is a bullet point</li>
    <li class="banana">this is a bullet point</li>
</ul>

<ol>
    <li><span>first</span></li>
    <li>second</li>
    <li>third</li>
    <li>third</li>
</ol>

<button>SUBMIT</button>

<hr />

<a href="https://google.com" target="_blank">Link</a>
<img width="200px" src="https://upload.wikimedia.org/wikipedia/commons/b/bc/Juvenile_Ragdoll.jpg?utm_source=en.wikipedia.org&utm_campaign=index&utm_content=original" alt="This is a cat">

<input type="date">
<img src="" alt="">
<hr>
<div>This is a div!</div><h1>This is an h1!</h1>
<span>I'm a span!</span><button>I'm a button</button>

<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Modi ducimus qui amet, distinctio expedita nisi ex maiores quas placeat accusantium dolor labore, commodi iusto recusandae, provident libero! Nam, commodi nemo?</p>

</body>
```

Open the `index.html` file in your browser.
