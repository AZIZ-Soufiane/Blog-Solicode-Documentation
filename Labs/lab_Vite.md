Laravel 12 (the current version as of November 2025) includes Tailwind CSS v4 and Vite by default in new projects, automated for fresh projects, so the transition is straightforward if you've started fresh. You'll mainly need to install dependencies, update your Blade templates, and run Vite commands.
 
 * 01 - Create your project
 ```
 composer create-project laravel/laravel myproject
 cd myproject
 ```

* 02 - Install Dependencies

```
npm install
```

This installs all frontend dependencies listed in your package.json.
If your project already includes Vite, the Laravel Vite plugin, Tailwind CSS v4, etc., this command will download them automatically.

Ensure Tailwind CSS v4 is set up (default in Laravel 12); no tailwind.config.js needed unless customizing.

If Tailwind isn't present (e.g., in an older setup), add it with ````
npm install tailwindcss @tailwindcss/vite````


* 03 - Configure Vite (If Needed)

Check vite.config.js in your project root. It should include the Laravel plugin and reference your entry points like resources/css/app.css and resources/js/app.js. For Tailwind v4, add the @tailwindcss/vite plugin if missing:

```
import { defineConfig } from 'vite';
import laravel from 'laravel-vite-plugin';
import tailwindcss from '@tailwindcss/vite';

export default defineConfig({
  plugins: [
    laravel(['resources/css/app.css', 'resources/js/app.js']),
    tailwindcss(),
  ],
});
```


* 04 - Update CSS Entry Point

In resources/css/app.css, ensure it imports Tailwind with @import "tailwindcss";. Add @source directives to scan your files for classes (e.g., Blade templates and JS files).

```
@import "tailwindcss";
@source '../../vendor/laravel/framework/src/Illuminate/Pagination/resources/views/*.blade.php';
@source '../**/*.blade.php';
@source '../**/*.js';
```


* 05 - Load Assets in Blade:

Remove the Tailwind CDN ```<script> or <link> from your Blade layouts (e.g., resources/views/layouts/app.blade.php). Replace it with the @vite directive in the <head>:```

```
@vite(['resources/css/app.css', 'resources/js/app.js'])
```
If your CSS is imported via JS (common in SPAs), use just @vite('resources/js/app.js')



* 06 - Run Vite

Start the dev server with ```npm run dev```` (or composer run dev for convenience). This watches for changes and enables HMR. For production, run npm run build to minify and version assets.