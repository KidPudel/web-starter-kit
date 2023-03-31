The main point where we put everything is `App.tsx`, that's a common one, okay?

Now for the folder structure.  

Again, every project is going to have components and hooks, so why not add folders for it?  
| + `components`, `hooks` to your project |

Great, now we can distinguish 3 project categories: **_beginner_**, **_intermediate_**, **_advanced_**

# beginner

```
my-react-app/
├── node_modules/
├── public/
│   ├── index.html
│   ├── favicon.ico
│   └── ...
├── src/
│   ├── components/
│   │   ├── Header.js
│   │   ├── Footer.js
│   │   └── ...
│   ├── hooks/
│   │   ├── useFetch.js
│   │   ├── useForm.js
│   │   └── ...
│   ├── App.js
│   ├── index.js
│   └── ...
├── package.json
├── package-lock.json
├── README.md
└── ...
```

# intermediate
```
my-react-app/
├── node_modules/
├── public/
│   ├── index.html
│   ├── favicon.ico
│   └── ...
├── src/
│   ├── assets/
│   │   ├── images/
│   │   ├── fonts/
│   │   └── ...
│   ├── components/
│   │   ├── common/
│   │   │   ├── Button/
│   │   │   ├── Input/
│   │   │   └── ...
│   │   ├── features/
│   │   │   ├── Dashboard/
│   │   │   ├── Profile/
│   │   │   └── ...
│   │   └── ui/
│   │       ├── Header/
│   │       ├── Sidebar/
│   │       └── ...
│   ├── context/
│   │   ├── AuthContext.js
│   │   ├── ThemeContext.js
│   │   └── ...
│   ├── data/
│   │   ├── api/
│   │   ├── constants/
│   │   └── ...
│   ├── hooks/
│   │   ├── useAuth.js
│   │   ├── useData.js
│   │   └── ...
│   ├── pages/
│   │   ├── Home/
│   │   ├── About/
│   │   └── ...
│   ├── utils/
│   │   ├── formatDate.js
│   │   ├── validateEmail.js
│   │   └── ...
│   ├── App.js
│   ├── index.js
│   └── ...
├── package.json
├── package-lock.json
├── README.md
└── ...
```
In this structure:
- The `assets` folder contains all the images, fonts, and other static files used in the app.   
- The `components` folder is divided into sub-folders based on the type of component:
  - such as `common` for reusable components, `features` for larger feature components, and `ui` for presentational components.

- The `context` folder contains any React Contexts used in the app, such as an AuthContext or ThemeContext.
- The `data` folder contains any data used in the app, such as API endpoints or constants. 
- The `hooks` folder contains custom hooks used throughout the app.
- The `pages` folder contains the top-level pages of the app, such as the home page, about page, and so on. **_It contains unique components to that page_**
- The `utils` folder contains any utility functions or modules used throughout the app.

# advanced

```

my-react-app/
├── node_modules/
├── public/
│   ├── index.html
│   ├── favicon.ico
│   └── ...
├── src/
│   ├── assets/
│   │   ├── images/
│   │   ├── fonts/
│   │   └── ...
│   ├── components/
│   │   ├── common/
│   │   │   ├── Button/
│   │   │   ├── Input/
│   │   │   └── ...
│   │   ├── features/
│   │   │   ├── Dashboard/
│   │   │   ├── Profile/
│   │   │   └── ...
│   │   └── ui/
│   │       ├── Header/
│   │       ├── Sidebar/
│   │       └── ...
│   ├── context/
│   │   ├── AuthContext.js
│   │   ├── ThemeContext.js
│   │   └── ...
│   ├── data/
│   │   ├── api/
│   │   ├── constants/
│   │   └── ...
│   ├── features/
│   │   ├── Auth/
│   │   ├── Notifications/
│   │   ├── Search/
│   │   └── ...
│   ├── hooks/
│   │   ├── useAuth.js
│   │   ├── useData.js
│   │   └── ...
│   ├── layouts/
│   │   ├── DashboardLayout.js
│   │   ├── PublicLayout.js
│   │   └── ...
│   ├── libs/
│   │   ├── moment.js
│   │   ├── axios.js
│   │   └── ...
│   ├── pages/
│   │   ├── Home/
│   │   ├── About/
│   │   └── ...
│   ├── services/
│   │   ├── AuthService.js
│   │   ├── NotificationService.js
│   │   └── ...
│   ├── utils/
│   │   ├── formatDate.js
│   │   ├── validateEmail.js
│   │   └── ...
│   ├── App.js
│   ├── index.js
│   └── ...
├── package.json
├── package-lock.json
├── README.md
└── ...
```
- the `features` folder contains top-level features of the app, such as authentication, notifications, search, and so on.
-  The `layouts` folder contains the layout components used to wrap the pages of the app, such as a DashboardLayout that adds a sidebar and navigation to the dashboard pages.
-  The `libs` folder contains any external libraries used in the app, such as `moment.js` for working with dates or `axios` for making API requests.
-  The `services` folder contains any services or classes used in the app, such as an AuthService for handling user authentication.


