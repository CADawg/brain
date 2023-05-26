---
dg-publish: true
---
Now works out of the box with Preact, [react-router-dom](https://www.npmjs.com/package/react-router-dom) on NPM.
The Accepted way to do React Router is now to define it in the index.js file like so:

```jsx
import { render } from 'preact'  
import { Home } from './Home'  
import {createBrowserRouter, RouterProvider} from "react-router-dom";  
  
const router = createBrowserRouter([  
	{  
		path: '/',  
		element: <Home />  
	},  
]);  
  
render(<RouterProvider router={router} />, document.getElementById('app') as HTMLElement)
```

### Loaders
Allow you to load async data and access them as if they were syncronous.
[[React Router - Loader]]

#Web #React