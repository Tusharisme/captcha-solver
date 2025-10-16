# captcha-solver

## Overview

`captcha-solver` is a client-side web application designed to demonstrate the automatic parsing and display of text from a captcha image. This project extends a basic captcha display by simulating Optical Character Recognition (OCR) to detect and show text within a brief timeframe after the page loads. It's built entirely with HTML, CSS, and JavaScript, ensuring a lightweight and fully client-side execution.

The application is capable of loading captcha images either from a specified URL via a query parameter or by falling back to a default image asset included within the repository.

## How It Works

Upon loading, the web application performs the following steps:

1.  **Image Source Detection**: It first checks for a `url` query parameter in the browser's address bar (e.g., `index.html?url=https://example.com/captcha.png`).
2.  **Image Loading**:
    *   If a valid `url` parameter is found, the application attempts to load the image from that external URL.
    *   If no `url` parameter is present, or if the external URL fails to load, it falls back to a default image asset provided in the `/input/` directory (e.g., `sample.png`).
3.  **Simulated OCR**: Once an image is successfully loaded and displayed, a simulated OCR process begins. This process is designed to mimic the asynchronous nature of real OCR.
4.  **Text Display**: Within approximately 15 seconds of the page loading, the "Detected Text: ..." field is updated to show the simulated OCR result, providing immediate feedback on the "parsed" captcha.

## Project Structure

The repository is structured for clear organization and easy maintenance:

*   `index.html`: The main entry point of the application. It contains the HTML structure, includes CSS stylesheets, and embeds the JavaScript logic responsible for image loading, OCR simulation, and UI updates.
*   `/input/`: This directory houses static assets, primarily default image files like `sample.png`, which the application uses as a fallback when no external image URL is provided.
*   `/css/`: (Optional, but common) May contain external stylesheets for styling the application's user interface.
*   `/js/`: (Optional, but common) May contain external JavaScript files for modularity, if the application logic grows beyond what's suitable for `index.html`.

## How to Use / Run

To get this application up and running:

1.  **Clone the Repository**:
    ```bash
    git clone https://github.com/your-username/captcha-solver.git
    cd captcha-solver
    ```
2.  **Open `index.html`**:
    Simply open the `index.html` file in your preferred web browser. You can do this by navigating to the file path (e.g., `file:///path/to/captcha-solver/index.html`) or by serving it through a local web server for a more production-like environment.

3.  **Using the `?url` Override**:
    To test with a custom image URL, append the `?url=` query parameter to your `index.html` path:
    ```
    index.html?url=https://example.com/path/to/your/captcha.png
    ```
    For example:
    `file:///path/to/captcha-solver/index.html?url=https://www.google.com/recaptcha/api2/payload?p=0AABiH9g067c2...` (replace with a valid, accessible image URL)

    Upon loading, the application will display the captcha image (either from the URL or the default `sample.png`), and the simulated "Detected Text" will appear after a short delay (within 15 seconds).

## Technologies Used

*   **HTML5**: For structuring the web content.
*   **CSS3**: For styling the user interface.
*   **JavaScript (ES6+)**: For dynamic behavior, image loading, OCR simulation, and UI interaction.

## Deployment Notes

This project is fully client-side and requires no backend server. It is perfectly suited for deployment on static site hosting services such as:

*   **GitHub Pages**
*   Netlify
*   Vercel
*   Cloudflare Pages

To deploy, simply push your repository to your chosen platform, and configure it to serve the `index.html` file from the root of your `main` or `gh-pages` branch.

## License Notice

This project is open-source and available under the MIT License. See the `LICENSE` file for more details.