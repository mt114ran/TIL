# Use Intersection Observer API

> How to use the [Intersection Observer API](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API) for multiple elements.<br>
> I have written the code on [CodePen](https://codepen.io/mt114ran/pen/QWZezRG), so if you have time, please try it out and see how it works.

---

First, implement the card elements in HTML. Style them using Tailwind.

```html
<div class="main transition-colors bg-slate-500/25 flex flex-col md:flex">
<h1 class="text-5xl mt-20 text-center font-extrabold">Test Intersection Observer API<br>↓</h1>
	<div class="card rounded-3xl my-40 mx-auto top-1/2 left-1/2 text-white font-bold bg-red-400 h-screen flex justify-center items-center w-60 shadow-xl">
		Red card
	</div>
	<div class="card rounded-3xl my-40 mx-auto top-1/2 left-1/2 text-white font-bold bg-orange-400 h-screen flex justify-center items-center w-60 shadow-xl">
		Orange card
	</div>
	<div class="card rounded-3xl my-40 mx-auto top-1/2 left-1/2 text-white font-bold bg-green-400 h-screen flex justify-center items-center w-60 shadow-xl">
		Green card
	</div>
  	<div class="card rounded-3xl my-40 mx-auto top-1/2 left-1/2 text-white font-bold bg-blue-400 h-screen flex justify-center items-center w-60 shadow-xl">
		Blue card
	</div>
  	<div class="card rounded-3xl my-40 mx-auto top-1/2 left-1/2 text-white font-bold bg-pink-400 h-screen flex justify-center items-center w-60 shadow-xl">
		Pink card
	</div>
</div>
```

Next, we will implement the logic using the Intersection Observer API to change the background color based on the displayed card's color.The key points are how to configure the Intersection Observer to observe multiple elements and how to implement separate logic for each element:

```javascript
const cards = document.querySelectorAll('.card');
const options = {
  root: null,
  rootMargin: "-50% 0px",
  threshold: 0
};

const observer = new IntersectionObserver(callback, options);

cards.forEach(card => {
  observer.observe(card);
});

function callback(entries) {
  entries.forEach(entry => {
    if (entry.isIntersecting ) {
      const targetStyleList = Object.values(entry.target.classList);
      const filteredArray = targetStyleList.filter(element => element.includes('bg-'));
      const targetColor = filteredArray[0];
      const replaceStr = targetColor.replace('400','300/50');

      const mainElement = document.querySelector(".main");
      const regex = /bg-.*/g;
      mainElement.classList.forEach(className => {
        if (regex.test(className)) {
          mainElement.classList.remove(className);
          mainElement.classList.add(replaceStr);
        }
      })
    }
  });
}

```

I explain it in more detail on [my personal blog](https://m-tomoya.org/how-to-intersection-observer-api/).

*2023.6.5*
