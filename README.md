# SEC Entity Common Stock Shares Outstanding Viewer

This project provides a single-page, responsive web application built with HTML and Tailwind CSS to display the maximum and minimum common stock shares outstanding for a given SEC CIK (Central Index Key) entity. The data is fetched directly from the SEC's XBRL API.

## Features

-   **Dynamic Data Display**: Fetches and displays the entity name, maximum, and minimum shares outstanding, along with their respective fiscal years, for common stock shares outstanding reported after the year 2020.
-   **Responsive Design**: Utilizes Tailwind CSS for a modern, mobile-first, and responsive user interface.
-   **Dynamic CIK Loading**: Supports loading data for different CIKs by appending `?CIK=<your_cik_here>` to the URL (e.g., `index.html?CIK=0001018724`). The page updates without a full reload.
-   **Initial Data**: Defaults to CMS Energy (CIK: 0000811156) if no CIK is specified in the URL.

## Setup and Running

To run this application, simply open the `index.html` file in your web browser. No special server setup is required for basic functionality.

1.  **Save Files**: Ensure `index.html`, `README.md`, and `LICENSE` are in the same directory.
2.  **Open `index.html`**: Double-click `index.html` or open it via your browser's file menu.

### Important Note on CORS and SEC API

When fetching data for CIKs other than the default `0000811156` directly from the browser, you might encounter Cross-Origin Resource Sharing (CORS) issues due to SEC API policies.

To bypass CORS restrictions for dynamic CIK loading, a CORS proxy is required. This application uses a placeholder proxy URL. You might need to:

-   Deploy your own CORS proxy.
-   Use a public CORS proxy service (e.g., `https://corsproxy.io/?`). The current implementation uses `https://corsproxy.io/?` by default for demonstration purposes. Be aware of rate limits and reliability when using public proxies for production.

**Example URL with a different CIK:**

`index.html?CIK=0001018724`

This will fetch and display data for Berkshire Hathaway Inc.

## Technologies Used

-   **HTML5**: Structure of the web page.
-   **Tailwind CSS**: Utility-first CSS framework for styling.
-   **JavaScript (Vanilla)**: For data fetching, processing, and DOM manipulation.

## License

This project is open-source and available under the MIT License. See the `LICENSE` file for more details.
