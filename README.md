# 📝 MockMCQ

Mobile-friendly MCQ practice app. Upload a PDF of questions, then take randomized tests and get scored instantly.

**🔗 Live:** https://mockmcq.netlify.app

## Features

- Reads MCQs from a PDF (the **bold** option is the correct answer)
- Review screen to fix answers before saving
- Random tests (default 100 questions) with shuffled options
- Instant score, retry wrong answers, score history
- Dark mode, works on phones
- Export / Import question bank as JSON

## PDF format

```
1. Question text?
(a) Option
(b) Option   <- bold = correct
(c) Option
(d) Option
```

Text-based PDFs only (scanned PDFs are not supported).

## Notes

- Data is saved in your browser's localStorage, so use **Export** to back it up.
- Built with plain HTML, CSS, JS and [PDF.js](https://mozilla.github.io/pdf.js/).
