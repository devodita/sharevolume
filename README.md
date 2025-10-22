# BXP, Inc. Shares Outstanding Dashboard

This is a single-page application built to display the maximum and minimum shares outstanding for BXP, Inc. (and other companies via CIK lookup) using data from the SEC EDGAR API.

## Features

*   **Dynamic Data Display**: Fetches and displays the entity name, maximum, and minimum shares outstanding from fiscal years after 2020.
*   **Responsive Design**: Utilizes Tailwind CSS for a mobile-first, responsive user interface.
*   **CIK Lookup**: Supports dynamic fetching for any SEC-registered company by appending a CIK query parameter to the URL (e.g., `index.html?CIK=0001018724`).
*   **Single-Page Application**: Updates content without a full page reload.

## Getting Started

To view the application, simply open the `index.html` file in your web browser.

### Default View

By default, the application will display data for BXP, Inc. (CIK: 0001037540).

### Custom CIK Lookup

To view data for a different company, append the `CIK` query parameter to the URL:

`index.html?CIK=0001018724`

Replace `0001018724` with the 10-digit CIK of the desired company.

## Technical Details

*   **Frontend**: HTML, Tailwind CSS, JavaScript
*   **Data Source**: SEC EDGAR API (specifically `EntityCommonStockSharesOutstanding.json` endpoint)
*   **Proxy**: Uses `api.allorigins.win` as a client-side proxy to bypass CORS restrictions for fetching SEC data.
    *   *Note*: Client-side `fetch` cannot directly set the `User-Agent` header for cross-origin requests. While the SEC guidance requires a descriptive `User-Agent`, this is typically handled by a server-side proxy. The current implementation relies on the proxy service to manage its own `User-Agent` or omits it for direct SEC requests.

## Included Files

*   `index.html`: The main single-page application.
*   `README.md`: This README file.
*   `LICENSE`: The MIT License.
*   `uid.txt`: An attachment provided with the project, containing a unique identifier.

## License

This project is open-source and available under the MIT License.
