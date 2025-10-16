# captcha-solver

## Overview

The `captcha-solver` repository hosts a clean, client-side web application designed to display captcha images and provide an interactive interface for users to input their solutions. This project focuses on the frontend display logic, allowing for flexible image loading either from a specified URL or a default local image. It's an excellent starting point for building more complex captcha solving systems or for educational purposes in web development.

## How It Works

This web application operates entirely within the user's browser, leveraging HTML, CSS, and JavaScript.

1.  **Image Loading:**
    *   If a `?url=` query parameter is provided in the browser's address bar (e.g., `index.html?url=https://example.com/some-captcha.png`), the application dynamically loads and displays the image from that external URL.
    *   If no `?url=` parameter is present, the application defaults to loading `sample.png` located in the `/input/` directory of this repository.
2.  **User Interface:**
    *   The displayed image occupies a prominent area on the page.
    *   Below the image, a designated space (e.g., a text input field or display area) is provided where a user or an integrated solver can input or display the solved captcha text.

## Project Structure

The repository is structured for clarity and ease of use:

*   `index.html`: The main entry point of the web application. It defines the basic page structure, includes the necessary CSS for styling, and links to the JavaScript for dynamic behavior.
*   `style.css`: Contains all the styling rules for the web app, ensuring a clean and responsive user interface.
*   `script.js`: Implements the core logic for the application, including parsing URL parameters, loading images, and managing the UI elements.
*   `/input/`: This directory contains `sample.png`, which serves as the default captcha image when no external URL is specified.

## How to Use / Run

To get the `captcha-solver` web app up and running:

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/your-username/captcha-solver.git
    cd captcha-solver
    ```
2.  **Open `index.html`:**
    Simply open the `index.html` file in your preferred web browser.
    *   **Default Mode:** When opened directly, it will display the `sample.png` image from the `/input/` directory.
    *   **URL Parameter Mode:** To load an external image, append a `?url=` parameter to the `index.html` path in your browser's address bar. For example:
        `file:///path/to/your/captcha-solver/index.html?url=https://assets.example.com/captcha/image123.png`
        (Note: For local file URLs, ensure your browser's security settings allow local file access or use a local web server for testing.)

## Technologies Used

*   **HTML5:** For structuring the web content.
*   **CSS3:** For styling the user interface.
*   **JavaScript (ES6+):** For all dynamic behavior, image loading, and UI manipulation.

## Deployment Notes

This web application is designed to be fully client-side and requires no backend server. As such, it is ideal for static site hosting services. It can be easily deployed to platforms like GitHub Pages, Netlify, or Vercel by simply pushing the repository's contents.

## License Notice

This project is open-source. Please refer to the `LICENSE` file in the repository for details on the applicable licensing terms.