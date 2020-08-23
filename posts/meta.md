# Meta
##### 2020.08.22

## I made a blog today

I tried to keep the size down, but the code highlighting library turned out to be 8x the size of the markdown parsing library.

This is going to be a template post I guess?

here are some things I can copy paste because I forget markdown on a weekly basis

## things to grab

Wow images
![Image](https://i.ibb.co/VwjgRSf/13.jpg)

And links
[Link](https://rsninja.dev)

And code
```
var post = window.location.search;
    if (post !== "") {
        post = post.substring(6, post.length);
        fetch(`posts/${post}.md`).then(Response => Response.text().then(text => {
            document.body.innerHTML += marked(text);
            [].forEach.call(document.getElementsByTagName("code"),e=>hljs.highlightBlock(e));
            document.body.removeChild(document.getElementById("links"));
        }));
    }
```

`<div style="width: 100%; height: 50px; background-color: #313131;">`

you can use html by the way mr. rsninja
<iframe src="https://rsninja.dev/blog" style="width: 800px;height:600px;"></iframe>