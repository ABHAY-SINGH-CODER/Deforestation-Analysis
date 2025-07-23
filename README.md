# 🛰️ Deforestation Analysis Tool

A web-based, interactive tool for visualizing and analyzing deforestation in near real-time. Users can select any region on a global map to receive a detailed analysis, including deforestation alerts and comparative satellite imagery.


## 🚀 Key Features

* **Interactive Global Map**: Built with Leaflet.js, providing a smooth and familiar map interface.
* **Select & Analyze**: Use the simple drawing tool to select any rectangular area of interest on the planet.
* **One-Click Analysis**: With a single click, send the selected area to a backend service for processing.
* **Hotspot Visualization**: Deforestation alerts are plotted directly on the map as "Critical" or "Moderate" hotspots.
* **Comparative Imagery**: View and compare satellite images from "Today" and "1 Month Ago" in both True Color and NDVI (Normalized Difference Vegetation Index) formats.
* **Modern & Responsive UI**: A clean, intuitive, and responsive interface that works on both desktop and mobile devices.
* **Clear Results Summary**: Get a quick overview of the number of alerts found in the selected region.

## 🛠️ How It Works

The tool provides a simple yet powerful workflow for environmental monitoring:

1.  **Area Selection**: The user draws a rectangle over an area of interest on the Leaflet map.
2.  **API Request**: The frontend captures the geographic coordinates (bounding box) of the selected rectangle. It then sends this data to the backend API (`https://carboneye-3.onrender.com/analyze-deforestation`).
3.  **Backend Processing**: The backend service receives the coordinates, fetches recent and historical satellite imagery for that location, and performs an analysis to detect changes in vegetation cover.
4.  **Data Response**: The API returns a JSON object containing:
    * A list of `alerts` with their severity (`critical`/`moderate`) and geographic position.
    * URLs for the generated `True Color` and `NDVI` satellite images for both "today" and "one month ago".
5.  **Frontend Visualization**: The frontend dynamically:
    * Plots the deforestation alerts on the map.
    * Displays the comparative satellite images in a responsive grid.
    * Updates the UI to show the analysis summary and legend.

## 💻 Technology Stack

This project is built entirely with frontend technologies, relying on an external API for data processing.

* **HTML5**: For the core structure of the application.
* **CSS3**: For all styling, animations, and responsive design, using modern features like Custom Properties (Variables) for easy theming.
* **JavaScript (ES6+)**: For all client-side logic, including map interactions, API calls, and DOM manipulation.
* [**Leaflet.js**](https://leafletjs.com/): A leading open-source JavaScript library for interactive maps.
* [**Leaflet.draw**](https://github.com/Leaflet/Leaflet.draw): A plugin for Leaflet to enable drawing and editing vectors on the map.

## ⚙️ Getting Started

To run this project locally, you just need a modern web browser.

### Prerequisites

* A web browser (e.g., Chrome, Firefox, Safari).
* A local web server (optional, but recommended for avoiding potential CORS issues). You can use the `Live Server` extension in VS Code or a simple Python server.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/deforestation-analysis-tool.git](https://github.com/your-username/deforestation-analysis-tool.git)
    ```

2.  **Navigate to the project directory:**
    ```bash
    cd deforestation-analysis-tool
    ```

3.  **Run the application:**
    * **Option A: Direct File Access**
        Simply open the `index.html` file in your web browser.
    * **Option B: Using a Local Server (Recommended)**
        If you have Python installed, run the following command from the project directory:
        ```bash
        # For Python 3
        python -m http.server
        ```
        Then, open your browser and go to `http://localhost:8000`.

### Configuration

The backend API endpoint is configured in the main script block within `index.html`. If you need to point to a different backend, modify this constant:

```javascript
const API_URL = '[https://carboneye-3.onrender.com/analyze-deforestation](https://carboneye-3.onrender.com/analyze-deforestation)';
```

## 🤝 Contributing

Contributions are welcome! If you have ideas for improvements or want to fix a bug, please feel free to:

1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/YourAmazingFeature`).
3.  Make your changes.
4.  Commit your changes (`git commit -m 'Add some AmazingFeature'`).
5.  Push to the branch (`git push origin feature/YourAmazingFeature`).
6.  Open a Pull Request.

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

## 🙏 Acknowledgements

* **Map Tiles**: [Esri](https://www.esri.com/en-us/home) — Source: Esri, i-cubed, USDA, USGS, AEX, GeoEye, Getmapping, Aerogrid, IGN, IGP, UPR-EGP, and the GIS User Community.
* **Libraries**: The teams behind [Leaflet.js](https://leafletjs.com/) and [Leaflet.draw](https://github.com/Leaflet/Leaflet.draw).
