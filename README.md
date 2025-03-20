✅ 1. Set Up the Environment
Clone or download the project locally.
Run the following commands:
bash
Copy
Edit
npm install
npm start
Ensure the app is running on http://localhost:3000.
Install the CodeSandbox CLI globally if needed:
bash
Copy
Edit
npm install -g codesandbox
Upload to CodeSandbox when you're ready:
bash
Copy
Edit
npm run upload
Ensure the link is editable and not read-only.
🐞 2. Debugging Approach
Bug 1: Select dropdown doesn't scroll with the page

Ensure the dropdown is absolutely positioned relative to the parent.
Use position: absolute with overflow: auto and ensure the parent container has position: relative.
Bug 2: Approve checkbox not working

Check the onChange handler of the checkbox component.
Ensure the event updates the correct transaction state.
Bug 3: Cannot select All Employees

Investigate the state update when selecting "All Employees".
Ensure that the employee filter resets the transaction data properly.
Bug 4: Clicking View More not appending data

Identify where new transactions are added to the state.
Use the spread operator to append new data instead of overwriting it.
Bug 5: Employees filter not available during loading

Ensure the employee loading state only reflects the employees request.
Separate this from the transaction loading state.
Bug 6: View More button behavior

Hide the button if:
The user is filtering by an employee.
No more data is available.
Track the current page and the last page for accurate pagination.
Bug 7: Approving a transaction won't persist

Ensure state mutations persist across filter changes.
Store the approval status in a global store or a persistent layer.
📤 3. Submission Checklist
Ensure all bugs are fixed and tested.
Open email.txt and add your email address.
Confirm your CodeSandbox link is editable.
Share the editable CodeSandbox link for submission.
