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

# Bug 3 Solution

1. when I redid the bug I realised that the problem might be a use case problem not a component problem.
2. I used "go to definition" functionality in vs code to find out that the component is used only in one place in app.tsx
3. I saw the onChange method and realized that here is the problem when I select all employees again this function gets called with `{id: '', firstName: 'All', lastName: 'Employees'}`
4. I also saw that you fetch all transactions after rendering using useEffect so I used the same function in the onChange callBack

notes: doing so might have some performance issues since I will be sending request every time I filter by employee and then select all employees again. perhaps it would be better if I store this in variable after the first request but I am not sure.

# Bug 4 Solution

1. I read the code and found out that the paginatedTransactions.data contains a page of transactions
2. so I need to store the previous transactions and append the new page to it.

# Bug 5 Solution

1. I knew where is the select component is rendered so I checked it and found out that the loading is controlled by a state, which get set to true after the two requests finished
2. replaced the loading state with employee.loading and then removed the loading state as it isn't used anywhere else.

# Bug 6 Solution

1. I went to where the button is renderd in the code.
2. I then changed the rendereing condition to the appropriate one.

# Bug 7 Solution

1. I couldn't reproduce the bug as the behaviour was as expected

note: I thing solving the previous bugs solved this issue.
