# Valentine Invitation Site

A small, single-folder Valentine invitation site with:

- An animated envelope landing page (`index.html`)
- A message card asking her to be your Valentine
- A playful **No** button that can't actually say no (3 different confirmation prompts, then disappears)
- A **Yes** button that opens a love letter page (`love.html`)

Everything is plain HTML with Tailwind CSS loaded from a CDN, so you can deploy it anywhere that can serve static files.

---

## How to use it

1. **Open the project**
   - Open the folder `Valentines` in your editor (VS Code, Cursor, etc.).

2. **Preview locally**
   - Double-click `index.html` to open it in your browser.
   - Or serve the folder with any simple static server if you prefer (not required).

3. **Customize the text**
   - In `index.html`, search for:
     - `Dear <span id="valentineName">Valentine</span>` – change `"Valentine"` to her name.
     - The main paragraph text inside the card – rewrite to sound exactly like you.
     - The button labels if you want a different tone (e.g. “Yes, absolutely”).
   - In `love.html`, customize:
     - The heading text (`You just made my heart so happy`).
     - The paragraphs inside the love letter.
     - The closing line (`Your person`) to your own name or nickname.

4. **Add her photo**
   - In `index.html`, look for the comment:
     - `<!-- TODO: Replace this placeholder with her real photo -->`
   - Replace the `<img>` `src` with a real image file, for example:
     - Put `her-photo.jpg` in the same folder.
     - Change the tag to: `<img src="her-photo.jpg" alt="Her beautiful photo" class="h-full w-full object-cover" />`

---

## How the buttons work

- **Yes button**
  - When she clicks **Yes**, the envelope opens (if it isn’t already) and then it navigates to `love.html`, which shows the love letter.

- **No button**
  - When she clicks **No**, a small modal appears asking if she’s really sure.
  - This happens **3 times** with a different, more dramatic / sweet question each time.
  - After the 3rd time, the **No** button fades away and can’t be clicked anymore.
  - So she never truly gets to say “no” – just teased into thinking again.

You can adjust the texts for those questions in `index.html` where the `noQuestions` array is defined.

---

## How to deploy

Because everything is static (just HTML, CSS via CDN, and a tiny bit of JS), deployment is very easy:

- **Option 1: Zip and send**
  - Zip the whole `Valentines` folder and send it to her.
  - She can just open `index.html` in her browser.

- **Option 2: GitHub Pages**
  1. Create a new GitHub repository and add the contents of this folder.
  2. Push the code.
  3. In the repo settings, enable **GitHub Pages** with the branch as `main` (or `master`) and root as `/`.
  4. It will give you a URL to share with her.

- **Option 3: Netlify / Vercel**
  1. Create an account on Netlify or Vercel.
  2. Create a new site from your Git repository or drag-and-drop the folder (Netlify).
  3. It will auto-detect it as a static site and give you a URL.

No build step is needed because Tailwind is loaded via CDN and JavaScript is inline.

---

## Optional tweaks

- Change the gradient colors in the `<body>` classes if you want a different vibe.
- Tweak the envelope size by adjusting the width/height classes on the envelope container in `index.html`.
- Adjust the timing of the envelope animation by editing the CSS in the `<style>` block at the top of `index.html`.

Have fun making it more “yours” – the more personal, the better.


