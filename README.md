# REACT-PROJECT => FireBlog App

## Steps to Solution

- Step 1 : Create React App using `npx create-react-app fireblog-app`

- Step 2 : Use Firebase Auth for authentication and Firebase Realtime Database for CRUD operations.

- Step 3 : You can use css frameworks like Bootstrap, Semantic UI, Material UI.

# <center>📜 SOME NOTES BEFORE STARTING 📜</center>

- <b>PROPS DRILLING</b> 👉 React developers often encounter scenarios where they must pass data/state from a top-level component to a deeply nested component. Prop drilling refers to <b>transporting this data/state as props</b> to the intended destination through intermediate components.

   + <b>Minibus analogy</b> 👉 The rearmost passenger can deliver his fare to the driver through the other passengers in front of him.

   + Props Drilling, may cause too many <b>renders</b> ❌

- We prefer to use <b>ContextAPI</b> to fix this problem 👇

   + If we have variables to store global data {user, theme, language} in an application, we can use ContextAPI.

   + Context API can be thought of as assistant in a minibus. We deliver the money to the driver at the very back via the assistant.

   + We create a global storage area (create method) with Context Api. With "UseContext()", we can get this data from that area.

- <b>Provider</b> 👇

   + When you create a context, you combine a provider with this context.

   + We wrap all the components with Provider.

   + Into Provider; we need to put all the components that we will wrap.

- <b>Router</b> 👇

   + We use "Router" to provide access to more than one page in SPAs (Single Page Application).

   + We use <b>"PrivateRoter"</b> to prevent unauthorized access to pages.

      - Those with Authorization will be able to access ✔ NewBlog>BlogForm, Detail, Profile, Update pages.

      - Those without Authorization  will be able to access ✔ just Navbar, Login/Register, Dashboard>BlogCard pages.