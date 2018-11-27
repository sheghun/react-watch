# react-watch
Watching build mode on Create React App

Create React App does not provide watching build mode oficially ([#1070](https://github.com/facebookincubator/create-react-app/issues/1070)).

This script provides watching build mode for an external tool such as Chrome Extensions or Firebase app.

## How to Use

Create a React app.

Put the script into `scripts/watch.js`.

Add `watch` task into the scripts block in `package.json` as follows:

```javascript
  "scripts": {
    "start": "react-scripts start",
    // Add next line
    "watch": "node scripts/watch.js",
    "build": "react-scripts build",
    "test": "react-scripts test --env=jsdom",
    "eject": "react-scripts eject"
  }
```

Run the `watch` task.

```sh
npm run watch
```

Change source code and check `build` output.

Directory structure may be following:

- `app/`
  - `src/`
  - `public/`
  - `scripts/`
    - `watch.js` (need to add)
  - `package.json` (need to modify)
  - `build/` (output)
