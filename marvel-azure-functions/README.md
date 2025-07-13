# Marvel Azure Functions

This project contains an Azure Function that fetches Marvel characters from the Marvel API. The function is designed to handle HTTP requests, validate API keys, and process responses from the Marvel API.

## Project Structure

```
marvel-azure-functions
├── src
│   └── functions
│       └── GetMarvelCharacter.js  # Azure Function to fetch Marvel characters
├── host.json                       # Configuration file for Azure Functions host
├── local.settings.json             # Local settings for environment variables
├── package.json                    # npm configuration file with dependencies
└── README.md                       # Project documentation
```

## Getting Started

### Prerequisites

- Node.js installed on your machine
- Azure Functions Core Tools for local development

### Setup

1. Clone the repository:
   ```
   git clone <repository-url>
   cd marvel-azure-functions
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Configure environment variables in `local.settings.json`:
   ```json
   {
     "IsEncrypted": false,
     "Values": {
       "MARVEL_PUBLIC_KEY": "<your-public-key>",
       "MARVEL_PRIVATE_KEY": "<your-private-key>"
     }
   }
   ```

### Running the Function Locally

To run the Azure Function locally, use the following command:
```
func start
```

You can then test the function by sending a GET request to:
```
http://localhost:7071/api/GetMarvelCharacter?nameStartsWith=<character-name>
```

### Deployment

For deployment to Azure, follow the Azure Functions deployment documentation to publish your function app.

## License

This project is licensed under the MIT License.