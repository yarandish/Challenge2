**Problem**:
The $ ("body") load function in jQuery allows the html content of a file to be loaded into the body, in which case all the scripts in the html file in the body are loaded and executed correctly.
How to provide html content from a variable to body instead of loading it from a file. For example, consider that

in index.html:
 
```
function callForm2() {

            window.keeper = window.document.body;

            $("body").load(
                "Form2.html"
            );

        }        

 function closeForm2() {

            window.document.body = window.keeper;

        }
```

in **callForm2** Before the current content is called from a file, it is stored in a window.keeper variable 
in **closeForm2()** , after calling the file , I want to take the content from the window.keeper variable (old body content)  and set to current body, in which case the content of the variable is not equal to the previously saved one, and I can not return the original content of the variable.

So how do I save the current content of a variable for the next call?
What is the correct way to save and call in this case?
