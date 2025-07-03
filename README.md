EXPLANATION OF THIS PROJECT

This is a validation form(register and login) using a react hook known as useState

- useState : A React hook that lets you add state (i.e., variables that change) to functional components.

- const Input: This is a React arrow function component named Input. It receives something called props. These are like values you send into the component.

- {label && (
  <!-- <label className="block text-sm font-medium text-gray-700 mb-1"> -->
  {label}
  <!-- </label> -->
  )}: This is a conditional rendering. It says: "If the label exists, show a <label> tag above the input.

- const handleChange = (e) => : handleChange runs every time a user types into an input field (like name, email, or password).(e) means the function takes an event object from the input field. When someone types into an input, this event carries useful info like:
  -What input was used (e.target.name)
  -What was typed (e.target.value)

- const { name, value } = e.target: It simply means:
-const name = e.target.name;
-const value = e.target.value;
name is the name of the input field (e.g., "email", "password") and value is what the user typed into the input
Example:
If the user types "user@gmail.com" into an input like this:
<!-- <input name="email" value="user@gmail.com" /> -->

- setFormData(...): This updates the form data in React state. This is the function that updates the formData state. Passing a new version of the form data.

- (prev) => (...): This is a function that gets the previous form data (what’s already typed so far), and returns a new updated version.

- ...prev: This copies everything in the old form data. It makes sure you don’t erase other fields.
  It's saying: “keep all the previous fields just the way they are.”

- [name]: value: This is dynamic key setting. It means: "Set the field that matches the name of the input to the new value the user typed."
  So if name = "email" and value = "user@gmail.com", it updates only the email field like this:
  {
  ...prev,
  email: "user@gmail.com"
  }

- const handleSubmit = (e) => : This creates a function called handleSubmit.
  (e) is the event object that React passes when something (like a form) happens.
  This function will run when the form is submitted (like clicking the submit button).

- e.preventDefault(): This stops that default refresh behavior.

- console.log(formData): console.log(...) just prints something in the browser’s developer console.
  formData is the object that holds all the form inputs (name, email, password).
  So this line shows you what the user typed in the form.
