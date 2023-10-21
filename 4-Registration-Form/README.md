# freeCodeCamp - Responsive Web Design - Learn HTML Forms by Creating a Registration Form


## Result
![Registration-Form-Image](Registration-Form.jpg)

## Steps
1. Welcome to the registration form project! Start by adding the !DOCTYPE html declaration at the top of the document
   so the browser knows what type of document it is reading.
   `<!DOCTYPE html>`

2. Below the DOCTYPE, add an html element with a lang attribute set to en
   so you have a place to start putting code.
   `<html lang="en"></html>`

3. Then add the opening and closing head and body tags inside the html element.
```
<head></head>
<body></body>
```

4. Add title and meta elements to head.
   Title the project Registration Form and give the charset attribute a value of UTF-8 for the meta element
```
<title>Registration Form</title>
<meta charset="UTF-8"/>
```

5. Add a self-closing link element to the head element.
   Give it the value of the rel attribute from stylesheet and the value of the href attribute from styles.css.
   `<link rel="stylesheet" href="styles.css"/>`

6. Inside the body, create a title to give context to the content by adding an h1 with the text Registration Form.
   `<h1>Registration Form</h1>`

7. Below the title, use the following text within a paragraph element to encourage users to register:
   `Please fill out this form with the required information`
   `<p>Please fill out this form with the required information</p>`

8. The vh unit means viewport height and is relative to 1% of the viewport height.
   It's time to improve the project with some CSS. Start by giving the body a width of 100%, and a height of 100vh.
```
body {
     width: 100%;
     height: 100vh;
}
```

9. Now, remove the horizontal scrollbar by setting the default body margin, used by some browsers, to 0.
```
body {
     width: 100%;
     height: 100vh;
     margin: 0;
}
```

10. This is better. Now, to make the background more comfortable to see, change the body's background-color to #1b1b32.
    Then, to see the text, change the color to #f5f6f7.
```
body {
     width: 100%;
     height: 100vh;
     margin: 0;
     background-color: #1b1b32;
     color: #f5f6f7;
}
```

11. As suggested by the title, you are creating a form.
    So, after the p element, insert form with an action attribute targeting https://register-demo.freecodecamp.org.
    `<form action="https://register-demo.freecodecamp.org"></form>`

12. The method attribute specifies how to submit form data to the URL specified in the action attribute.
    Form data can be sent via a GET request as URL parameters (with method="get")
    or via a POST request as data in the request body (with method="post").
    Set the method attribute so that it sends the form data through a POST request.
    `<form action='https://register-demo.freecodecamp.org' method="post"></form>`

13. As the form will have three distinct sections, add three fieldset elements within the form element.
    `<fieldset></fieldset><fieldset></fieldset><fieldset></fieldset>`

14. The first fieldset will have fields for name, email and password.
    Start by adding four label elements to the first fieldset.
    `<fieldset><label></label><label></label><label></label><label></label></fieldset>`

15. Add the following texts to the label elements:
```
Enter Your First Name:
Enter Your Last Name:
Enter Your Email:
Create a New Password:
```
```
<fieldset>
     <label>Enter Your First Name:</label>
     <label>Enter Your Last Name:</label>
     <label>Enter Your Email:</label>
     <label>Create a New Password:</label>
</fieldset>
```

16. The rem unit stands for root in and is relative to the font size of the html element.
    Since label elements are inline by default, they will be displayed side by side on the same line,
    making the text difficult to read.
    To make them appear on separate lines, add display: block to the label element
    and add a margin of 0.5rem 0, to separate them from each other.
```
label {
     display: block;
     margin: 0.5rem 0;
}
```

17. Add an input element inside each label element.
    Don't forget to add each input element after the label text and include a space after the colon.
```
<fieldset>
     <label>Enter Your First Name: <input /></label>
     <label>Enter Your Last Name: <input /></label>
     <label>Enter Your Email: <input /></label>
     <label>Create a New Password: <input /></label>
</fieldset>
```

18. Following accessibility best practices, link the input and label elements using the for attribute.
    Use first-name, last-name, email, and new-password as values for the respective id attributes.
```
<fieldset>
     <label for="first-name">Enter Your First Name: <input id="first-name"/></label>
     <label for="last-name">Enter Your Last Name: <input id="last-name"/></label>
     <label for="email">Enter Your Email: <input id="email"/></label>
     <label for="new-password">Create a New Password: <input id="new-password"/></label>
</fieldset>
```

19. Specifying the type attribute of a form element is important for the browser to know what type of data it should expect.
    If type is not specified, the browser defaults to text.
    Give the first two input elements a text type attribute, the third an email type attribute, and the fourth a password type attribute.
    The email type only allows emails with @ and a . in the domain.
    The password type hides the input and warns if the site does not use HTTPS.
```
<fieldset>
     <label for="first-name">Enter Your First Name: <input id="first-name" type="text"/></label>
     <label for="last-name">Enter Your Last Name: <input id="last-name" type="text"/></label>
     <label for="email">Enter Your Email: <input id="email" type="email"/></label>
     <label for="new-password">Create a New Password: <input id="new-password" type="password"/></label>
</fieldset>
```

20. The first input element with the type value of submit is automatically defined so that
    send the closest parent form element.
    To handle form submission, after the last fieldset element,
    add an input element with the type attribute set to submit and the value attribute set to Submit.
    `<input type="submit" value="Submit"/>`

21. At this point, you should be able to submit the form. However, you will notice that not much happens.
    To make the form more interactive, add the required attribute to the input elements in the first fieldset.
    Now, if you try to submit the form without filling in the required fields, you will see an error message.
```
<fieldset>
     <label for="first-name">Enter Your First Name: <input id="first-name" type="text" required/></label>
     <label for="last-name">Enter Your Last Name: <input id="last-name" type="text" required/></label>
     <label for="email">Enter Your Email: <input id="email" type="email" required/></label>
     <label for="new-password">Create a New Password: <input id="new-password" type="password" required/></label>
</fieldset>
```

22. Certain type attribute values come with built-in validation form.
    For example, type="email" requires the value to be a valid email address.
    Add custom validation to the password input element by adding a minlength attribute with a value of 8.
    This prevents entries of less than 8 characters from being sent.
    `<label for="new-password">Create a New Password: <input id="new-password" type="password" required minlength="8"/></label>`

23. With type="password" you can use the pattern attribute to define a regular expression that the password must match to be considered valid.
    Add a pattern attribute to the password input element to require the input to match the values: [a-z0-5]{8,}
    The above command is a regular expression that matches eight or more lowercase letters or the digits 0 through 5.
    Now remove the minlength attribute and try it out.
    `<label for="new-password">Create a New Password: <input id="new-password" type="password" required pattern="[a-z0-5]{8,}"/></ label>`

24. Let's move on to the next part of the registration form.
    This section will ask for the type of account the user is opening.
    Start by adding two label elements to the second fieldset.
```
<fieldset>
   <label></label>
   <label></label>
</fieldset>
```

25. Users will be able to choose a personal account, Personal, or a corporate account, Business.
    To do this, inside the first two label elements, add an input element with type="radio".
```
<fieldset>
     <label><input type="radio"/>/label>
     <label><input type="radio"/></label>
</fieldset>
```

26. Within each label element and immediately after the input element,
    add a space and respectively add the following text:
```
Personal
Business
```
```
<label><input type="radio" /> Personal</label>
<label><input type="radio" /> Business</label>
```

27. Only one radio button input should be selectable at a time.
    However, the form does not know whether the radio button inputs are related.
    To relate radio button entries, give them the same name attribute with a value of account-type.
    Now, you cannot select both radio button inputs at the same time.
```
<label><input type="radio" name="account-type"/> Personal</label>
<label><input type="radio" name="account-type"/> Business</label>
```

28. Currently, when someone submits the form, they can submit it without checking the radio buttons.
    Although you previously used a required attribute to indicate that the input is required,
    this may not work in this case as adding the attribute to both inputs will convey the
    wrong information to form users.
    To resolve this, you can provide the context of what is needed by adding a legend element below
    of the second fieldset with the text Account type (required). Therefore, add the checked attribute to the Personal entry
    to make sure the form is submitted with the required data in it.
```
<fieldset>
     <legend>Account type (required)</legend>
     <label><input type="radio" name="account-type" checked/> Personal</label>
     <label><input type="radio" name="account-type"/> Business</label>
</fieldset>
```

29. Follow accessibility best practices by linking the input and label elements in the second fieldset.
    Use personal-account and business-account as values for the respective id attributes.
```
<fieldset>
     <legend>Account type (required)</legend>
     <label for="personal-account"><input id="personal-account" type="radio" name="account-type" checked/> Personal</label>
     <label for="business-account"><input id="business-account" type="radio" name="account-type"/> Business</label>
</fieldset>
```

30. You need to confirm that the user has read the terms and conditions.
    Add the label element after the third fieldset and an input element with the type attribute with the checkbox value inside the newly added label element.
    Make this input element required, as users should not sign up without reading the terms and conditions.
    Don't forget to add an id attribute to terms-and-conditions to help with accessibility.
    `<label for="terms-and-conditions"><input id="terms-and-conditions" type="checkbox" required/></label>`

31. Add the text I accept the terms and conditions to the newly added label.
    Then, make a link in the terms and conditions text pointing to the following location:
    `https://www.freecodecamp.org/news/terms-of-service/`
```
<label for="terms-and-conditions"><input id="terms-and-conditions" type="checkbox" required/>
     I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a>
</label>
```

32. Now let's make the last fieldset.
    What if you want to allow a user to upload a profile photo?
    Well, the file type input allows this.
    Add a label with the text Upload a profile picture: and insert an input into it that accepts file uploads.
```
<fieldset>
     <label>
         Upload a profile picture:
         <input type="file" />
     </label>
</fieldset>
```

33. Add another label after the first, with the text Input your age (years):. Then, nest an input with the type of number.
    Then add a min attribute to the input with a value of 13, as users under 13 should not register.
    Additionally, users will likely be no older than 120; add a max attribute with a value of 120.
    Now, if someone tries to submit the form with values outside the range, a warning will appear and the form will not be submitted.
    Give it a try.
```
<label>
     Input your age (years):
     <input type="number" min="13" max="120"/>
</label>
```

34. Adding a dropdown list to the form is easy with the select element.
    The select element is a repository for a group of option elements, and the option element functions as a label for each select option.
    Both elements require closing tags.
    Start by adding a select element below the two label elements.
    You must nest 5 option elements inside the select element.
```
<select>
     <option></option>
     <option></option>
     <option></option>
     <option></option>
     <option></option>
</select>
```

35. Nest the select element (with its option elements) inside a label element with the text How did you hear about us?.
    The text must come before the select element.
```
<label>How did you hear about us?
     <select>
         <option></option>
         <option></option>
         <option></option>
         <option></option>
         <option></option>
     </select>
</label>
```

36. The drop-down list options are currently empty.
    To give them content, add the following text to each option element below:
```
(select one)
freeCodeCamp News
freeCodeCamp YouTube Channel
freeCodeCamp Forum
Other
```
```
<label>How did you hear about us?
     <select>
         <option>(select one)</option>
         <option>freeCodeCamp News</option>
         <option>freeCodeCamp YouTube Channel</option>
         <option>freeCodeCamp Forum</option>
         <option>Other</option>
     </select>
</label>
```


37. Submitting a form with an option selected would not send a useful value to the server.
    This way, each option needs to receive a value attribute. Without this, the text content of the option will be sent to the server.
    Give the first option a value of "" and subsequent option elements attributes a value of 1 to 4.
```
<label>How did you hear about us?
     <select>
         <option value="">(select one)</option>
         <option value="1">freeCodeCamp News</option>
         <option value="2">freeCodeCamp YouTube Channel</option>
         <option value="3">freeCodeCamp Forum</option>
         <option value="4">Other</option>
     </select>
</label>
```

38. The textarea element acts like an input element of type text, but comes with the additional benefit of being able to receive text
    across multiple lines and an initial number of rows and columns.
    Users will be able to register with a biography.
    Add a label with the text Provide a bio: at the end of the fieldset.
    Add a textarea element inside the label element.
    Note that the textarea element requires a closing tag.
```
<label>Provide bio:
     <textarea></textarea>
</label>
```

39. Link applicable form elements and label elements.
    Use profile-picture, age, referrer and bio as values for the respective id attributes.
```
<fieldset>
     <label for="profile-picture">
         Upload a profile picture:
         <input type="file" id="profile-picture"/>
     </label>
     <label for="age">
         Input your age (years):
         <input type="number" min="13" max="120" id="age"/>
     </label>
     <label for="referrer">How did you hear about us?
         <select id="referrer">
             <option value="">(select one)</option>
             <option value="1">freeCodeCamp News</option>
             <option value="2">freeCodeCamp YouTube Channel</option>
             <option value="3">freeCodeCamp Forum</option>
             <option value="4">Other</option>
         </select>
     </label>
     <label for="bio">Provide a bio:
         <textarea id="bio"></textarea>
     </label>
</fieldset>
```

40. The textarea is too small.
    To give it an initial size, you can add the rows and cols attributes.
    Add an initial size of 3 rows and 30 columns.
    `<textarea id="bio" rows="3" cols="30"></textarea>`

41. To give Campers an idea of what to put in the bio, the placeholder attribute is used.
    The placeholder accepts a text value, which is displayed until the user starts typing.
    Give the textarea a placeholder of I like coding on the beach....
    `<textarea id="bio" rows="3" cols="30" placeholder="I like coding on the beach...."></textarea>`

42. With form submissions, it is useful and good practice to give each submitted element a name attribute.
    This attribute is used to identify the element upon form submission.
    Give each sendable element a unique name attribute of your choice, except for the two radio inputs (the radio buttons).
```
<fieldset>
     <label for="first-name">Enter Your First Name: <input id="first-name" type="text" name="first-name" required/></label>
     <label for="last-name">Enter Your Last Name: <input id="last-name" type="text" name="last-name" required/></label>
     <label for="email">Enter Your Email: <input id="email" type="email" name="email" required/></label>
     <label for="new-password">Create a New Password: <input id="new-password" type="password" name="new-password" required pattern="[a-z0-5]{8, }"/></label>
</fieldset>
<fieldset>
     <legend>Account type (required)</legend>
     <label for="personal-account"><input id="personal-account" type="radio" name="account-type" checked/> Personal</label>
     <label for="business-account"><input id="business-account" type="radio" name="account-type"/> Business</label>
</fieldset>
<fieldset>
     <label for="profile-picture">
         Upload a profile picture:
         <input type="file" id="profile-picture" name="profile-picture"/>
     </label>
     <label for="age">
         Input your age (years):
         <input type="number" min="13" max="120" id="age" name="age"/>
     </label>
     <label for="referrer">How did you hear about us?
         <select id="referrer" name="referrer">
             <option value="">(select one)</option>
             <option value="1">freeCodeCamp News</option>
             <option value="2">freeCodeCamp YouTube Channel</option>
             <option value="3">freeCodeCamp Forum</option>
             <option value="4">Other</option>
         </select>
     </label>
     <label for="bio">Provide a bio:
         <textarea id="bio" rows="3" cols="30" placeholder="I like coding on the beach...." name="bio"></textarea>
     </label>
</fieldset>
<label for="terms-and-conditions">
     <input id="terms-and-conditions" type="checkbox" name="terms-and-conditions" required/>
     I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a>
</label>
```

43. The HTML for the registration form has been finalized.
    Now, you can tidy it up a bit.
    Start by changing the font to Tahoma and the font size to 16px in the body.
```
body {
     width: 100%;
     height: 100vh;
     margin: 0;
     background-color: #1b1b32;
     color: #f5f6f7;
     font-family: Tahoma;
     font-size: 16px;
}
```

44. Center the h1 and p elements and give them a margin of 1em auto.
    Then also align the text using center.
```
h1, p {
     margin: 1em auto;
     text-align: center;
}
```

45. Center the form element by setting the margin to 0 auto.
    Now, correct the size so that the maximum width is 500px, and the minimum 300px.
    Within that range, make it have a width of 60vw.
```
form {
     margin: 0 auto;
     max-width: 500px;
     min-width: 300px;
     width: 60vw;
}
```

46. During development, it is helpful to see the default fieldset borders.
    However, they make the content appear very separate from each other.
    Remove the border and add 2rem of spacing only at the top and bottom of each fieldset.
    Make sure to remove the left and right padding.
```
fieldset {
     border: none;
     padding: 2rem 0;
}
```

47. To give the fieldset elements a bit of separation,
    select them and give them the border-bottom attribute of 3px solid #3b3b4f.
```
fieldset {
     border: none;
     padding: 2rem 0;
     border-bottom: 3px solid #3b3b4f;
}
```

48. The border of the last fieldset element looks a little out of place.
    You can select the last element of a specific type using the CSS last-of-type pseudo-class, like this:
    `p:last-of-type { }`
    This will select the last element p.
    Create a selector that targets the last fieldset element and set the border-bottom attribute to none.
```
fieldset:last-of-type {
     border-bottom: none;
}
```

49. It would be nicer if the label text was displayed above the form elements.
    Select all input, textarea and select elements, and make them take the entire width of the parent elements.
    Additionally, add 10px margin to the top of the selected elements. Set the other margins to 0.
```
input, textarea, select {
     margin: 10px 0 0 0;
     width: 100%;
}
```

50. For the second fieldset, you want the input and label to appear on the same line.
    Start by giving the input elements in the second fieldset an inline class.
```
<label for="personal-account"><input id="personal-account" type="radio" name="account-type" checked class="inline"/> Personal</label>
<label for="business-account"><input id="business-account" type="radio" name="account-type" class="inline"/> Business</label>
```

51. Select only the .inline elements and give them a width of unset.
    This will remove the previous rule that sets all input elements to width: 100%.
```
.inline {
     width: unset;
}
```

52. Add a little space between the .inline elements and the label text, giving a right margin of 0.5em.
    Set the other margins to 0.
```
.inline {
     width: unset;
     margin: 0 0.5em 0 0;
}
```

53. If you look closely, you will notice that the .inline elements are too high on the line.
    To avoid this, set the vertical-align property to middle.
```
.inline {
     width: unset;
     margin: 0 0.5em 0 0;
     vertical-align: middle;
}
```

54. To make the input and textarea elements blend into the background, set their background-color to #0a0a23.
    Then, give them a 1px border, solid with a color of #0a0a23.
```
input, textarea {
     background-color: #0a0a23;
     border: 1px solid #0a0a23;
}
```

55. Currently, if you type into the input or textarea elements, you cannot see the text.
    Also, their height is very small so they are easy to use.
    Fix this by setting color to #ffffff and setting min-height to 2em.

```
input, textarea {
     background-color: #0a0a23;
     border: 1px solid #0a0a23;
     color: #ffffff;
     min-height: 2em;
}
```

56. You want the select element to remain on a white background,
    but now it is not getting the same min-height as the input and textarea elements.
    Move the min-height property and value so that all three element types have the same min-height value
    and the select element still has a white background.
```
input,
textarea,
select {
   margin: 10px 0 0 0;
   width: 100%;
   min-height: 2em;
}

input, textarea {
   background-color: #0a0a23;
   border: 1px solid #0a0a23;
   color: #ffffff;
}
```

57. To style the submit button, you can use an attribute selector, which selects an element based on the given value.
    Example: `input[name="password"]`
    The code above selects input elements with a name attribute with the value password.
    Now, use the attribute selector to style the submit button with a block display and width of 60%.
```
input[type="submit"] {
     display: block;
     width: 60%
}
```

58. With a block display the send button is on the left edge of the parent element.
    Use the same technique used to center the form to center the submit button.
```
input[type="submit"] {
     display: block;
     width: 60%;
     margin: 0 auto;
}
```

59. To make the submit button look more in line with the rest of the form,
    give it the same height as the other fields (2em).
    Also, increase the font-size to 1.1rem.
```
input[type="submit"] {
     display: block;
     width: 60%;
     margin: 0 auto;
     height: 2em;
     font-size: 1.1rem;
}
```

60. To make the submit button appear more distinct,
    give it a background-color of #3b3b4f and a border-color of white.
```
input[type="submit"] {
     display: block;
     width: 60%;
     margin: 0 auto;
     height: 2em;
     font-size: 1.1rem;
     background-color: #3b3b4f;
     border-color: white;
}
```

61. Lastly, for the submit button, you want to separate it from the fieldset above and
    adjust its width to never be below 300px.
    Change the margin property so that it includes 1em at the top and bottom and at the same time
    Leave the left and right margins set to auto. Then set the width as described above.
```
input[type="submit"] {
     display: block;
     width: 60%;
     margin: 1em auto;
     height: 2em;
     font-size: 1.1rem;
     background-color: #3b3b4f;
     border-color: white;
     min-width: 300px;
}
```

62. Most browsers inject their own default CSS properties and values for different elements.
    If you look closely, you might notice that the file input is smaller than the other text input elements.
    By default, a padding of 1px 2px is given to input elements that you can type on.
    Using another attribute selector, style the input with the file type so that it has the same padding.
    than the other input elements.
```
input[type="file"] {
     padding: 1px 2px;
}
```

63. Speaking of padding, the submit button is at the bottom of the form element.
    Add 2em of padding to the bottom of the form only.
```
form {
     margin: 0 auto;
     max-width: 500px;
     min-width: 300px;
     width: 60vw;
     padding: 2em;
}
```

64. Last but not least, make the input for terms and conditions inline.
    Then, change the color of the link element text, terms and conditions, to #dfdfe2.
    Good job! You have completed the final part of the Registration Form practice project.
```
<input id="terms-and-conditions" type="checkbox" name="terms-and-conditions" required class="inline" />
```
```
a {
     color: #dfdfe2;
}
```


## References
https://www.freecodecamp.org/learn/2022/responsive-web-design/learn-html-forms-by-building-a-registration-form/
, accessed on 10/21/2023.