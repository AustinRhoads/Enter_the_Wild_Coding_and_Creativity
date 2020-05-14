# Creativity: 
![Image](https://github.com/AustinRhoads/Enter_the_Wild_Coding_and_Creativity/blob/master/maples_guadalupe_nps.jpg)
## The red leaf maple forest in Guadalupe National Park, TX

When I think of creativity, immediatly the french painter Jean Giraud, "Moebius", pops into my head. His work is other worldly and extremely imaginitive as is evident in his costume and set design of the movie _The Fifth Element_. Most people dont associate creativity with a technical skill such as coding. However, creativity and critical thinking have always gone hand in hand. Simply observe the work of any great artist to see the fruits of great technical skill coupled with personal vision. As a newb entering into the world of coding, I am pleased to find many opportunities to get creative and I decided to make an app that connects people with the beauty of novel places such as the maple forest of Guadalupe National Park.

Problem solving is a great springboard for creativity. The harder the problem the more deeply we can look into the critical nature of what we are trying to accomplish. This pushes us to learn new things and to innovate.

My first real portfolio project is a Ruby CLI app called find-a-park-cli. This app allows users to search by state and by activity to view a matching list of national parks. It's an excorcise in object oriented programming. All data is parsed from the National Parks website by using the Nokogiri gem. Throughout the process of building this app I was able to learn new things and explore alternitive ways to solve problems. My first big problem came very unexpectedly.

 

# Nokogiri: 
## Ice fishing in Lake Clark, Ak 
Nokogiri is a Ruby gem used to parse files such as HTML. It's name comes from the Japanese fine toothed saw (BTW I happen to own one and any woodworkers out there should try it if given the chance. Clean, narrow cuts and some have both crosscut and ripsaw on either side of the blade! Super cool :) Anywho...) Thus far I could find what I was looking for by a simple two part process. First inspect the page and find the element with the selector tool and then do a bit of fishing until you return the desired data. I thought this was going to be the easiest part of the process. And it was, at first... 

The National Parks website I was to scrape had a form of selectable elements, such as, the state and the activity to filter the search results. Scraping the state and activity names went by quickly and soon after I pulled the URL associated with each search result. I searched Alaska and fishing. One of the results was Lake Clark. I knew If I could pull the text "Lake Clark" the rest of the data would come quickly. However this didn't happen. I played around with selecting the parent elements by ID, by class name and nothing worked. Eventually I printed all the XML nodes searching for the string "Lake CLark" but it was nowhere to be found. I love problem solving but I admit this was a _bit_ frustrating so I decided to take a break and take on a problem I knew I could solve, a sudoku puzzle.

What I love about sudoku is that all the answers you need are already there waiting to be discovered. I was thinking about this when I remembered something I had learned how to do with javascript, class toggle.
Basically, class toggle works like this... say you have a list of _park_ objects. You give each _park_ the class name "unselected". Elements would only be displayed on the HTML if they have a "selected" class. What toggle does is switches the class name from "unselected" to "selected" or visa versa to display or not display a _park_. This meant that somewhere on that page was data on every single park. I inspected the site's sources and sure enough I found a Json file with every single park listed with all activities and states associated with the park! I didn't know a thing about Json but it didn't matter. I could parse everything I needed from the text of this file. All the answers I needed were in one place waiting to be discovered.
Often creativity is the product of gaining a new perspective. Never underestimate the power of taking breaks.

# Object Oriented Programming:
## Spring time in Death Valley, CA
At this point, my app had the data it needed but other than that it was as baren as a desert. I had to start building objects.
Essentially, everything in Ruby is an object. From strings and integers to class instances and even class itself. An object is how we define talking about a thing. It is also a function, it defines how it interacts with other things. Objects are like creatures in an ecosystem that interact and grow with each other. A state is not only a name and abbreviation, "California, CA", but also in this context a state can have many parks, multiple states can have access to those parks, and there should never be more than one state with the same name. However, the state itself is not equal to it's name. A state is a state and any instance of a state or a park should reflect a real state or park as much as possible. I believe this to be an important distinction in OOP as it's concievable that a park could change it's name and in theory this should be the same instance of a park object. Another example would be if two different parks went by the same basic name and had the same genreal location ( which is the case for Natchez Trace scenic trail and Natchez Trace parkway in Alabama). If an object was defined soley by it's name many parks would not be created in an attempt to control redundancy. What this tells me is that as much as I try to make the state class like a real state it will always be an artifact designed by me to serve my purpose, and so I must always keep this in mind as im writing code.
In my case I can use the url as the control factor. No two parks even with the same name should ever have the same URL.


# conclusion: 
## Summer somewhere, SW
Creativity comes from solving big problems. Hitting a wall is the best oppotunity to to let your imagination explore its inventiveness.
## Welcome to GitHub Pages



### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/AustinRhoads/Enter_the_Wild_Coding_and_Creativity/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
