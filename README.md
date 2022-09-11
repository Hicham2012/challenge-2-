# Product preview card component

Another simple HTML and CSS work, feel free to use it on your webpage or any other personal use

## Welcome 🤗
I wanna thank you firstly for checking on my humble work. If you find any issue, please feel free to correct me.

## equipements 🤓
Here is what I used to make the webpage:
| Editor | Languages | Frameworks |
| --- | ---| --- |
| [Vs code](https://code.visualstudio.com/)| Vanilla HTML and CSS | None|

I beleive you can use any text editor to make this, [Replit](https://replit.com/~) for example...

## Code 🧐
For the code, all you need to remember is that **HTML is used to structure** while **CSS is used to style**. And the way to display them can be different from each person.
Here is the HTML code I made for this one

```html
<body>
    <main>

        <img src="/images/image-product-desktop.jpg" width="323px" alt="product" class="desktop">
        <img src="/images/image-product-mobile.jpg" class="mobile" width="323px">

        <div class="description">
            <h3>PERFUME</h3>

            <h2>Gabrielle Essence Eau De Parfum</h2>

            <p class="p-1">A floral, solar and voluptuous interpretation composed by Olivier Polge, Perfumer-Creator for the House of CHANEL.</p>
            <div class="prices">
                <p class="p-2">$149.99</p>
                <p class="p-3"><s>$169.99</s></p>
            </div>
            <button><img src="/images/icon-cart.svg" alt="cart">&nbsp;Add to Cart</button>
        </div>

    </main>

    <div class="attribution">
        Challenge by &nbsp;<a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. Coded by &nbsp;&nbsp;<a href="https://www.frontendmentor.io/profile/Hicham2012" target="_blank">Hicham ZAADLA</a>.
    </div>
</body>
```
### Notice here that we added two picture, one for desktop and one for the mobile and we did give them different classes
```html
        <img src="/images/image-product-desktop.jpg" width="323px" alt="product" class="desktop">
        <img src="/images/image-product-mobile.jpg" class="mobile" width="323px">
```
Let's look into the CSS to see why it will come in handy, and how we will display them 🧐
```css
@import url('https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,700&family=Montserrat:wght@500;700&display=swap');
body {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: hsl(30, 38%, 92%);
}

main {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: row;
    height: 100vh;
    width: 95vh;
    margin-bottom: 0px;
}

.mobile {
    display: none;
}

.desktop {
    border-radius: 10px 0 0 10px;
    box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 4px;
}

.description {
    background: hsl(0, 0%, 100%);
    /* border: 5px solid blue; */
    display: flex;
    flex-direction: column;
    text-align: left;
    height: 485px;
    width: 320px;
    border-radius: 0px 10px 10px 0;
    box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 4px;
}


/***********\
    Texts
\***********/

h3 {
    /* border: 2px solid green; */
    margin-left: 30px;
    letter-spacing: 5px;
    font-family: 'Montserrat';
    font-weight: 500;
    font-size: 13px;
    color: hsl(228, 12%, 48%);
}

h2 {
    /* border: 2px solid purple; */
    margin-left: 30px;
    margin-right: 40px;
    margin-top: 0;
    margin-bottom: 10px;
    font-family: 'Fraunces';
    font-weight: 700;
    font-size: 40px;
    color: hsl(212, 21%, 14%);
}

.p-1 {
    /* border: 2px solid red; */
    margin-left: 30px;
    margin-top: 0;
    margin-right: 68px;
    font-family: sans-serif;
    font-weight: 400;
    font-size: 18px;
    color: hsl(228, 12%, 48%);
    margin-bottom: 0;
}

.prices {
    /* border: 2px solid yellow; */
    display: flex;
    flex-direction: row;
    width: 50px;
    gap: 50px;
    margin-left: 30px;
    margin-top: 0;
    margin-bottom: -15px;
}

.p-2 {
    /* border: 2px solid orange; */
    font-family: 'Fraunces';
    font-weight: 700;
    font-size: 35px;
    color: hsl(126, 42%, 38%);
    margin-top: 18px;
}

.p-3 {
    /* border: 2px solid orchid; */
    margin-top: 50px;
    margin-left: -35px;
    font-family: sans-serif;
    color: hsl(228, 12%, 48%);
    margin-top: 31px;
    margin-bottom: 35px;
}

button {
    margin-left: 30px;
    margin-right: 50px;
    height: 47px;
    border-radius: 8px;
    background: hsl(126, 42%, 38%);
    font-family: sans-serif;
    font-size: 15px;
    font-weight: 700;
    color: white;
    border: hsl(126, 42%, 38%);
    margin-top: 0;
    margin-bottom: 0;
    cursor: pointer;
}

button:active {
    background: hsl(212, 21%, 14%);
    transition: 5ms;
}

.attribution {
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    margin-top: 0px;
    color: gray;
    font-size: 12px;
    font-family: sans-serif;
    text-decoration: none;
}

.attribution a {
    color: rgb(66, 39, 39);
    text-decoration: none;
}


/************\
  Mobile-view
\************/

@media only screen and (max-width: 375px) {
    body {
        width: auto;
    }
    main {
        display: contents;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height: auto;
        width: 50px;
    }
    .desktop {
        display: none;
    }
    .mobile {
        display: flex;
        flex-direction: column;
        height: 240px;
        border-radius: 10px 10px 0 0;
    }
    .description {
        border-radius: 0 0 10px 10px;
    }
    .attribution {
        margin-top: 40px;
    }
}
```
You can see that we made the mobile picture display to none, while the desktop picture will apear, and then switched it when the max-width is 375px for phone screens by using @media

## Shoutout 🙏
I wanna thank [frontend Mentor](www.frontendmentor.io) for making funny challenges.
Big thanks to the feedbacks I received on my first challenge!!

  ### Again, please feel free to correct me if I made any issue 🙌
