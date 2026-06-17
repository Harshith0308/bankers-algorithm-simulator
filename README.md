# Banker's Algorithm Simulator

An interactive, browser-based simulator for the **Banker's Algorithm** — the classic
deadlock-avoidance and resource-allocation technique used in operating systems. Built
with plain HTML, CSS, and JavaScript (no frameworks, no build step), so it runs by
simply opening a file in the browser.

## Overview

The Banker's Algorithm decides whether granting a resource request will keep the
system in a **safe state**. This simulator lets you configure a system of processes
and resources, run the safety check, and submit dynamic resource requests — watching
in real time whether each request is granted or denied, and why.

## Features

- **Configurable system** — set any number of processes (n) and resource types (m).
- **Editable matrices** — enter the *Available* vector, *Max* demand matrix, and
  *Allocation* matrix directly in the UI.
- **Automatic Need matrix** — computed as `Need = Max − Allocation`.
- **Safety algorithm** — determines whether the current state is safe and displays a
  valid **safe sequence** when one exists.
- **Step-by-step trace** — a collapsible table shows how the *Work* vector evolves as
  each process completes.
- **Dynamic resource requests** — submit a request for any process; the simulator
  validates it against *Need* and *Available*, tentatively allocates, re-runs the
  safety check, and grants or rolls back accordingly.
- **Request log** — every request is recorded with its outcome and the reason.

## Getting Started

No installation or build is required.

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo>.git
   ```
2. Open `index.html` in any modern web browser.

Alternatively, enable **GitHub Pages** (Settings → Pages → deploy from the default
branch) to host a live version directly from the repo.

## How to Use

1. Enter the **number of processes** and **number of resources**, then click
   **Generate Matrices**.
2. Fill in the **Available**, **Max**, and **Allocation** values.
3. Click **Run Initial Safety Check** to compute the *Need* matrix and find a safe
   sequence (or detect an unsafe state).
4. Optionally, select a process, enter a **Request Vector**, and click
   **Submit Resource Request** to test dynamic allocation.

## Project Structure

```
.
├── index.html      # Main page and UI markup
├── style.css       # Styling
├── script.js       # Banker's Algorithm logic and DOM rendering
└── docs/           # Project report (PDF and DOCX)
```

## Concepts Demonstrated

- Deadlock avoidance and the concept of a *safe state*
- The Safety Algorithm (Work / Finish vectors)
- The Resource-Request Algorithm with safe rollback
- Need / Max / Allocation / Available matrix relationships

## Tech Stack

- HTML5
- CSS3
- Vanilla JavaScript (ES6)

## License

This project is licensed under the [MIT License](LICENSE).

## Author

**Harshith Sai**
