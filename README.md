How to create custom cursor using HTML , CSS & JS

## Method - 1 

https://github.com/BroLetsCodeIt/custom_cursor/assets/113767803/c237780c-3be7-4348-8e33-bd35a0e8c01b

## Method - 2 ( with gsap )

- html
```html
 <div class="movingcursor">
              <button>Play reel</button>
 </div>
```
- css
- 
```css

.page1 .movingcursor{
    position: absolute;
    width: 9vw;
    height: 9vw;
    background-color: #FF5838;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    transform: translate(-50% , -50%);
    /* z-index: 35; */
}
.page1 .movingcursor button{
    color: black;
    background-color: transparent;
    outline: none;
    border: none;
    font-size: 1.2vw;
    font-weight: 600;
    font-family: nb;
}

```

- js
```js
const cursor = document.querySelector('.page1 .movingcursor');
const page1 = document.querySelector('.page1');
page1.addEventListener('mousemove',(e) =>{
   
    // cursor.style.left = e.x + "px";
    // cursor.style.top = e.y + "px";


    gsap.to(cursor,{
        duration:'1',
        x:e.x,
        y:e.y,
        ease:'power2'
    })
})

```
