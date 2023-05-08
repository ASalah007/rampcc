# Bug 1 Solution

1. I opened the browser and inspected the element and found out the problem is in div with class RampInputSelect--dropdown-container

2. I searched using vscode for that class to find the file I must edit.

3. I noticed that you use javascript and react states to dynamically place the container, and In my opinion this is an overkill

4. I deleted the js code and edited the css to properly place the container.

notes: changing css might have side effects (I didn't change that much though ;) ), I would have checked other places this component is used to make sure that nothing is break and everything is working as expected, but since the application is one page I am good to go.


# Bug 2 Solution

1. while I was solving the first Bug I how the code is organized and I knew where I need to look.
2. I found out that you are making a custom check box by customizing the label tag and hiding the real input tag
3. since the input tag is hidden that user can not "change" it so I need to move the onChange function call to the input tag

