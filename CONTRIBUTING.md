# Contributing to QR On-Site

<a href="https://winter-of-open-source.vercel.app/"><img src="https://raw.githubusercontent.com/datavorous/tinytracer/main/media/banner.png"></a>

Welcome to Winter of Open Source! 🎉    
We're excited to have you contribute to this QR Code Scanner and Generator project.

## Learning Resources

Before you start contributing, we **strongly recommend** learning the fundamentals of QR code encoding and decoding. The goal of this project is to build the scanner and generator logic **from scratch without using any prebuilt libraries or modules**.
https://dev.to/maxart2501/let-s-develop-a-qr-code-generator-part-i-basic-concepts-510a

### QR Code Generator - Essential Reading

You may follow this comprehensive 10-part tutorial series to understand QR code generation from the ground up:

| Part | Title | Topics Covered |
|------|-------|----------------|
| 1 | [Basic Concepts](https://dev.to/maxart2501/let-s-develop-a-qr-code-generator-part-i-basic-concepts-510a) | Data types, sizes, error correction, fixed patterns, capacity |
| 2 | [Sequencing Data](https://dev.to/maxart2501/let-s-develop-a-qr-code-generator-part-ii-sequencing-data-4ae) | Data encoding, byte mode, character count |
| 3 | [Error Correction](https://dev.to/maxart2501/let-s-develop-a-qr-code-generator-part-iii-error-correction-1kbm) | Reed-Solomon error correction, polynomial division |
| 4 | [Placing the Bits](https://dev.to/maxart2501/let-s-develop-a-qr-code-generator-part-iv-placing-the-bits-4cg6) | Module placement, data regions |
| 5 | [Masking](https://dev.to/maxart2501/let-s-develop-a-qr-code-generator-part-v-masking-3cjl) | Mask patterns, penalty scoring |
| 6 | [Format Information](https://dev.to/maxart2501/let-s-develop-a-qr-code-generator-part-vi-format-information-1k1g) | Format bits, error correction level encoding |
| 7 | [Painting the Canvas](https://dev.to/maxart2501/let-s-develop-a-qr-code-generator-part-vii-painting-the-canvas-27i6) | Rendering QR codes |
| 8 | [Bigger Sizes](https://dev.to/maxart2501/let-s-develop-a-qr-code-generator-part-viii-bigger-sizes-2hj5) | Handling larger versions |
| 9 | [Structuring Larger Versions](https://dev.to/maxart2501/let-s-develop-a-qr-code-generator-part-ix-structuring-larger-versions-2n5d) | Multiple data blocks, interleaving |
| 10 | [Creating Larger Codes](https://dev.to/maxart2501/let-s-develop-a-qr-code-generator-part-x-creating-larger-codes-31f4) | Complete implementation for all versions |

### QR Code Scanner - Suggested Readings

| Resource | Description |
|----------|-------------|
| [Thonky QR Code Tutorial](https://www.thonky.com/qr-code-tutorial/) | Comprehensive reference for QR code structure |
| [ISO/IEC 18004](https://www.iso.org/standard/62021.html) | Official QR code specification |
| [ZXing Library Algorithms](https://github.com/zxing/zxing/wiki/How-it-works) | Understanding detection and decoding algorithms |
| [QR Code Finder Pattern Detection](https://www.codeproject.com/Articles/1089319/QR-Code-Detection-and-Decoding) | Image processing techniques for QR detection |

### Additional Resources

- [Reed-Solomon Error Correction Tutorial](https://www.nayuki.io/page/reed-solomon-error-correcting-code-decoder), [Galois Field Arithmetic](https://research.swtch.com/field) : for understanding error correction
- [Computer Vision Basics (for Scanner)](https://docs.opencv.org/4.x/dc/da5/tutorial_py_drawing_functions.html) : for QR code detection
- [Canvas API (for rendering)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) : for rendering the QR codes

> [!IMPORTANT]
> **Do NOT use libraries like `qrcode.js`, `jsQR`, or similar.** The goal is to understand and implement the algorithms yourself!

---

## Getting Started

### Prerequisites
1. Basic knowledge of HTML, CSS, and JavaScript
2. Understanding of binary data and bitwise operations
3. Git installed on your system
4. A GitHub account

### Setting Up Local Environment

1. **Fork the repository**
   
   Click the "Fork" button at the top right of this repository.

2. **Clone your fork**

```bash
git clone https://github.com/YOUR_NAME/qr-on-site.git
cd qr-on-site
```

3. **Open in your browser**

   Simply open `index.html` in your browser to test the application.

4. **Use a local server** (recommended for development)

```bash
# Using Python
python -m http.server 8000

# Using Node.js (npx)
npx serve .

# Using VS Code Live Server extension
# Right-click on index.html -> "Open with Live Server"
```

---

## How to Contribute

### Step 1: Choose an Issue

* Browse [open issues](../../issues)
* Look for labels:
  * `good first issue` – beginner-friendly
  * `easy`, `medium`, `hard` – based on difficulty
  * `scanner`, `generator` – based on component
  * `documentation`, `bug`, `feature`, `enhancement`

### Step 2: Assign Yourself

* Comment `/assign` on the issue
* Wait for maintainer approval
* Complete issue within **48 hours**
* Work on **only 1 issue at a time**

### Step 3: Create a Branch

```bash
git checkout -b fix/issue-number-short-description
```

Example branch names:

* `fix/23-add-error-correction`
* `feature/45-implement-finder-pattern`
* `docs/12-improve-readme`

### Step 4: Make Changes

* Follow existing code style
* Add meaningful comments explaining **why**, not just what
* Test your changes thoroughly in multiple browsers
* Keep commits atomic

### Step 5: Commit Changes

```bash
git add .
git commit -m "Clear commit message

- Description of changes
- Link to issue: Fixes #23"
```

### Step 6: Push & Create PR

```bash
git push origin fix/issue-number-short-description
```

* Go to your fork on GitHub → "Compare & pull request"
* Fill out the PR template:
    - Link the issue using `Fixes #<issue-number>`
    - Describe what changes you made
    - Include screenshots/test results if applicable
    - Check all checklist items (if present)

---

## PR Acceptance Criteria

* Code is clean, commented, and follows project style
* No external QR libraries used (build from scratch!)
* Code tested in Chrome, Firefox, and Safari
* PR linked to an issue
* Screenshots/demos included if applicable
* No plagiarism

## Points System

| Contribution Type | Points |
| ----------------- | ------ |
| Easy Issue        | 10     |
| Medium Issue      | 20     |
| Hard Issue        | 40     |
| Documentation Fix | 5      |
| Bug Fix           | 20     |
| Feature Addition  | 30     |

### Bonuses

* First 10 PRs : +10 points
* First PR of the week : +10 points
* Most impactful PR : +50 points

---

## Reporting Bugs

* Provide description, steps to reproduce, expected vs actual behavior
* Include browser name and version
* Include screenshots if any
* Include console error messages if applicable

## Suggesting Features

* Describe the feature
* Explain why it's useful
* Optional: share implementation ideas

> [!NOTE]
> Follow the default templates while creating an Issue.

---

## Code Style

- Use 2-space indentation for HTML/CSS/JS
- Use descriptive variable names
- Maximum line length: 100 characters
- Explain **why**, not just what in comments
- Use ES6+ features where appropriate

### Example:

```javascript
// Good: Explains WHY
// Apply mask pattern 0: (row + col) % 2 === 0
// This creates a checkerboard pattern to improve readability
function applyMask0(row, col, bit) {
  return (row + col) % 2 === 0 ? !bit : bit;
}

// Bad: Explains WHAT (obvious from code)
// XOR the bit if condition is met
function applyMask0(row, col, bit) {
  return (row + col) % 2 === 0 ? !bit : bit;
}
```

---

## Getting Help

* Discord: [Server link]()
* GitHub Discussions
* Comment on issues to reach maintainers

## Important Rules

* Work on **one issue at a time**
* Complete assigned issues in 48 hours (can be extended based on difficulty)
* Respect code of conduct
* Always link your PR to an issue
* Avoid plagiarism or AI generated slop
* **NO external QR code libraries** – implement from scratch!

<p align="center">
<b>Happy Contributing! ❤️</b>
</p>
