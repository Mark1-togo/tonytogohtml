<!-- Video -->
<video controls src="video.mp4">
  <track
    src="captions.vtt" 
    kind="captions"
    srclang="en"
    label="English" 
  />
</video>

<!-- Audio -->
<audio controls src="audio.mp3">
  <track
    src="captions.vtt"
    kind="captions"
    srclang="en"
    label="English"
  />
</audio>

<!-- -- ACCESS KEYS ---- -->
Skip to content
Search 11,800+ news articles, tutorials, and books


Menu
Profile
Certified Full Stack Developer Curriculum
Working with Accessible Media Elements
What Are Some Ways to Make Web Applications Keyboard Accessible?
Watch the video or read the transcript and answer the questions below.


Transcript
What are some ways to make web applications keyboard accessible?

Many users rely on keyboards instead of mice due to physical disabilities, repetitive strain injuries, or personal preference. This includes users of screen readers and those who may not have a working mouse. Keyboard accessibility ensures these users can navigate web applications effectively without barriers.

Let's look at some practical techniques you can employ to make web applications keyboard accessible.

Many users use the Tab key to navigate through interactive elements on a webpage. The tabindex attribute is used to make elements focusable and define the relative order in which they should be navigated using the keyboard. It takes a numerical value, which can be positive, zero, or negative.

Here is the basic syntax:

<element tabindex="number">Element Text</element>
It is important to never use the tabindex attribute with a value greater than 0. Instead, you should either use a value of 0 or -1.

You can set the tabindex to -1 to allow it to receive programmatic focus. This is used in a variety of situations for "focus management", such as when you need to set the focus on a heading, error message, or dialog, or you are building custom components such as tabbing interfaces or tree components.

<p tabindex="-1">Sorry, there was an error with your submission.</p>
Setting tabindex to 0 allows you to add an element that does not receive keyboard focus by default into the page's natural tab order. This allows keyboard users to Tab to the element. This is primarily used when building custom elements that need keyboard functionality.

<div role="combobox" tabindex="0">
accesskey is another attribute you can use to make your web project keyboard accessible. It allows you to define a key that focuses on or activates a particular element:

<button accesskey="s">Save</button>
<button accesskey="c">Cancel</button>
<a href="index.html" accesskey="h">Home</a>
In the above code:

accesskey="s" assigns the key S to the Save button. On most browsers, pressing ALT + S (on Windows) and CTRL + Option + S (on Mac) will activate this button.
accesskey="c" sets the key C to the Cancel button, allowing users to activate it using ALT + C (Windows) and CTRL + Option + C (Mac).
accesskey="h" assigns the key H to the Home link, allowing users to navigate to the homepage using ALT + H (Windows) and CTRL + Option + H (Mac).
Please note that the exact key combination to activate the accesskey might vary depending on the browser and operating system. It's typically ALT + Specified Key on Windows and CTRL + Option + Specified Key on Mac.

Another way to make the keyboard accessible in your apps is to make sure you provide clear focus indicators. If you feel the default browser focus indicator is not enough, you can override it by targeting the focus state of the element.

Here is an example of styling the focus state for an HTML element:

element:focus {
  outline: 2px solid #005fcc;
}
The outline property is used to define the outline around the element. This example sets the outline to a solid blue line with 2 pixels set for the thickness. The focus indicator should be styled in a way that makes it obvious which element currently has focus. In order to be accessible, the indicator must have a minimum color contrast of at least 3:1 with the background color it covers.

You should also avoid keyboard traps, which occur when a user cannot move focus away from a certain element in components like modals and popups.

Questions

Why is the tabindex property important when managing keyboard navigation on a webpage?


It makes the page load faster.

It allows you to control the order in which elements are focused when using the tab key.

It adds animations to focusable elements.

It hides non-essential elements from keyboard navigation.

How does the accesskey attribute contribute to keyboard accessibility on a webpage?


It enhances the visual appearance of the webpage.

It speeds up the loading time of the website.

It allows you to define a specific key that focuses on or activates a particular element.

It automatically generates shortcut keys for all elements.

Why exactly is it important to avoid keyboard traps in web applications?


It improves SEO.

It lets the developer work faster.

It ensures the page has fewer interactive elements.

It ensures users can move focus away from elements like modals and popups.
Check your answer
Ask for Help
Navigated to What Are Some Ways to Make Web Applications Keyboard Accessible?

<!-- HTML Accessibility Review -->

Skip to content
Search 11,800+ news articles, tutorials, and books


Menu
Profile
Saved! Your code was saved to your browser's local storage.Close
×
Certified Full Stack Developer Curriculum
HTML Accessibility Review
HTML Accessibility Review
Introduction to Accessibility
Web Content Accessibility Guidelines: The Web Content Accessibility Guidelines (WCAG) are a set of guidelines for making web content more accessible to people with disabilities. The four principles of WCAG are POUR which stands for Perceivable, Operable, Understandable, and Robust.
Assistive Technology for Accessibility
Screen readers: Software programs that read the content of a computer screen out loud. They are used by people who are blind or visually impaired to access the web.
Large text or braille keyboards: Used by people with visual impairments to access the web.
Screen magnifiers: Software programs that enlarge the content of a computer screen. They are used by people with low vision to access the web.
Alternative pointing devices: Used by people with mobility impairments to access the web. This includes devices such as joysticks, trackballs, and touchpads.
Voice recognition: Used by people with mobility impairments to access the web. It allows users to control a computer using their voice.
Accessibility Auditing Tools
Common Accessibility Tools: Google Lighthouse, Wave, IBM Equal Accessibility Checker, and axe DevTools are some of the common accessibility tools used to audit the accessibility of a website.
Accessibility Best Practices
Proper heading level structure: You should use proper heading levels to create a logical structure for your content. This helps people using assistive technologies understand the content of your website.
Accessibility and Tables: When using tables, you should use the th element to define header cells and the td element to define data cells. This helps people using assistive technologies understand the structure of the table. With the caption element, you can write the caption (or title) of a table, so users, especially those who use assistive technologies, can quickly understand the table's purpose and content. You should place the caption element immediately after the opening tag of the table element. This way, screen readers and other assistive technologies can provide more context by announcing the caption before reading the content.
Importance for inputs to have an associated label: You should use the label element to associate labels with form inputs. This helps people using assistive technologies understand the purpose of the input.
Importance of good alt text: You should use the alt attribute to provide a text alternative for images. This helps people using assistive technologies understand the content of the image.
Importance of good link text: You should use descriptive link text to help users understand the purpose of the link. This helps people using assistive technologies understand the purpose of the link.
Best practices for making audio and video content accessible: You should provide captions and transcripts for audio and video content to make it accessible to people with hearing impairments. You should also provide audio descriptions for video content to make it accessible to people with visual impairments.
tabindex attribute: Used to make elements focusable and define the relative order in which they should be navigated using the keyboard. It is important to never use the tabindex attribute with a value greater than 0. Instead, you should either use a value of 0 or -1. For more information, review the prior lecture video on keyboard accessibility.
<p tabindex="-1">Sorry, there was an error with your submission.</p>
accesskey attribute: Used to define a keyboard shortcut for an element. This can help users with mobility impairments navigate the website more easily.
<button accesskey="s">Save</button>
<button accesskey="c">Cancel</button>
<a href="index.html" accesskey="h">Home</a>
WAI-ARIA, Roles, and Attributes
WAI-ARIA: It stands for Web Accessibility Initiative - Accessible Rich Internet Applications. It is a set of attributes that can be added to HTML elements to improve accessibility. It provides additional information to assistive technologies about the purpose and structure of the content.
ARIA roles: A set of predefined roles that can be added to HTML elements to define their purpose. This helps people using assistive technologies understand the content of the website. Examples include role="tab", role="menu", and role="alert".
There are six main categories of ARIA roles:

Document structure roles: These roles define the overall structure of the web page. With these roles, assistive technologies can understand the relationships between different sections and help users navigate the content.

Widget roles: These roles define the purpose and functionality of interactive elements, like scrollbars.

Landmark roles: These roles classify and label the primary sections of a web page. Screen readers use them to provide convenient navigation to important sections of a page.

Live region roles: These roles define elements with content that will change dynamically. This way, screen readers and other assistive technologies can announce changes to users with visual disabilities.

Window roles: These roles define sub-windows, like pop up modal dialogues. These roles include alertdialog and dialog.

Abstract roles: These roles help organize the document. They're only meant to be used internally by the browser, not by developers, so you should know that they exist but you shouldn't use them on your websites or web applications.

aria-label and aria-labelledby attributes: These attributes are used to give an element a programmatic (or accessible) name, which helps people using assistive technology (such as screen readers) understand the purpose of the element. They are often used when the visual label for an element is an image or symbol rather than text. aria-label allows you to define the name directly in the attribute while aria-labelledby allows you to reference existing text on the page.

<button aria-label="Search">
    <i class="fas fa-search"></i>
</button>
<input type="text" aria-labelledby="search-btn">
<button type="button" id="search-btn">Search</button>
aria-hidden attribute: Used to hide an element from assistive technologies such as screen readers. For example, this can be used to hide decorative images that do not provide any meaningful content.
<button>
    <i class="fa-solid fa-gear" aria-hidden="true"></i>
    <span class="label">Settings</span>
</button>
aria-expanded attribute: Used to convey the state of a toggle (or disclosure) feature to screen reader users.
<button aria-expanded="true">Menu</button>
aria-live attribute: Used to indicate that an element's content is important enough to require that any changes to the content should be announced immediately to screen reader users. This can include status messages like updating the number of results returned from a search, or an error message displayed after an unsuccessful form submission.
<div aria-live="assertive">
    <p>Your session will expire in 30 seconds.</p>
</div>
<div aria-live="polite">
    <p>File successfully uploaded</p>
</div>
Common ARIA states: Common ARIA states include aria-haspopup, aria-checked, aria-disabled, and aria-selected. These attributes can be used to indicate the state of an element and help people using assistive technologies understand the content of the website.
aria-haspopup attribute: This state is used to indicate that an interactive element will trigger a pop-up element when activated. You can only use the aria-haspopup attribute when the pop-up has one of the following roles: menu, listbox, tree, grid, or dialog. The value of aria-haspopup must be either one of these roles or true, which is the same as menu.
<button id="menubutton" aria-haspopup="menu" aria-controls="filemenu" aria-expanded="false">File</button>
<ul id="filemenu" role="menu" aria-labelledby="menubutton" hidden>
  <li role="menuitem" tabindex="-1">Open</li>
  <li role="menuitem" tabindex="-1">New</li>
  <li role="menuitem" tabindex="-1">Save</li>
  <li role="menuitem" tabindex="-1">Delete</li>
</ul>
aria-checked attribute: This attribute is used to indicate whether an element is in the checked state. It is most commonly used when creating custom checkboxes, radio buttons, switches, and listboxes.
<div role="checkbox" aria-checked="true" tabindex="0">Checkbox</div>
aria-disabled attribute: This state is used to indicate that an element is disabled only to people using assistive technologies, such as screen readers.
<div role="button" tabindex="-1" aria-disabled="true">Edit</div>
aria-selected attribute: This state is used to indicate that an element is selected. You can use this state on custom controls like a tabbed interface, a listbox, or a grid.
<div role="tablist">
    <button role="tab" aria-selected="true">Tab 1</button>
    <button role="tab" aria-selected="false">Tab 2</button>
    <button role="tab" aria-selected="false">Tab 3</button>
</div>
aria-controls attribute: Used to associate an element with another element that it controls. This helps people using assistive technologies understand the relationship between the elements.
<div role="tablist">
    <button role="tab" id="tab1" aria-controls="section1" aria-selected="true">
        Tab 1
    </button>
    <button role="tab" id="tab2" aria-controls="section2" aria-selected="false">
        Tab 2
    </button>
    <button role="tab" id="tab3" aria-controls="section3" aria-selected="false">
        Tab 3
    </button>
</div>
aria-describedby attribute: Used to provide additional information about an element by associating it with another element that contains the information. This gives people using screen readers immediate access to the additional information when they navigate to the element. Common usage would include associating formatting instructions to a text input or an error message to an input after an invalid form submission.
<form>
    <label for="password">Password:</label>
    <input type="password" id="password" aria-describedby="password-help" />
    <p id="password-help">Your password must be at least 8 characters long.</p>
</form>
Assignment

Review the HTML Accessibility topics and concepts.

Please complete the assignment
Submit
Ask for Help
Navigated to HTML Accessibility Review

<!-- ------- HTML REVIEWS ------ -->


Skip to content
Search 11,800+ news articles, tutorials, and books


Menu
Profile
Saved! Your code was saved to your browser's local storage.Close
×
Certified Full Stack Developer Curriculum
HTML Review
HTML Review
Review the concepts below to prepare for the upcoming prep exam.

HTML Basics
Role of HTML: HTML (Hypertext Markup Language) is the foundation of web structure, defining the elements of a webpage.
HTML Elements: Used to represent content on the page. Most of them are made by an opening and a closing tag (e.g., <h1></h1>, <p></p>).
HTML Structure: HTML consists of a head and body, where metadata, styles, and content are structured.
Common HTML Elements: Headings (<h1> - <h6>), paragraphs (<p>), and div containers (<div>).
div elements: The div element is a generic HTML element that does not hold any semantic meaning. It is used as a generic container to hold other HTML elements.
Void Elements: Do not have a closing tag (e.g., <img>).
Attributes: Adding metadata and behavior to elements.
Identifiers and Grouping
IDs: Unique element identifiers.
Classes: Grouping elements for styling and behavior.
Special Characters and Linking
HTML entities: Using special characters like &amp; and &lt;.
link element: Linking to external stylesheets.
script element: Embedding external JavaScript files.
Boilerplate and Encoding
HTML boilerplate: Basic structure of a webpage, which includes the DOCTYPE, html, head, and body elements. It should be used as the starting point for an HTML document.
UTF-8 character encoding: Ensuring universal character display.
SEO and Social Sharing
Meta tags (description): Providing a short description for the web page and impacting SEO.
Open Graph tags: Enhancing social media sharing.
Media Elements and Optimization
Replaced elements: Embedded content (e.g., images, iframes).
Optimizing media: Techniques to improve media performance.
Image formats and licenses: Understanding usage rights and types.
SVGs: Scalable vector graphics for sharp visuals.
Multimedia Integration
HTML audio and video elements: Embedding multimedia.
Embedding with <iframe>: Integrating external video content.
Paths and Link Behavior
Target attribute types: Controlling link behavior.
Absolute vs. relative paths: Navigating directories.
Path syntax: Understanding /, ./, ../ for file navigation.
Link states: Managing different link interactions (hover, active).
Importance of Semantic HTML
Structural hierarchy for heading elements: It is important to use the correct heading element to maintain the structural hierarchy of the content. The h1 element is the highest level of heading and the h6 element is the lowest level of heading.
Presentational HTML elements: Elements that define the appearance of content. Ex. the deprecated center, big, and font elements.
Semantic HTML elements: These elements provide meaning to the structure of the content. Examples include:
<header>: Represents introductory content.
<nav>: Contains navigation links.
<article>: Represents self-contained content.
<aside>: Used for sidebars or related content.
<section>: Groups related content within a document.
<footer>: Defines the footer for a section or document.
Semantic HTML Elements
Emphasis (em) element: Marks text that has stress emphasis.
Idiomatic Text (i) element: Used for highlighting alternative voice or mood, idiomatic terms from another language, technical terms, and thoughts.
Strong Importance (strong) element: Marks text that has strong importance.
Bring Attention To (b) element: Used to bring attention to text that is not important for the meaning of the content.
Description List (dl) element: Used to represent a list of term-description groupings.
Description Term (dt) element: Used to represent the term being defined.
Description Details (dd) element: Used to represent the description of the term.
Block Quotation (blockquote) element: Used to represent a section that is quoted from another source.
Inline Quotation (q) element: Used to represent a short inline quotation.
Abbreviation (abbr) element: Used to represent an abbreviation or acronym.
Contact Address (address) element: Used to represent the contact information.
(Date) Time (time) element: Used to represent a date and/or time.
Superscript (sup) element: Used to represent superscript text.
Subscript (sub) element: Used to represent subscript text.
Inline Code (code) element: Used to represent a fragment of computer code.
Unarticulated Annotation (u) element: Used to represent a span of inline text which should be rendered in a way that indicates that it has a non-textual annotation.
Ruby Annotation (ruby) element: Used to represent the text of a ruby annotation.
Strikethrough (s) element: Used to represent content that is no longer accurate or relevant.
HTML Form Elements and Attributes
Forms
form element: Used to create an HTML form for user input.
action attribute: Defines where to send form data.
method attribute: Determines how form data is sent (GET or POST).
Common Input Types:
text, email, password, radio, checkbox, number, date.
action attribute: used to specify the URL where the form data should be sent.
method attribute: used to specify the HTTP method to use when sending the form data. The most common methods are GET and POST.
<form method="value-goes-here" action="url-goes-here">
  <!-- inputs go inside here -->
</form>
input element: used to create an input field for user input.
type attribute: used to specify the type of input field. Ex. text, email, number, radio, checkbox, etc.
placeholder attribute: used to show a hint to the user to show them what to enter in the input field.
value attribute: used to specify the value of the input. If the input has a button type, the value attribute can be used to set the button text.
size attribute: used to define the number of characters that should be visible as the user types into the input.
min attribute: can be used with input types such as number to specify the minimum value allowed in the input field.
max attribute: can be used with input types such as number to specify the maximum value allowed in the input field.
minlength attribute: used to specify the minimum number of characters required in an input field.
maxlength attribute: used to specify the maximum number of characters allowed in an input field.
required attribute: used to specify that an input field must be filled out before submitting the form.
disabled attribute: used to specify that an input field should be disabled.
readonly attribute: used to specify that an input field is read-only.
<!-- Text input -->
<input 
  type="text"
  id="name"
  name="name"
  placeholder="e.g. Quincy Larson"
  size="20"
  minlength="5"
  maxlength="30"
  required
/>

<!-- Number input -->
<input 
  type="number"
  id="quantity"
  name="quantity"
  min="2"
  max="10"
  disabled
/>

<!-- Button -->
<input type="button" value="Show Alert" />
label element: used to create a label for an input field.
for attribute: used to specify which input field the label is for.
Implicit form association: inputs can be associated with labels by wrapping the input field inside the label element.
<form action="">
  <label>
    Full Name:
    <input type="text" />
  </label>
</form>
Explicit form association: inputs can be associated with labels by using the for attribute on the label element.
<form action="">
  <label for="email">Email Address: </label>
  <input type="email" id="email" />
</form>
button element: used to create a clickable button. A button can also have a type attribute, which is used to control the behavior of the button when it is activated. Ex. submit, reset, button.
<button type="button">Show Form</button>
<button type="submit">Submit Form</button>
<button type="reset">Reset Form</button>
fieldset element: used to group related inputs together.
legend element: used to add a caption to describe the group of inputs.
<!-- Radio group -->
<fieldset>
  <legend>Was this your first time at our hotel?</legend>

  <label for="yes-option">Yes</label>
  <input id="yes-option" type="radio" name="hotel-stay" />

  <label for="no-option">No</label>
  <input id="no-option" type="radio" name="hotel-stay" />
</fieldset>

<!-- Checkbox group -->
<fieldset>
  <legend>
    Why did you choose to stay at our hotel? (Check all that apply)
  </legend>

  <label for="location">Location</label>
  <input type="checkbox" id="location" name="location" value="location" />

  <label for="price">Price</label>
  <input type="checkbox" id="price" name="price" value="price" />
</fieldset>
Focused state: this is the state of an input field when it is selected by the user.
Working with HTML Table Elements and Attributes
Table element: used to create an HTML table.
Table Head (thead) element: used to group the header content in an HTML table.
Table Row (tr) element: used to create a row in an HTML table.
Table Header (th) element: used to create a header cell in an HTML table.
Table body (tbody) element: used to group the body content in an HTML table.
Table Data Cell (td) element: used to create a data cell in an HTML table.
Table Foot (tfoot) element: used to group the footer content in an HTML table.
caption element: used to add a title of an HTML table.
colspan attribute: used to specify the number of columns a table cell should span.
<table>
  <caption>Exam Grades</caption>

  <thead>
    <tr>
      <th>Last Name</th>
      <th>First Name</th>
      <th>Grade</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Davis</td>
      <td>Alex</td>
      <td>54</td>
    </tr>

    <tr>
      <td>Doe</td>
      <td>Samantha</td>
      <td>92</td>
    </tr>

    <tr>
      <td>Rodriguez</td>
      <td>Marcus</td>
      <td>88</td>
    </tr>
  </tbody>

  <tfoot>
    <tr>
      <td colspan="2">Average Grade</td>
      <td>78</td>
    </tr>
  </tfoot>
</table>
HTML Tools
HTML validator: A tool that checks the syntax of HTML code to ensure it is valid.
DOM inspector: A tool that allows you to inspect and modify the HTML structure of a web page.
Devtools: A set of web developer tools built directly into the browser that helps you debug, profile, and analyze web pages.
Introduction to Accessibility
Web Content Accessibility Guidelines: The Web Content Accessibility Guidelines (WCAG) are a set of guidelines for making web content more accessible to people with disabilities. The four principles of WCAG are POUR which stands for Perceivable, Operable, Understandable, and Robust.
Assistive Technology for Accessibility
Screen readers: Software programs that read the content of a computer screen out loud. They are used by people who are blind or visually impaired to access the web.
Large text or braille keyboards: Used by people with visual impairments to access the web.
Screen magnifiers: Software programs that enlarge the content of a computer screen. They are used by people with low vision to access the web.
Alternative pointing devices: Used by people with mobility impairments to access the web. This includes devices such as joysticks, trackballs, and touchpads.
Voice recognition: Used by people with mobility impairments to access the web. It allows users to control a computer using their voice.
Accessibility Auditing Tools
Common Accessibility Tools: Google Lighthouse, Wave, IBM Equal Accessibility Checker, and axe DevTools are some of the common accessibility tools used to audit the accessibility of a website.
Accessibility Best Practices
Proper heading level structure: You should use proper heading levels to create a logical structure for your content. This helps assistive technologies understand the content of your website.
Accessibility and Tables: When using tables, you should use the th element to define header cells and the td element to define data cells. This helps assistive technologies understand the structure of the table.
Importance for inputs to have an associated label: You should use the label element to associate labels with form inputs. This helps assistive technologies understand the purpose of the input.
Importance of good alt text: You should use the alt attribute to provide a text alternative for images. This helps assistive technologies understand the content of the image.
Importance of good link text: You should use descriptive link text to help users understand the purpose of the link. This helps assistive technologies understand the purpose of the link.
Best practices for making audio and video content accessible: You should provide captions and transcripts for audio and video content to make it accessible to people with hearing impairments. You should also provide audio descriptions for video content to make it accessible to people with visual impairments.
tabindex attribute: Used to make elements focusable and define the relative order in which they should be navigated using the keyboard. It is important to never use the tabindex attribute with a value greater than 0. Instead, you should either use a value of 0 or -1. For more information, review the prior lecture video on keyboard accessibility.
accesskey attribute: Used to define a keyboard shortcut for an element. This can help users with mobility impairments navigate the website more easily.
WAI-ARIA, Roles, and Attributes
WAI-ARIA: It stands for Web Accessibility Initiative - Accessible Rich Internet Applications. It is a set of attributes that can be added to HTML elements to improve accessibility. It provides additional information to assistive technologies about the purpose and structure of the content.
ARIA roles: A set of predefined roles that can be added to HTML elements to define their purpose. This helps assistive technologies understand the content of the website. Examples include role="tab", role="menu", and role="alert".
aria-label and aria-labelledby attributes: These attributes are used to give an element a programmatic (or accessible) name, which helps assistive technology (such as screen readers) understand the purpose of the element. They are often used when the visual label for an element is an image or symbol rather than text. aria-label allows you to define the name directly in the attribute while aria-labelledby allows you to reference existing text on the page.
aria-hidden attribute: Used to hide an element from assistive technologies such as screen readers. For example, this can be used to hide decorative images that do not provide any meaningful content.
aria-expanded attribute: Used to convey the state of a toggle (or disclosure) feature to screen reader users.
aria-live attribute: Used to indicate that an element's content is important enough to require that any changes to the content should be announced immediately to screen reader users. This can include status messages like updating the number of results returned from a search, or an error message displayed after an unsuccessful form submission.
Common ARIA states: Common ARIA states include aria-haspopup, aria-checked, aria-disabled, and aria-selected. These attributes can be used to indicate the state of an element and help assistive technologies understand the content of the website.
aria-controls attribute: Used to associate an element with another element that it controls. This helps assistive technologies understand the relationship between the elements.
aria-describedby attribute: Used to provide additional information about an element by associating it with another element that contains the information. This helps assistive technologies understand the purpose of the element.
Assignment

Review the HTML topics and concepts.

Please complete the assignment
Submit
Ask for Help
Navigated to HTML Review
