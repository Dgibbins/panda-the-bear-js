1.  Change profile picture.
$('img.profile-image').attr('src', 'http://placekitten.com/g/400/400');

1. Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.

$('#left-image img').attr('src', 'http://placekitten.com/g/200/200');

2. Select the heading that says "Panda the Bear" and change it to your own name. (hint: use text())

$('h1').text("Ryan Anderson");

3. Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)

var i = $('#employment .info-title i.icon-suitcase')

$("#employment .info-title ").text("     Employment").prepend(i)


4. Panda the Bear is lying about their skills! Take the "time travel" skill off the page to satisfy your personal sense of justice. Use your googling and docs-skimming skillz to find a jQuery function that will allow you to remove elements from the DOM. (hint: there are multiple ways of doing this, but the parent() function might be useful when it comes to selecting the right element)

$(".bar-default ")[2].remove();
                  OR
$("#time-travel ").parent().remove();

5. Change the colour of the body. (hint: use css())

$('body').css('background-color', 'red');

6. Change the colour used by the highlight class.

$('.highlight').css('background-color', 'yellow');

7. Change the font family of the h1 to 'monospace'.

$('h1').css('font-family', 'monospace');

8. Find a way to select the round icons in the sidebar and then change their colour.

$(".action-icon-bg").css("background-color", "red");

9. Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".

$('form input#name').attr('placeholder', "identify yourself")

10. Change the placeholder attribute of the message field to "state your business"

$('form textarea#message').attr('placeholder', "State your Biznatch").

11. Give the name field a "value" attribute of "your nemesis".

$('form input#name').val("Marry Poppins")

12. Change the value attribute of the email field to "koalathebear@gmail.com".
$('form input#email').val("Pizza")
13. Change the value of the submit button on the contact form to "En garde!".
$('form input#submit').attr("value","En-Garde")

14. Bonus: disable button.
$('form input#submit').attr("disabled",true);

15. Delete  ul
$('ul.bio-info').empty();

Part II

1. That drawing of Pikachu is really cute. Let’s duplicate it using clone() and insert it at the bottom of the page using insertAfter() or appendTo().

$('#right-image').clone().appendTo("section");

2. Wow, that was so satisfying I think we should do it 10 more times. Use a for loop to help you do this.

for (var i = 0; i < 100; i++){$('#right-image').clone().appendTo("section")};


3. Let’s add a message about when the page was las3. t updated. We'll do this by appending a new <li> element to the <ul> in the sidebar (you might need to refresh the page to bring back the list items that we emptied out earlier).

var listItem = document.createElement('li');
undefined
index.html:148 GET https://player.vimeo.com/video/138616931 net::ERR_TIMED_OUT
listItem
<li>​</li>​
var leftSpan = document.createElement('span');
undefined
var lastUpdated = document.createTextNode('Page last updated on');
undefined
leftSpan.appendChild(lastUpdated);
"Page last updated on"

listItem.appendChild(leftSpand);
VM10668:1 Uncaught ReferenceError: leftSpand is not defined
    at <anonymous>:1:22
(anonymous) @ VM10668:1

listItem.appendChild(leftSpan);
<span>​Page last updated on​</span>​

var lastUpdatedDate = document.createTextNode('Jan 1st 1970');
undefined

var rightSpan = document.createElement('span');
undefined

rightSpan.appendChild(lastUpdatedDate);
"Jan 1st 1970"

listItem.appendChild(rightSpan);
<span>​Jan 1st 1970​</span>​

$('ul').append(listItem) to attach it.
