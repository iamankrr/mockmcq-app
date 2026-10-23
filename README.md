# 📝 MockMCQ

A simple, mobile-friendly MCQ practice app. Upload a PDF of questions, and the app builds a question bank by itself. Then take randomized tests and get scored instantly.

Everything runs in the browser. There is no server and no database.

## ✨ Features

- **PDF upload**: reads multiple-choice questions straight from a PDF
- **Auto answer detection**: the **bold** option in the PDF is taken as the correct answer
- **Review screen**: check the parsed questions and fix any answer before saving
- **Randomized tests**: a new set of questions (default 100) every time, with shuffled options
- **Fair rotation**: questions shown fewer times are picked first, so repeats are minimized
- **Instant score**: correct answers in green, wrong answers in red
- **Retry mode**: practice only the wrong or skipped questions
- **Progress bar** and score history
- **Dark mode** and a mobile-first layout
- **Export / Import** the question bank as JSON

## 📄 Expected PDF format

Each question should have a number and exactly four options. The correct option must be in **bold**.

```
1. Which level is formed when similar cells perform a specific function?
(a) Organ
(b) Tissue        <- bold
(c) Organ system
(d) Population
```

Both `a.` and `(a)` option styles are supported.

> The PDF must contain real text. Scanned (image-only) PDFs are not supported, because bold text cannot be detected without OCR.

## 🚀 How to use

1. Open the site.
2. Upload your PDF.
3. Check the review screen. Questions marked ⚠️ need you to choose the correct option manually.
4. Tap **Save all**.
5. Set the number of questions and tap **Start Test**.
6. Submit to see your score and the correct answers.

## 💾 Data storage

The question bank and score history are saved in your browser's `localStorage`.

- Data stays on your device and is never uploaded anywhere.
- Each browser and each domain has its own separate data.
- Use **Export** to download `mcq-bank.json` and **Import** to load it on another device.
- Clearing your browser data will delete the bank, so keep an exported backup.

## 🛠 Tech stack

- HTML, CSS, JavaScript (single file: `index.html`)
- [PDF.js](https://mozilla.github.io/pdf.js/) for reading PDFs

## 🌐 Deployment

The app is a single static file, so it can be hosted anywhere.

- **Netlify**: connect this repo, leave build command and publish directory empty
- **GitHub Pages**: Settings → Pages → Deploy from branch → `main` / root

Every commit to `main` redeploys the site automatically.

## 🔧 Run locally

No build step is needed. Download `index.html` and open it in a browser.

## ⚠️ Known limitations

- Bold detection depends on the PDF's font names. Some PDFs may need manual answer selection on the review screen.
- Uploading the same PDF twice adds its questions twice.
- Data does not sync between devices automatically.

## 📜 License

Personal project. Add a license of your choice if you plan to share it.
