# Bug 1 Solution

1. I opened the browser and inspected the element and found out the problem is in div with class RampInputSelect--dropdown-container

2. I searched using vscode for that class to find the file I must edit.

3. I noticed that you use javascript and react states to dynamically place the container, and In my opinion this is an overkill

4. I deleted the js code and edited the css to properly place the container.

notes: changing css might have side effects (I didn't change that much though ;) ), I would have checked other places this component is used to make sure that nothing is break and everything is working as expected, but since the application is one page I am good to go.
