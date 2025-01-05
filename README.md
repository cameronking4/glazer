# Glazer - Interactive React Component Editor CLI

**Transform your development workflow with Glazer, a powerful CLI tool that overlays a React-based WYSIWYG editor on your web project. Seamlessly design, edit, and style React components interactively with Tailwind CSS.**

---

## Features 🚀

1. **CLI Commands**
   - `npm install -g glazer`: Install the CLI tool globally.
   - `glazer run`: Serve your web app and overlay the design editor.
   - Package.json integration for streamlined use with `npm run dev`.

2. **Integrated Server**
   - Lightweight Node.js server to serve the web app.
   - Proxy requests to your local app running on `localhost:3000`.

3. **React WYSIWYG Editor**
   - Interactive editor overlay for real-time design.
   - Drag, hover, and edit React components with ease.
   - Sidebar for component selection and manipulation.

4. **Tailwind CSS Integration**
   - Directly tweak Tailwind classes within the editor.
   - Real-time suggestions and validation for Tailwind utilities.

5. **Live Preview**
   - Real-time updates reflected in your app.
   - Overlay the editor dynamically using iframes or direct DOM injection.

6. **Component Manipulation**
   - Parse and render React components dynamically.
   - Add, remove, and edit components visually on a design canvas.

---

## Installation 🛠️

```bash
npm install -g glazer
```

## Usage 💡

Start your app with the interactive editor overlay:
```bash
glazer run
```

Add Glazer to your package.json scripts for quick access:
```
"scripts": {
  "dev": "glazer run"
}
```

## How It Works ⚙️

1. CLI Tool

The CLI initializes a Node.js server to serve your app and overlay the WYSIWYG editor.

2. Server

Proxies your local app while injecting the editor overlay:
```
const express = require('express');
const path = require('path');

const app = express();
const port = process.env.PORT || 3000;

app.use(express.static(path.resolve(process.cwd(), 'build')));
app.get('*', (req, res) => res.sendFile(path.resolve(__dirname, './editor.html')));

app.listen(port, () => console.log(`Glazer running at http://localhost:${port}`));
```

3. React-Based Editor

The editor provides a sidebar for selecting components, a draggable canvas for interactive design, and tools for editing Tailwind CSS styles.

## Core Benefits 🎯
	•	Real-time Editing: See changes instantly with live updates.
	•	Tailwind CSS at Your Fingertips: Modify styles dynamically with autocomplete and validation.
	•	Enhanced Developer Productivity: Design and code simultaneously without context switching.

## Contribute ❤️

Contributions are welcome! If you encounter bugs or have feature requests, feel free to open an issue or submit a pull request.

## License 📜

This project is licensed under the MIT License. See the LICENSE file for details.

## Sponsors 🌟

Help support this project and accelerate modern UI development! Sponsor us on GitHub.
