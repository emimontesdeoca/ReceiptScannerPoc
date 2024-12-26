# ReceiptScanner 🧾

## 🎉 **Part of the Calendario de Adviento de Inteligencia Artificial 2024** 🎉

**About the Advent Calendar of AI**  
Advent calendars have become a cherished tradition in the tech community, eagerly anticipated every year. During December, experts and enthusiasts from various fields share their knowledge in different formats:

- Blog posts  
- Videos  
- Webinars  
- Interesting announcements related to AI  
- And more

This 2024, Pablito Piovano and Roberto Navarro are leading the second edition of the **Calendario de Adviento de Inteligencia Artificial en Español**, bridging the gap across the ocean. The goal of this event is to create a platform for sharing AI knowledge and experiences, providing a valuable resource for both beginners and experts in the field.

For more details, you can check out the event's page: [Calendario de Adviento de Inteligencia Artificial 2024](https://dev.to/roberto_navarro_mate/calendario-de-adviento-de-inteligencia-artificial-2024-en-espanol-bdb).

---

**¿Qué es un calendario de adviento?**  
Los calendarios de Adviento son una tradición entrañable en la comunidad tecnológica, que cada año anticipan con entusiasmo. Durante el mes de diciembre, expertos y entusiastas de diversas áreas comparten su conocimiento a través de distintos formatos:

- Publicaciones de blog  
- Vídeos  
- Seminarios web  
- Anuncios interesantes relacionados con la IA  
- Y más

Este 2024, Pablito Piovano y Roberto Navarro nos embarcamos en la segunda edición del **Calendario de Adviento de Inteligencia Artificial en Español** a ambos lados del charco. Este evento tiene como objetivo crear una plataforma de intercambio de conocimientos y experiencias sobre Inteligencia Artificial, proporcionando un valioso recurso tanto para principiantes como para expertos en el campo.

Para más detalles, puedes revisar la página del evento: [Calendario de Adviento de Inteligencia Artificial 2024](https://dev.to/roberto_navarro_mate/calendario-de-adviento-de-inteligencia-artificial-2024-en-espanol-bdb).

---

ReceiptScanner is an innovative tool designed to scan, process, and extract detailed information from receipt images. Leveraging artificial intelligence (AI) and advanced image recognition, the application can intelligently identify individual items on a receipt along with their respective prices. Perfect for businesses and individuals who want to digitize receipts quickly and efficiently!

## Table of Contents
- [Features](#features)
- [System Requirements](#system-requirements)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Features
- **Receipt Scanning**: Capture and process receipt images instantly.
- **Item Detection**: Automatically identify individual items on a receipt.
- **Cost Extraction**: Extract and display item costs in a structured format.
- **AI-Powered Accuracy**: Uses cutting-edge AI models to ensure accurate recognition of various receipt formats.
- **Exportable Data**: Easily export scanned data to various formats like CSV or JSON for further processing.
- **Multi-Language Support**: Supports receipt recognition in multiple languages, perfect for global use.
- **User-Friendly Interface**: A sleek, easy-to-use interface to manage and view receipt data.

## System Requirements
Before installing ReceiptScanner, ensure your system meets the following requirements:

- **Operating System**: Windows 10 or later / Linux (Ubuntu 20.04 or later) / macOS
- **Runtime Environment**: .NET 8
- **Processor**: Intel i5 or equivalent
- **Memory**: 8 GB RAM or higher
- **Storage**: 2 GB of available space
- **Additional Software**:
  - Access to **Azure OpenAI API** for receipt text recognition
  - A modern web browser for accessing the web interface

## Installation
Follow these steps to install ReceiptScanner:

1. **Clone the Repository**:
    ```sh
    git clone https://github.com/emimontesdeoca/ReceiptScannerPoc.git
    cd ReceiptScannerPoc
    ```

2. **Set Up the Environment**:
   Ensure .NET 8 SDK is installed on your machine. Download it [here](https://dotnet.microsoft.com/download).

3. **Install Dependencies**:
   Install the necessary packages using NuGet Package Manager:
   ```sh
   dotnet restore
   ```

4. **Configure Azure OpenAI Integration**:
   - Set up an **Azure OpenAI** subscription and get your API key from [Azure's OpenAI Service](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/).
   - Configure the `appsettings.json` file with your API key and endpoint.

5. **Build the Application**:
   ```sh
   dotnet build
   ```

6. **Run the Application**:
   ```sh
   dotnet run
   ```

## Project Structure
The project is structured as follows:

```
C:\DEVELOPMENT\PROJECTS\RECEIPTSCANNER
├───ReceiptScanner.ApiService
├───ReceiptScanner.AiService
├───ReceiptScanner.Web
├───ReceiptScanner.ServiceDefaults
└───ReceiptScanner.ApiService
```

- **ReceiptScanner.ApiService**: Contains the API endpoints for processing receipt images.
- **ReceiptScanner.AiService**: Handles AI-based receipt image recognition and item detection using Azure OpenAI.
- **ReceiptScanner.Web**: The user interface where users can upload receipts and view results.
- **ReceiptScanner.ServiceDefaults**: Contains default configurations and services for the application.

## Configuration
Edit the `appsettings.json` file in the `ReceiptScanner.AiService` project to include your Azure OpenAI API integration settings:

```json
{
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "AllowedHosts": "*",
  "AzureOpenAI": {
    "ApiEndpoint": "https://<your-endpoint>.openai.azure.com/",
    "ApiKey": "<your-api-key>",
    "DeploymentName": "<your-deployment-name>",
    "Prompt": "The image provided is a receipt. Please extract all items with their corresponding prices, along with the store name, date, and total. Return the data in a structured JSON format with fields 'Items' (array of items with 'Name' and 'Price'), 'Store', 'Date', and 'Total'."
  }
}
```

## Usage
1. **Launch the Application**:
   Start the application via the command line or your chosen IDE.

2. **Upload a Receipt**:
   Use the web interface to upload receipt images for processing. Supported image formats include JPG, PNG, and PDF.

3. **Configure Settings**:
   - Ensure the Azure OpenAI API keys and endpoint are correctly set in `appsettings.json`.
   - Configure any additional settings for data export and UI preferences.

4. **Start Scanning**:
   After uploading, the application will begin processing the receipt and display the extracted information such as items and their prices.

5. **Review and Export Results**:
   View the extracted data in the dashboard, and export it as CSV or JSON for further analysis or record-keeping.

## Contributing
We welcome contributions to ReceiptScanner!

1. **Fork the Repository**.
2. **Create a Branch**: 
   ```sh
   git checkout -b feature/your-feature-name
   ```
3. **Commit Your Changes**: 
   ```sh
   git commit -m 'Add some feature'
   ```
4. **Push to the Branch**:
   ```sh
   git push origin feature/your-feature-name
   ```
5. **Open a Pull Request**.

## License
Distributed under the MIT License. See `LICENSE` for more information.

---

Thank you for using ReceiptScanner! We hope this tool brings more efficiency to your daily receipt management and helps you digitize your receipts with ease.