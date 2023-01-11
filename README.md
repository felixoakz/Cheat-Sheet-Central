# Cheat Sheet Central 1.0
#### Video Demo:  <URL https://youtu.be/5lMlsBnLndo>
#### Description:

###### Intro:
Learning a new thing can often be overwhelming due to the amount of information we need to absorb. This is especially true when it comes to learning the various tools and technologies we need to master in order to build bigger projects.

###### What is it:
I have created a web application that displays a simple, practical table of cheat sheets for various technologies. The application is designed for quick reference when it comes to finding code snippets or learning keyboard shortcuts for different tools.

The web application is designed to be multi-language and fast-rendering, so that people from all around the world can use it. It requires no login or session, and the goal is to help users identify the most important commands and gradually learn and use them until they become natural. This way, we can save time and energy for what really matters.

###### The idea:
The idea for this project came to me while I was learning a variety of technologies during my CS50 course. I found it overwhelming to have to memorize commands for the terminal, keyboard shortcuts for VSCode, and syntax for languages like Python, JS, HTML, and CSS, not to mention various other technologies like Jinja. I noticed that this was a common problem when I saw many scattered JPEG and PNG files on the internet with cheat sheets for different technologies. I thought it would be great to have a single page on the web where we could consult all of these cheat sheets instead of wasting time searching for help everywhere.

I confirmed that this was a common practice among developers when I saw my professor, David, constantly checking his own cheat sheet for writing HTML viewport meta tags. He told me that it was okay, and that nobody can possibly memorize everything because technologies are always changing and new ones are constantly appearing. We need to use our heads as processors, not hard drives.

###### The execution:
The web application is a better-constructed version of a previous project I created called "homepage." This time, I used a Flask controller and only three HTML templates instead of creating the page statically with just HTML and CSS. The application has a layout template, an index template, and a sheet template. The Flask engine controller has a single route that takes input from the selected technology via POST from the index page, and then renders the corresponding cheat sheet on the sheet template within a table. The controller queries a server-side SQL database with the necessary data based on the user's selection, and stores it in a variable to be rendered on the client-side on the sheet template. The queries use question mark-bound parameters to prevent SQL injection attacks, even though the application does not currently receive user input.

The layout template has a navbar that works well on any display. It shrinks on mobile devices for better visibility and is rendered on all templates for easy access from any page. It also includes a link to the repository for anyone who wants to check out the code.
I opted to use as little JavaScript as possible to ensure that the page runs quickly and efficiently on any device and internet connection. The only JavaScript snippet I used is for a Google Translator API, which allows the user to translate the index page and site description live. This was a useful addition because the application is intended for a global audience.

###### Conclusion:
In conclusion, the web application I created is a simple, practical tool for quickly referencing cheat sheets for various technologies. It is designed to be multi-language and fast-rendering, and requires no login or session. The goal is to help users identify the most important commands and gradually learn and use them until they become natural, saving time and energy for what really matters.
