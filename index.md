# Morphtoken
An ERC721 token that adds interoperability between collectible applications. A Morphtoken is a generic and unique crypto asset which can be used to in many different collectible games.

<img src="morphtoken.png " width="120" />

## Introduction

### What does interoperability mean?
Multiple different collectible games, services, trackers, and apps can use Morphtoken such that each token is a different collectible in each respective application, owned by a single user. More on why this is useful later.

### Why?
The goal is to make it easier, cheaper, more fun, to launch and use crypto collectable projects.

### What's with the barebones website?
Morphtoken is as simple as possible, so is the documentation and website.

***

## Specs

### White Paper
Coming very soon.

### Genes
Each Morphtoken has a gene which can used to determine how it is represented in different applications. Each gene is made up of:

- A 'Counter variable' which is the unique number for the order the assets were created in. The first Morphtoken 'Counter variable' is 1; the last is 10,000,000.
- 3 'Boolean variables' represented as a 1 or 0.
- A 'DNA sequence' represented as an 18 digit long number.
- A 'P variable' represented as a number between 1 and 100.



***

## Distribution
This is still under consideration. We want to give away as many Morphtokens as possible to members of the Ethereum and Crypto community so that more people will be inspired to more easily create applications with unique crypto items.

We are still figuring out the best way to do that.

***

# Examples

What if every professional athlete played in every sports league? If you owned the baseball card for pitcher Joe Schmoe you could also use it as the basketball card for point-guard Joe Schmoe.  That's what we're going for here.

## Simple specific individual use case  

A Morphtoken has a unique ID, for example **123123123**.  

An app could use this coin to to represent a soldier in a strategy game.  The soldiers strength could be represented as the first 4 digits of the ID divided by 9, and its defense represented by rest of the ID divided by 10.  Using modulus will work better here than division but for simplicity we chose division.

Now the owner of that Morphtoken has a unique solder in that app with **136** strength and **2312** health in that application.

## Interoperability use example

**App A** : Every token is represented by a shape. Even number IDs are squares. Odd number IDs are triangles, unless the ID ends in 999, in which case the token represents a circle. Circles are rare.

**App B** : Every token is a color represented by the last 6 digits of the ID.  

If a user owns the Morphtoken with ID **888123888** they own it in both apps A and B.  In app A it is a common (1/2 chance) square. In app B the Morphtoken is represented by a random color.

If a user owns the Morphtoken with ID **999123999** they own it in both apps A and B.  In app A it is a rare (1/1000 chance) circle, where as in App B is it a regular random color with the same probability as any other.

Trading colors in App B becomes especially interesting when there is a chance that the Morphtoken up for trade is a rare shape in App A, or some other app in the ecosystem.

***

## Contact
This is an idea by Joseph Schiarizzi. Find me here:  
[twitter](https://twitter.com/cupojoseph)  
[email](mailto:jschiarizzi@gmail.com)
[personal portfolio](http://josephschiarizzi.com)

Let us know if you have questions or have used Morphtoken in your application.

<!-- Some HTML for a crypto donation bin-->
## Donation Bin

<style>

.donate-crypto-box {
  display: flex;
  align-items: center;
  width: 100%;
  padding: 1em;
  box-sizing: border-box;
  -webkit-user-select: none;
     -moz-user-select: none;
      -ms-user-select: none;
          user-select: none;
  cursor: text;
}

.coin {
  display: inline-block;
  position: relative;
  min-width: 3em;
  min-height: 3em;
  -webkit-animation: spin 3s cubic-bezier(0.3, 2, 0.4, 0.8) infinite both;
          animation: spin 3s cubic-bezier(0.3, 2, 0.4, 0.8) infinite both;
  -webkit-transform-style: preserve-3d;
          transform-style: preserve-3d;
  vertical-align: middle;
}
@-webkit-keyframes spin {
  0%, 10% {
    -webkit-transform: rotate(-10deg) perspective(400px);
            transform: rotate(-10deg) perspective(400px);
  }
  90%, 100% {
    -webkit-transform: rotate(-10deg) perspective(400px) rotateY(180deg);
            transform: rotate(-10deg) perspective(400px) rotateY(180deg);
  }
}
@keyframes spin {
  0%, 10% {
    -webkit-transform: rotate(-10deg) perspective(400px);
            transform: rotate(-10deg) perspective(400px);
  }
  90%, 100% {
    -webkit-transform: rotate(-10deg) perspective(400px) rotateY(180deg);
            transform: rotate(-10deg) perspective(400px) rotateY(180deg);
  }
}
.coin-face {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  border-radius: 50%;
}
.coin-face:nth-child(1) {
  -webkit-transform: translateZ(-0.2em) rotateY(-180deg);
          transform: translateZ(-0.2em) rotateY(-180deg);
}
.coin-face:nth-child(2) {
  -webkit-transform: translateZ(-0.1em);
          transform: translateZ(-0.1em);
}
.coin-face:nth-child(4) {
  -webkit-transform: translateZ(0.1em);
          transform: translateZ(0.1em);
}
.coin-face:nth-child(5) {
  -webkit-transform: translateZ(0.2em);
          transform: translateZ(0.2em);
}
.coin-face svg {
  width: 100%;
  height: 100%;
}

.coin-address {
  flex: 1;
  font: .7em/2.5 Monaco, monospace;
  text-align: center;
  margin-left: 1em;
  border-width: 0 0 2px;
  border-color: rgba(0, 0, 0, 0.1);
  transition: border-color .3s;
  cursor: text;
}
.coin-address:hover {
  transition-duration: .1s;
}


.eth {
  max-width: 23em;
}
.eth .coin-face {
  background: shade(#6F7CBA, 35%);
}
.eth .coin-face:nth-child(1), .eth .coin-face:nth-child(5) {
  background: #6F7CBA;
}
.eth .coin-address:hover, .eth .coin-address:focus {
  border-color: #6F7CBA;
}

body {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  font-size: 4vmin;
}

.donate-crypto-box:nth-child(1) .coin {
  -webkit-animation-delay: 0.2s;
          animation-delay: 0.2s;
}

.donate-crypto-box:nth-child(2) .coin {
  -webkit-animation-delay: 0.4s;
          animation-delay: 0.4s;
}

.donate-crypto-box:nth-child(3) .coin {
  -webkit-animation-delay: 0.6s;
          animation-delay: 0.6s;
}

</style>


<label class="eth donate-crypto-box">
  <div class="coin">
    <div class="coin-face">
      <svg height="10" viewbox="0 0 32 32" width="10" xmlns="http://www.w3.org/2000/svg">
        <path d="M10.13 17.76c-.1-.15-.06-.2.09-.12l5.49 3.09c.15.08.4.08.56 0l5.58-3.08c.16-.08.2-.03.1.11L16.2 25.9c-.1.15-.28.15-.38 0l-5.7-8.13zm.04-2.03a.3.3 0 0 1-.13-.42l5.74-9.2c.1-.15.25-.15.34 0l5.77 9.19c.1.14.05.33-.12.41l-5.5 2.78a.73.73 0 0 1-.6 0l-5.5-2.76z" fill="#FFF">
        </path>
      </svg>
    </div>
    <div class="coin-face"></div>
    <div class="coin-face"></div>
    <div class="coin-face"></div>
    <div class="coin-face">
      <svg height="8" viewbox="0 0 32 32" width="8" xmlns="http://www.w3.org/2000/svg">
        <path d="M10.13 17.76c-.1-.15-.06-.2.09-.12l5.49 3.09c.15.08.4.08.56 0l5.58-3.08c.16-.08.2-.03.1.11L16.2 25.9c-.1.15-.28.15-.38 0l-5.7-8.13zm.04-2.03a.3.3 0 0 1-.13-.42l5.74-9.2c.1-.15.25-.15.34 0l5.77 9.19c.1.14.05.33-.12.41l-5.5 2.78a.73.73 0 0 1-.6 0l-5.5-2.76z" fill="#fff">
        </path>
      </svg>
    </div>
  </div>
  <input class="coin-address" onclick="this.select()" readonly="readonly" spellcheck="false" type="text" value="0xF4EbAbA0445a21B35f9Bdd919DCC967a30BE83CB" />
  </label>
