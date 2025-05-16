# Fullstack MERN Blogging Website

Fork this repo of "MERN Blogging Website" to start following the video tutorial.

Checkout website demo - [Demo](https://youtu.be/J7BGuuuvDDk)

![Thumbnail](https://c10.patreonusercontent.com/4/patreon-media/p/post/90122909/dd5363bd03fb4a6c8fcd5d15df98e6bf/eyJ3Ijo4MjB9/1.png?token-time=1697414400&token-hash=BZ-Mzp19WnBLcCFB8LmJFDw98mpnCRGcOCt_T615miY%3D)

This website features include -
1. Modern Blog Editor using Editor JS.
2. Google Authentication for Users
3. Dynamic Blog Pages on dynamic urls.
4. Search Page for Searching Blogs & users.
5. Dedicated Users Profile with thier social links and written blogs.
6. Dedicated dashboard to manage blogs either published or draft.
7. Blog Post Analytics, editable and deletable.
8. Like interaction on Blogs with feature to comment on the blog.
9. Reply to comments. ( A nested Comment System )
10. Every interaction on site stores as a notification for their respective users.
11. Recent notification highlight separating them from old notifications.
12. Edit profile option to update social links, bio and username
13. Also user can change login password from settings.
14. Its mobile responsive with modern design + fade in animation on pages.
And much more.

---
# Starting up the project
## Start Up the frontend server
``` bash
npm install
npm run dev
```
## Start Up the backend server
Change the directory to the server
``` bash
npm install
```
---
# 1. Navbar
Link: https://youtu.be/J7BGuuuvDDk?si=7BXToFGabEzxw9Yy&t=1446

## Notes:
- You need to wrap the app in a Browser Router to be able to use Link tags that lets you click on a link without reloading the page

--
# 2. Routes
Link: https://youtu.be/J7BGuuuvDDk?si=JYbhqaRloah9NZGP&t=3287

In App.jsx you have to import to be able to create seperate routes
``` jsx
import { Route, Routes } from "react-router-dom";

const App = () => {
    return (
        <Routes>
            <Route path="/" element={<Navbar />}>
                <Route path="signin" element={<h1>Sign in page</h1>}/>
                <Route path="signup" element={<h1>Sign up page</h1>}/>
            </Route>
        </Routes>
    )
}
```
In this example you can see that we use the Routes and the Route tag to create multiple routes. Here we want to have the Navbar on each page while also rendering the signin and signup page, but its tricky in react. You need to Use the Outlet in the react component.

Navbar Component
``` jsx
import { useState } from "react"
import logo from "../imgs/logo.png"
import { Link, Outlet } from "react-router-dom"

const Navbar = () => {

    const [ searchBoxVisibility, setSearchBoxVisibility] = useState(false)


    return (
        <>
            <nav className="navbar">
            </nav>

            <Outlet/>
        </>
    )
}

export default Navbar
```
I hide the content in the nav tags, but you can see the `Outlet` import as well as where `Outlet` tag is placed for any content to follow to be placed.

---
# 3.User Auth Form
Link: https://youtu.be/J7BGuuuvDDk?si=xrCO6rAJMlS58E_b&t=3730

---
# 4. Page Animation
Link: https://youtu.be/J7BGuuuvDDk?si=4jZ9UK9RAkguRbhc&t=5870