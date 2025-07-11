# Vue Dischi

Vue Dischi is a modern front-end web application developed with Vue.js. It serves as a dynamic interface for displaying a collection of music albums, fetching data asynchronously to provide an interactive user experience.

## Key Features

*   **Music Album Display**: Neatly presents a collection of music albums, likely including details such as artist, title, and cover art.
*   **Dynamic Data Retrieval**: Fetches album data asynchronously, ensuring the application remains responsive and up-to-date.
*   **Responsive UI**: Utilizes Bootstrap to provide a modern, mobile-first, and responsive user interface that adapts to various screen sizes.
*   **Vue.js Powered**: Built entirely with the Vue.js framework, leveraging its component-based architecture for maintainable and scalable development.

## Tech Stack

*   **Front-end Framework**: Vue.js
*   **Styling**: Bootstrap, Sass
*   **HTTP Client**: Axios
*   **Build Tool**: Vue CLI
*   **Languages**: JavaScript, HTML, CSS

## Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

*   Node.js (LTS recommended)
*   npm or Yarn

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/vue-dischi.git # Replace with actual repo URL
    cd vue-dischi
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    # OR
    yarn install
    ```

### Running the Project

1.  **Compile and hot-reload for development:**
    ```bash
    npm run serve
    # OR
    yarn serve
    ```
    This will typically launch the application on `http://localhost:8080`.

2.  **Compile and minify for production:**
    ```bash
    npm run build
    # OR
    yarn build
    ```
    This command compiles the application into static files for production deployment, typically in a `dist/` directory.

3.  **Run linting checks:**
    ```bash
    npm run lint
    # OR
    yarn lint
    ```