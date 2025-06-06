## **1. WHAT IS CSS**
- `CSS` stands for **Cascading Style Sheet**.
    - css uses `cascading algorithm` to style the sheet.
    - If we are applying styling to an element and there are more than one code pointers which are styling the html element then which styling will be given precedence is decided by `cascading algorithm`.
- `CSS` is used in html to style the page.

- One valid css styling or instruction ends with semi-colon.
- There are three ways by which we can apply css.
    1. Inline css.
    2. Internal css.
    3. External css.
- One should never ever do **inline css** and should avoid i**nternal css** as much as possible.
- The **css** that is written later will be used for styling the sheet i.e. if there is more than one css code which is styling the same html element, then the css code written later will be given preference.
    - #### **examples**
        ```
        <style>
            span{
                font-size: 20px;
                }
            h2{
                color:blue;
            }
        </style>
        </head>
        <link rel="stylesheet" href="Style.css">
        ```
        In the above example h2 element is being applied css to change the color to blue in the internal css but in external css which is Style.css file h2 element is given css of color: gold. Since external css is applied later hence h2 element color will be changed to gold.
### **INLINE CSS**
- Inline css means if there is an HTML element i.e. all the html element like **h1**, **div**, **span** etc. have special attribute named `style` where we can write a bunch of css.
- Inline css can be applied by using `style` attribute of an html element.

- One valid styling of inline css ends with semi-colon.
-  For ex.  ``<h2 style="color:gold; font=50px;"> Rahul singh </h2>.``
- Inline css is not so good because when we write a lot of css then the html page will not look that much good. hence Internal css is used.
### **INTERNAL CSS**
- `Internal css` is used within the **head** tag of html document by using `style` tag.

- This way of applying css is used to syle the particular tag.
    - example:
     ```
     <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
        <style>
            span{
                font-size: 20px;
            }
        </style>
    </head>
- This way of styling the html page is called internal beacuse within the same page css is being used.
- Why `internal css` is not preferred over `external css`.
    - There is the concept called `seperation of concern` which says that in relevant file there should only be relevant code.  i.e. if there is html element in one file then that file should only contain html element to design the webpage. css code must be written in the separate file.
### **EXTERNAL CSS**
- Extenal css is called external because the css is written in the other document.

- The html document in which css is to be applied has to be linked to this css file using link tag.
- For ex. ``<link rel="stylesheet" href="Style.css">``
## **2. SELECTORS**
- Selectors is a mechanism which css provide us to collectively select a bunch of html elements together and style them together.

- Here are different types of selectors based on which type of html elements it select.
### **2.1 UNIVERSAL SELECTOR**
- This selectors select everything in the html document and apply css rule to everything.

- This selector select every html tag manually and apply styling to it.
- Represented by `*`.
- Ex: 
    ```
    * {
        background-color:blue;
    }
    ```
### **2.2 TYPE SELECTOR**
- This selector select a particular html element and then apply styling to it.

- Ex:
        ```
        h2{
            background-color: blue;
        }
        ```
### **2.3 CLASS SELECTOR**
- Class selector says that all the element with corresponding given class attribute will be selected.

- **Syntax**: 
    ```
    .(class-name){

    }
    ```
- For ex: 
    ``` 
    .mid-text{
        background-color: red;
    }
    ```
### **2.4 ID SELECTOR**
- This selector selects the element with particular id attribute and apply styling to it.

- Syntax:
    ```              
        #(id-attribute-name){
                }
    ```
- EX: 
    ```
        #head-text{
                    text-decoration-line:underline;
                    text-decoration-style:wavy;
                }
     ```


### **2.5 ATTRIBUTE SELECTOR:**
-  This selector selects all the html element having the mentioned attribute and apply styling to it.
        
### **2.6 SELECTOR LIST:**
- Agar aap ek se jyada html element pe same styling apply karna chahte hai to ek saath bhi kar sake hai

- For ex. agar mai div tag and h2 tag dono html element pe same styling apply karna chahta hun to mai `,` ka use karke kar sakta hun jaisa ki neeche diya gya hai.
- ```
        div,h2{
                font-size:larger;
            }
    ```
### **2.7 COMBINATORS:**
#### **2.7.1. DESCENDANT COMBINATOR:**
-  The descendant combinator, typically represented by a single space `" "` character, combines two selectors 
such that elements matched by the second selector are selected if they have an ancestor (parent, parent's parent, parent's parent's parent, etc.) element matching the first selector.

- For ex:
        ```
            A B{
                 color: white;
                }
        ```
            - All the html element B which is the descendant of A will be selected and styling will be applied to it only.

#### **2.7.2 CHILD COMBINATOR:**                
- The child combinator `>` is placed between two CSS selectors. It matches only those elements matched by the second selector that are the direct children of elements matched by the first. Descendant elements further down the hierarchy don't match.

- For example, to select only `<p>` elements that are direct children of `<article>` elements:
    ```
        article > p{
                    }
    ```
                
#### **2.7.3. NEXT-SIBLING COMBINATOR / ADJACENT-SIBLING COMBINATOR:**
- The next-sibling combinator  `+` is placed between two CSS selectors. It matches only those elements matched by the second selector that are the next sibling element of the first selector. For example, to select all `<img>` elements that are immediately preceded by a `<p>` element:

    ```
        p + img{
               }
    ```
                
#### **2.7.4. GENRAL SIBLINGS COMBINATOR:**
- If you want to select siblings of an element even if they are not directly adjacent, then you can use the subsequent-sibling combinator `~` . To select all `<img>` elements that come anywhere after `<p>` elements, we'd do this:

     ```
        p ~ img{
        }
    ```                
### **2.8. PSEUDO CLASSES AND PSEUDO ELEMENTS:**
- If you want to make some changes to the selected html element based on some event.

- For ex: if you are hovering over to an element then you want to make some changes. In this case pseudo classes and pseudo elements are used.
#### **2.8.1 PSEUDO CLASSES**
- Represented by : 
- For ex:
        ```
            a :hover{
                text-decoration:none;
                }
        ```
    - What this example is saying that whenever we hover over anchor tag then the underline should go away.
                       hover class is not actually present in the html doc.

    - `:visited pseudo class`
    - `:hover pseudo class`
            
#### **2.8.2 PSEUDO ELEMENTS:**
- Represented by ::

- Pseudo elements are the html elements that are not actually present in the html doc.
            
