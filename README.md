EXPLANATION OF THIS PROJECT

This is a validation form(register and login) using a react hook known as useState

a. useState : A React hook that lets you add state (i.e., variables that change) to functional components.

b. const [name, setName] = useState("");
const [email, setEmail] = useState("");
const [password, setPassword] = useState("");

These lines create 3 pieces of state:

- name, email, and password are the current values.
- setName, setEmail, and setPassword are functions used to update them.
- useState("") means each one starts as an empty string.

c. e.preventDefault() prevents the page from reloading when the form is submitted (which is the default browser behavior).

d. const handleSubmit = async (e) => {
console.log(name, email, password);
};

This function runs when the Sign Up button is clicked.
It logs the user’s name, email, and password to the console for now (just for testing).

e. onChange: This is an event in React that runs when something changes in the input field (for example; when the user types something).

(e): This stands for event. It's a special object that React gives you. It contains information about what happened (in this case, what the user typed).

e.target.value: e.target refers to the input box itself (the thing the user is typing in).

.value is what the user typed. So e.target.value gives us the actual text the user typed into the input field.

setEmail(e.target.value): This is calling a function named setEmail and giving it the user's input. This function is used to store or update the email in your component’s state.

f. type="submit" triggers the form submission.
