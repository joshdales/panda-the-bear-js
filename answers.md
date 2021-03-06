# Part 1
## Question 1
Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.

```javascript
var profile_image = document.querySelector('.profile-image');
profile_image.src = profile_image.src = 'https://placebear.com/400/400';
```

## Question 2
Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.

```javascript
var skyImage = document.querySelector('#left-image.portfolio-image > img');
skyImage.src = 'http://www.vanguarduniversityvoice.com/wp-content/uploads/2016/10/starry-sky-forest-325x225.jpg';
```


## Question 3
Select the heading that says "Panda the Bear" and change it to your own name.

```javascript
var title = document.querySelector('h1.highlight');
title.innerText = 'Josh Dales'
```


## Question 4
Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)

```javascript
empolymentTitle = document.querySelector('#employment .info-title');
empolymentTitle.innerText = 'Jobs and tings';
```


## Question 5
Change the colour of the body.

```javascript
var body = document.querySelector('body');
body.style.background = 'cadetblue';
```


## Question 6
Change the colour of each element using the highlight class. Use a for loop to do this.

```javascript
var highlight = document.querySelectorAll('.highlight');
highlight.forEach(function(element) {
    element.style.color = 'black';
})
```


## Question 7
Change the font family of the h1 to 'monospace'.

```javascript
var h1 = document.querySelector('h1');
h1.style.fontFamily = 'monospace';
```


## Question 8
Find a way to select the round icons in the sidebar and then change their colour.

```javascript
var roundIcons = document.querySelectorAll('.action-icon-bg');
roundIcons.forEach(function(icon){
    icon.style.background = 'green';
});
```


## Question 9
Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".

```javascript
var nameField = document.querySelector('input#name.contact-info');
nameField.placeholder = 'Identify Yourself';
```


## Question 10
Change the placeholder attribute of the message field to "state your business".

```javascript
var message = document.querySelector('textarea#message');
message.placeholder = 'State your business';
```


## Question 11
Give the name field a "value" attribute of "your nemesis".

```javascript
nameField.value = 'Your Nemesis';
```

## Question 12
Change the value attribute of the email field to "koalathebear@gmail.com".

```javascript
var emailField = document.querySelector('input#email.contact-info');
emailField.value = 'koalathebear@gmail.com';
```

## Question 13
Change the value of the submit button on the contact form to "En garde!".

```javascript
var submitButton = document.querySelector('input#submit');
submitButton.value = 'En garde!';
```

## Question 14
We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).

```javascript
submitButton.disabled = true;
```

## Question 15
We should help Panda protect their privacy by erasing their personal details from the sidebar.

```javascript
var bio = document.querySelector('.bio-info');
var bioInfo = document.querySelectorAll('.bio-info-value');
bioInfo.forEach(function(info) {
  info.innerText = '';
});
```


# Part 2
## Question 1
Panda the Bear is lying about their skills! Take the "time travel" skill off the page to satisfy your personal sense of justice. Use your googling and docs-skimming skillz to find a jQuery function that will allow you to remove elements from the DOM. (hint: there are multiple ways of doing this, but the parent() function might be useful when it comes to selecting the right element)

```javascript
var barDefault = document.querySelectorAll('.bar-default');
var TimeTravel = barDefault.forEach(function(bar) {
    if (document.querySelector('#time-travel')) {
        return bar}
      }
    );
barDefault[2].removeChild(timeTravel);
```

## Question 2
That drawing of Pikachu is really cute. Let’s duplicate it using cloneNode() and insert it at the bottom of the .portfolio-container using insertAdjacentHTML() or appendChild().

```javascript
var pikaImage = document.querySelector('#right-image.portfolio-image > img');
var portfolioContainer = document.querySelector('.portfolio-container');
var clonePika = pikaImage.cloneNode();
portfolioContainer.appendChild(clonePika);
```
## Question 3
Wow, that was so satisfying I think we should do it 10 more times. Use a for loop to help you do this.

```javascript
for (var i = 0; i <= 10; i++) {
    portfolioContainer.appendChild( pikaImage.cloneNode() ) };
```

## Question 4
Let’s add a message about when the page was last updated. We'll do this by appending a new <li> element to the <ul> in the sidebar (you might need to refresh the page to bring back the list items that we emptied out earlier).

```javascript
var newListItem = document.createElement('li');
newListItem.className += 'bio-info-item';
var leftSpan = document.createElement('span');
leftSpan.className += 'bio-info-title';
var lastUpdated = document.createTextNode('Page Last Updated on');
var rightSpan = document.createElement('span');
rightSpan.className += 'bio-info-value';
var updatedText = document.createTextNode(new Date());
leftSpan.appendChild(lastUpdated);
rightSpan.appendChild(updatedText);
newListItem.appendChild(leftSpan);
newListItem.appendChild(rightSpan);
var bioInfo = document.querySelector('.bio-info');
bioInfo.appendChild(newListItem);

```
