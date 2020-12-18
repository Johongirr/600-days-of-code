# Johongir

## 100 Days of Code

### Day 1: Dec 4, 2020

#### Introduction
So actually I've started 600 days of code challenge for about 2 weeks and I'm also starting to keep journal of my progress each day. I'm going to write about what new I've learned today and what were the challenges that i could solve. So hopefully this challenge keeps me accounted for the upcoming NOWS. So let's rock it

#### What I've learned so far
So i've learned algorithms, memory, and nowdays I'm learning data structures and today i've learned about singly linked lists


### Day 2: Dec 5, 2020

#### Things I've learned
Today I've learned about Doubly Linked List Which data structure that consists of Nodes And Each node in the list connected with each other via pointers(links, references) unlike Singly Linked List, nodes in DLL has knows address of both node next to it and node before it.

#### Advantages of DLL over SLL
While removing last node is O(n) in DLL it is constant because of nodes in DLL has previous and next pointers but in SLL has only next pointer which points node after it, so you can just make second to last node tail which is constant time O(1)

You can loop through both forward and backwards in DLL but in only left to right 

#### Disadvantages of DLL over SLL
As nodes in DLL use two pointers and data while in SLL only uses data and a single pointer, that's why DLL require more memory than SLL

#### Resource
I've been learning Algorithms and Data Structures Which is the course of Colt Steele. And I'm very satisfied with his course for it contains not only theortical explanations of topics but also practical exercies


### Day 3: Dec 6, 2020

#### Things I've Learned
 * Stacks and Queues
 * Trees/Binary Trees/Binary Search Trees
 
 
#### Stacks
Stack is FILO(first-in-last-out) and LIFO(last-in-first-out) data structure. It stores called functions and it has finite storage when functions keep being called error is thrown "Maximum Call stack size exceeded"

##### How functions are stored and removed
When functions is called, we say it is pushed into stack it is stored in call-stack and when program executed all codes till curly brace of function or it encounters return keyword it is removed or popped from the call-stack

##### Stacks Analogy
Imagine you keep stacking up plates on top of another and when you need to clean them, you start by removing the plate at the very top which was put last so the plate first put in the stack will be removed last

##### Real World use cases
For storing invoked functions
undo/redo in photoshop 

##### How to implement it with code
You have two options to do it 
1. By using array you can simulate stack but it is very inefficient with unshift and shift as all items has to be reindexed when one of these methods used, use push and pop instead
2. SLL or DLL SLL is very efficient enough to implement stack.

##### Big O of stacks with SLL/DLL 
Adding and Removing O(1)
Searching and Accessing O(n)


#### Queues
Queues are FIFO(first-in-first-out) and LILO(last-in-last-out) data structure

##### How to implement it with code
You can implement it with array or SLL/DLL
1. Implementing queues with array is very inefficient with arrays as you have to use combination of push and shift or unshift and pop both of which cause all items being reindexed. Imagine working with millions of sets of data.
2. Use SLL/DLL

##### Big O of Queues with SLL/DLL
Adding and Removing O(1)
Accessing and Searching O(n)


### Day 4: Dec 7, 2020

#### Things I've learned today
 * Tree Traversal
 * Breadth First Search
 * Depth First Search (Pre-Order; Post-Order; In-Order)
   
   
##### Tree Traversal
Traversing Tree is process of visiting (checking and or updating) each node exactly once in the tree data structures

##### Breadth First Search
Breadth First Search  searches nodes on the same level and it uses queue(array/sll/dll) to enqueue them and after it visited them, itdequeue them

##### Depth First Search
Depth First Search searches nodes vertically and it has 3 algorithms on its own to visit nodes on the specific order

##### Pre-Order and for What it is used for
In Pre-Order algorithm first root(parent) node visited, then all left child nodes and all right child nodes: ROOT -> LEFT CHILD -> RIGHT CHILD
It is used to copy tree

##### Post-Order and for What it is used for
In Post-Order first left child node then right child node and then finally parent node visited: LEFT CHILD -> RIGHT CHILD -> ROOT 
It's used to delete tree as it first visits child nodes then parent node

##### In-Order
In In-Order first left child node and then its parent node then right child node visited: LEFT CHILD -> ROOT -> RIGHT CHILD
If we use In-Order in BSTS we will get sorted data



### Day 5: Dec 8, 2020

#### Things I've learned today
 * Binary Heaps
 * Priority Queues
        
        
##### Binary Heaps
Binary Heaps are one of the Heap data structure and is also like tree especially Binary Search Tree

Binary Heaps has following things:
1. Each parent node can have at most 2 child nodes
2. left child node is always inserted first. As a result they become compact trees. Unlike BSTS in which as a result of adding all nodes to one side, SLL/DLL like structure is created.
3. In Binary Heaps there are no such rules as values of the child nodes that are greater than the values of the parent node, go to the right side of the parent node and values of the child nodes that are smaller than the values of the parent node, go to the left side of the parent node.
4. There are 2 rules to use BH, values of parent nodes either must alwaybe greater than their child nodes or values of parent nodes must always be smaller than values of child nodes based on type of heap is used
5. In Max Binary Heaps value of parent node must always be greater than values of child nodes
6. In Min Binary Heaps value of parent node must always be smaller than values of child nodes
7. BH can be implemented by SLL/DLL but it is most often used and recommended with Array as by using one awesome math formula -> 
   * We can find left and right child of parent node by following formula:  parent node at index of "n" in an array, its left child is stored at index of  2 * n + 1 and its      right child is stored at index of 2 * n + 2 and they have to be floored as division returns decimal as in array indexes integer based
   * We can find index parent node in index of child at "n" (n - 1) / 2 and it has to be floored
8. Big O of Adding and Removing is O(log n) and Searching is O(n)
9. It is used to implement Graph Traversal
10. It is used to implement Priority Queues

##### Priority Queues
1. Priority Queues are data structure in which nodes are specified priorities and nodes with higher priorities are dequeued(executed, served) before nodes with lower priorities.
2. It is best implemented with Binary Heaps



### Day 6: Dec 9, 2020

#### Things I've learned today
 * Hash Tables
       
##### Hash Tables
Hash Tables are data structure that consists of collection of key-value pairs and it's built-in most programming languages. We know it as Objects and Maps in JavaScript and dictionaries in Python and it is built-in many other programming languages.

##### How to Create Hash Table
Hash Tables is implemented with Array
We have to use a hash function to convert key to valid index to find value of it.

##### Hash Function
1. Hash function basically creates index for key-value pairs to be inserted in arrays
2. It uses prime numbers to distribute key-value pairs evenly throughout an array.
3. Optimally array length of also should be some prime number 
3. Same input always produce same output
4. It takes input of any size and create fixed size (if array length is 10 it will create indexes 0-9 regardkess input sizes
5. It should be fast (constant time)

##### Hash Collision
Hash collision is when more than one key-value pair is inserted at the same index
It has 2 solutions
1. Use Separate chaining which is you can insert more than single key-value pair at the same index thus number of key-value pairs are more than length of an array
2. Use Linear probing which is you can insert only one key-value pair at each index thus array length and amount of key-value pairs will be equal

##### Hash function use cases
It is used in Security, Cryptography, Hash Tables

##### Big O of Hash Tables
Average case: Adding O(1); Removing O(1); Accessing O(1)

Worst Case O(n)



### Day 7: Dec 10, 2020

##### Things I've done today
 * Today I wrote my first ever blog
 * Decided to create my Youtube channel
 
##### My Blog
I wrote my first ever blog on blogging platform DEV.to. It was just introduction on about me and 100 days of coding challenge that I started. And my goal of sharing my weekly progress on it

##### My Youtube Channel
I've finally made commitment to create my Youtube channel. I collected enough information on how to create Youtube channel and based on collected data, I made a plan on what kind of youtube channel i'm creating, what I'm teaching the first. So I'm teaching as I'm learning in my curriculum



### Day 8: Dec 11, 2020

##### Things I've learned
 * How internet works
 * Web hosting and domain name
 * What is software
 * Software devlopment life cycle
 
*I'll go briefly on each topic as they all were very long materials

##### How Internet Works
Internet works via well defined interfaces, protocols, packet routing routers, IP protocols, TCP protocols, FTP protocols and many more protocosl. It could be said Internet consits of protocols on how computers should communicate with each other.
 
##### Internet layers
Internet can be broken down into four independent layers each of which uses capabilities of layers underneath it. These layers are called network layers.And they are followings:
1. Application layer - application layers all capabilites of layers below it wihout worrying their implementation details, all the things that is interacted on the internet lives in this layer and also many protofols, IMAP, FTP and many more

2. Transport layer - This layer is there for if data loss in Link and Internet layers. That's why TCP layer lives in here which has 2 jobs. TCP reconstruct messages from packets and TCP re-transmit packets that did not reach to the destination computer

3. Internet layer - is concerned with routing packets to their destinations. IP Internet Protocol lives in here which is job is specify routers how to move packets to the destination computer but it doesn't guarentee that packet always make it to the destination
4. Link layer - it is physical layer which transmits data bits via some physical things in the form of fibre optic cables or wi-fi radio signals

##### Web Hostingn and domain name
Web hosting is remote computer server which is inserted into hude building or warehouse which stores files of your website and put your website onlin on the Internet
Domain name is address of your website

##### What is software
Software is sets of instrucions to tell computer what to do

There are types of software
1. Application software is anything that's designed for the client: website, webapp, browser, mediaplayer, spreadsheet and many many more

2. System software is anything to do with internal sytem of the computer like hardware, OS, Word processing editor and it works as interface between hardware and user applications


##### SDLC
It consits of 7 stages
1. Planning 
2. Requirement analysis
3. Design
4. Implementation/Coding
5. Testing
6. Deployment
7. Maintanance




### Day 9: Dec 12, 2020

##### Thing I've learned
 * How browser Works
 

##### How Browser Works
Browser is software application that is installed on the computer and is the client on the  Internet. It's used to retrieve web pages, documents, PDFs and display them on the screen

##### Web page, Website, Web server, Search engine
1. Web page is a single html document which can inlude external css, internal css, third party librariies and javascript files
2. Website is the collection of web pages that's linked with each other via links 
3. Web server is the remote computer where website is stored
4. Search engine is that which helps to find web pages. Search engines examples: Google, Yahoo, Yandex and more and also you can use search bar at the top of your browser


##### Browser Structure
1. UI of Browser which user directly interacts with are as followings: prev and next buttons, load and pause buttons, settings, preferences, bookmark, search bar, and many more
2. The Browser engine combines capabalities of UI of Browser with Rendering engine
3. Rendering engine displays parsed content of HTML, CSS, JavaScript and visual assets little by little on the screen as it receives packets from network calls to the server.
So Rendering engine can't wait till all packets come and parse them and display that'would be horrible UX and for this reason it gradually displays parsed contents of HTML,CSS,JAVASCRIPT and other visual assets to the users
4. Networking - is where request is made to the server HTTP/HTTPS
5. JavaScript interpreter - is used to parse and execute javascript code
6. Data Storage - this is a persisten layer and browser sometimes needs to save data locally like cookies and sessions and it has built-in storage  localStorage, IndexedDB, WebSQL and FileSystem.



### Day 10: Dec 13, 2020

##### Things I've learned
 * What is Client and Server

##### Client
Client is software application that runs on OS, mobile phones and any devices that has internet connection and installed browser. Users use it to browse the web.

##### Client-side code
Client-side code runs on the browser and so called front end developers use front end programming languages like Javascript, HTML, CSS to create UI of website

##### Server
Server is the remote computer on the web where it stores all files of static and dynamic website

##### Server-side code
Server-side code runs on the server and it's called backend programming where developer by using backend programming languages such as PHP, PYTHON, RUBY and their corresponding frameworks to dynamically create webpages based on the client's request



### Day 11: Dec 14, 2020

##### Things I've learned
 * 10 most commonly used software architectural patterns
 
##### Software architectural pattern
Software Architectural patterns is general reusable solutions to  commonly occuring problems in Software Architecture within a given context. They are like design patterns but their scope is broader

##### 10 most commonly used Software architectural patterns are as followings:
 1. Layered pattern
 2. Client Server pattern
 3. Master Slave pattern
 4. Pipe Filter pattern
 5. Broker pattern
 6. Peer-to-peer pattern
 7. Event-bust pattern
 8. Model-view-controller pattern
 9. Blackboard pattern
 10.Interpreter pattern
 
 
 
 ### Day 12: Dec 15, 2020
 
 #### Things I've done
 Today I only solved coding challenges and reviewed some lessons
 
 
 
 ### Day 13: Dec 16, 2020
 
 #### Thing's I've done
 Today I've solved coding challenges on data structures that I've learned from tomorrow I'm starting with HTML
 
 
 
 ### Day 14: Dec 17, 2020
 
 #### Things I've learned
  * HTML basics, semantic elements, best practises
  
  
 ##### Semantic HTML
 Semantics in HTML just means giving content of the web page proper meaning, outline and structure and by using appropriate semantic HTML elements.

- So in short semantic element

    Semantic element indicates what kind of content it contains

- What using semantic elements result in

    Using semantic elements help enable computers, screen readers, search engines and other devices to effectively read and  understand content of the web page.

- Why developers/designers should about using semantic elements
    - For search engines

        Semantic elements enable search engine to better read and understand the content of your websites. this ultimately placing you higher in search engine ranks

    - For screen readers

        Many disabled people such as visually impaired(blind) people use screen readers which reads content on the web for them. screen readers understand well semantic elements so semantic elements make website accessible to everyone

- text based semantical elements
    - headings <h1> to <h6>

        Headings help breaking content of the page and  with building hierarchy of each web page thus enabling searching engines index of a page and determine content of the web age. And they should be for semantic meaning not for making text bold

        - can you have more than one h1 in a single page

            version of before HTML5; h1 must be used once for per page and it indicates semantic meaning for screen readers that what this page is about

            But this is no longer case with HTML5; you can use multiple h1 headings for each web page

    - paragraphs <p></p>

        paragraphs just contains paragraphs and often used after heading to describe what title says in heading

    - bold text with <strong></strong> and <b></b>

        <strong></strong> semantic elements indicates that it contains important text

        <b></b> on the other hand is used to just making text stylistically bold

    - emphasizing text <em></em> and <i></i>

        <em></em> element is used to indicate that text it contains should be emphasized

        <i></i> text contains in it semantically means that it's alternative voice or tone. 

- structurally semantical elements
    - What are structurally semantical elements

        They give semantic structure to the web page and can be used multiple times as long as used correctly

    - header element

        <header> </header> elements semantically means that it's top part of the web page, article, sections, and other fragment of the web page. Inside header element can include followings introductory text, heading,  or even navigation 

    - navigation element

        <nav></nav> is used to indicate it contains major navigational links of the web page. It should only be used with major navigational sections such as global navigations, a table of contents, next/previous links  and other major navigational links

        - Can it be used everywhere

            No. if there's single link and not very important links use <a></a>

    - article element

        <article></article> element is used to indicate independent and context free section of the page that can be independently distributed and reused and still makes sense when used in different context.

        - How to decide whether to use article or not

            So when deciding to use article or not, we should think that if content in it is reused in different context does it still makes sense in new context if so we can use it.

    - section element

        Thematic means: - indicating theme of sentence;

        <section></section> semantically indicates that it contains thematically related group of content and generally includes heading.

        Section is useful to break up and provide a hierarchy for the web page

    - aside element

        <aside></aside> element contains content like sidebars, inserts or brief explanations and content in it is related  to its surrounding content(its parent element → it's nested inside another element)

        - Usage with article

            if aside is used inside article element it contains content about author of the article

    - footer element

        <footer></footer> element  semantically indicates  the end of the page, section, article or other fragment of the web page. And it's at the bottom of its parent element. And it should only contains content that's related to its parent element not different




 ### Day 15: Dec 18, 2020
 
 #### Things I've learned
  * CSS position elements
  * In which order to use CSS declarations
  
  - CSS
    - Declarations order

        You should combine declarations that are related to into single group in this order

        Reason positioning comes first because positioning element can remove it from normal document flow and override box model styles

        And box model comes next as it describe dimensions of elements

        Other do not effect above two in any shape of form so they come last

        1. Positioning
        2. Box Model
        3. Typography
        4. Visual
        5. Misc

        ```html
        declaration-order {
          /* Positioning */
          position: absolute;
          top: 0;
          right: 0;
          bottom: 0;
          left: 0;
          z-index: 100;

          /* Box-model */
          display: block;
          float: right;
          width: 100px;
          height: 100px;

          /* Typography */
          font: normal 13px "Helvetica Neue", sans-serif;
          line-height: 1.5;
          color: #333;
          text-align: center;

          /* Visual */
          background-color: #f5f5f5;
          border: 1px solid #e5e5e5;
          border-radius: 3px;

          /* Misc */
          opacity: 1;
        }
        ```

    - Selectors

        Avoid using attribute selectors because the Browser performance slow down causes by usage attribute selectors

    - CSS link pseudo-classes
        - What are the actual link pseudo-classes

            :link and :visited are made specifically for <a> tag to style it

        - What are dynamic pseudo-classes

            Dynamic pseudo-classes are :active, :hover, :focus which can be used to style not only links but any HTML elements

        - What link pseudo-classes

            Link pseudo-classes are just certain states of HTML links and knowing exact states of when they are activated enabling designers to be able to design link effectively

        - CSS pseudo-classes list for styling links

            :link, :visited, :hover, :active and :focus

            ```css
            * Default */
            a {
              color: blue;
            }
            /* Unvisited links */
            a:link {
              color: blue;
            }
            /* Visited links */
            a:visited {
              color: purple;
            }
            /* Hover state */
            a:hover {
              color: red; 
            }
            /* Focused state */
            a:focus {
              color: orange;
            }
            /* Activated state */
            a:active {
              color: green;
            }
            ```

        - Overview of pseudo-classes

            :link selects unvisited links

            :visited selects visited links

            :hover is the state of when user places his mouse pointer on top of the link or other element on which hover is used

            :active state occurs when user clicks-and-mouse-down on the link or element in which active is used without releasing mouse button.

            :focus state happens  when user tabs the link or element in it focus is used or after user clicks on the link or element in it focus is used

        - In which order CSS pseudo classes should be used

            This order below is suggested order

            ```css
            a { }
            a:link { }
            a:visited { }
            a:hover { }
            a:focus { }
            a:active { }
            ```

        - Modern browsers on :link and :visited link pseudo-classes

            Modern browsers restrict how :link and :visited should be used for security reasons. as hackers can manipulate :visited property to link to other hacky websites.

            :visited and :link link pseudo-classes should be used for changing following properties

            - `[color](https://css-tricks.com/almanac/properties/c/color/)`
            - `[background-color](https://css-tricks.com/almanac/properties/b/background-color/)`
            - `[border-color](https://css-tricks.com/almanac/properties/b/border/)` (and its sub-properties)
            - `[outline-color](https://css-tricks.com/almanac/properties/o/outline/)`
            - The color parts of the `fill` and `stroke` properties

- positioned elements
    - position fixed

        element with position fixed placed relative to the browser viewport

    - position absolute

        element with position absolute placed relative to its the closest parent other than ''static'' but with followings (absolute, fixed, relative)

    - setting width on absolutely and fixed positioned elements

        Setting width 100% on elements with positioned ''absolute, fixed; left, right''  is the same as setting both left:0 and right:0. instead use one only not both

    - Browser and position fixed

        Browsers break position: fixed on elements whose parent used transform property.

        This result in its parent element to be placed position relative and that position fixed element be placed as position absolute
