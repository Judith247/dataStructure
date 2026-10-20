# QueuePass — Queue-Based Ticket Booking Website

QueuePass is an educational website showing a real-world use of the **Queue** data structure in ticket booking. It demonstrates **FIFO (First In, First Out)**: the first customer to join is the first customer called.

## Features

- Register a customer for a sample event
- Assign a sequential queue ticket (Q001, Q002, ...)
- Select an event and number of tickets
- Display the live waiting queue and each customer's position
- Call the next customer using FIFO order
- Track waiting and served counts
- Add sample customers and reset the demo
- Explain enqueue, dequeue, front/peek, and real-world applications
- Responsive layout for mobile and desktop

## Files

- `index.html` — website structure and content
- `style.css` — responsive visual design
- `script.js` — interactive website queue simulation
- `queue.py` — standalone Python implementation of the FIFO queue
- `vercel.json` — static deployment configuration

## Run locally

You can open `index.html` in a browser, or run a simple local web server:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

To run the Python data-structure example:

```bash
python queue.py
```

## Deploy with GitHub Pages

1. Create a GitHub repository and upload all project files.
2. Open **Settings → Pages**.
3. Under build/deployment, select **Deploy from a branch**.
4. Choose the `main` branch and `/ (root)`, then save.
5. Wait for GitHub Pages to publish the website.

## Deploy with Vercel

1. Push this project to a GitHub repository.
2. Sign in to Vercel and choose **Add New → Project**.
3. Import the repository.
4. For this static website, use no build command and set the output directory to `.` (the project root), if Vercel asks.
5. Deploy.

## Important technical note

The deployed interactive demo uses JavaScript in the browser so it can run as a static site on GitHub Pages or Vercel. `queue.py` is the separate Python implementation of the same FIFO logic for the data-structure requirement and can be run from the command line.

This is a **demo**, not a production ticket-selling service. The queue exists in the current browser session; it is not shared across visitors, and it is not saved to a database. There is no payment processing or real ticket issuance. A production multi-user system would need a backend API, database, authentication, ticket inventory management, and payment integration.
