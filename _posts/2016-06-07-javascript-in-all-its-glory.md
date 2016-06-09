---
layout: post 
title: Javascript In All Its Glory
---

Me "It wasn't *my* idea to learn javascript..."

Mentor: "Yes, but Javascript is like herpes, everyone has to deal with it in the end"[^notphp]

## Things to watch out for
After *strenuously* avoiding front-end where possible, I spent from 28th May to about 4th June[^history] crying, and learning CSS by trying to make my website look pretty (and yes, I realise I am miles from being a CSSensei). Then I bit the bullet and decided to do some Javascript[^yavascript]. I spent about 3 days  making [this](https://github.com/scripttease/rainbow-rain/tree/gh-pages) and I think I learnt some things. Mostly what NOT to do. This post enumerates some of the screwups I made along the way.

I have of course, (because I'm a geek who loves to do it functionally) read The Good Parts. But reading TGP is, to making actual stuff do things with Javascript, what dildos are to... yeah.

### Where do you put it in?
So,  if you put it in the head, you have to include on load[^loadjoke]. Seriously though. Where do you put it and why? At first I was putting my Javascript inside `<script></script>` tags, straight into my HTML. And then I spent ages changing perfectly(ahem) good code trying to figure out why nothing was happening. Finally I searched Stackoverflow[^stackoverflow] and found [Why is document.body null in my javascript?](http://stackoverflow.com/questions/9916747/why-is-document-body-null-in-my-javascript) That's when I learned about 'window.onload'.  SO what is window.onload? The first thing I did was to wrap my code in a window.onload handler as suggested. Then I went and read up about where to actually put my javascript...

### You gotta put it right at the end of the body, baby!
It seems, historically a lot of people put their JS in the head tag... And some people (Google web devs) suggest putting it at the END of your HTML page... This might cause loading to be faster BUT your page won't validate if the JS is neither in the head or the body... So if you HAVE to put it in, the best solution seems to be to put it at the end of the body. Extract the actual javascript to a file `myscript.js` put it in the root, and reference it like so in your HTML:

```HTML5
...
<body>
...
    <script src="myscript.js"></script>
  </body>
</html>
```


___
[^loadjoke]: Look, enough bad puns already. Make up your own. 
[^yavascript]: I think it's pronounced YAVAscript? Might be a soft 'j'...
[^stackoverflow]: I just LOVE [Stackoverflow](http://stackoverflow.com/) :purple_heart:
[^notphp]: At least he is a strong advocate of NOT learning PHP. Ever. For any reason. ('There's never a reason')
[^history]: I know the approximate dates because I searched my browser history for 'Stackoverflow'. Seriously. Did I tell you how much I love Stackoverflow?[^stackoverflow]. Yeah.
