** Question 1
Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.

var profile_image = document.querySelector('.profile-image');
profile_image.src = profile_image.src = 'https://placebear.com/400/400';

** Question 2
Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.

var skyImage = document.querySelector('#left-image.portfolio-image > img');
skyImage.src = 'http://www.vanguarduniversityvoice.com/wp-content/uploads/2016/10/starry-sky-forest-325x225.jpg';

** Question 3
Select the heading that says "Panda the Bear" and change it to your own name.

var title = document.querySelector('h1.highlight');
title.innerText = 'Josh Dales'

** Question 4
Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)

empolymentTitle = document.querySelector('#employment .info-title')
empolymentTitle.innerText = 'Jobs and tings';
