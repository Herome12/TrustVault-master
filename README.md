

---

# Banking System

This project is a banking system built using Next.js for the frontend, Appwrite for the backend, Plaid for banking integration, and Dwolla sandbox to manage bank accounts.

## Table of Contents

- [Getting Started](#getting-started)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Folder Structure](#folder-structure)
- [Contributing](#contributing)
- [License](#license)

## Getting Started

Follow these instructions to set up and run the project on your local machine for development and testing purposes.

## Prerequisites

- [Node.js](https://nodejs.org/) (v14 or later)
- [Appwrite](https://appwrite.io/) (latest version)
- [Plaid](https://plaid.com/) (development account)
- [Dwolla](https://www.dwolla.com/) (sandbox account)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/banking-system.git
   cd banking-system
   ```

2. Install the dependencies:

   ```bash
   npm install
   ```

3. Set up Appwrite:

   - Follow the [Appwrite installation guide](https://appwrite.io/docs/installation) to set up your Appwrite server.
   - Create a new project in Appwrite.
   - Create the necessary database collections and authentication rules.

4. Set up Plaid:

   - Sign up for a Plaid account and create a development environment.
   - Obtain your Plaid API keys (client_id, secret, and public_key).

5. Set up Dwolla:

   - Sign up for a Dwolla sandbox account.
   - Obtain your Dwolla API keys (key and secret).

## Configuration

Create a `.env.local` file in the root directory of the project and add the following environment variables:

```env
# Appwrite
NEXT_PUBLIC_APPWRITE_ENDPOINT=<YOUR_APPWRITE_ENDPOINT>
NEXT_PUBLIC_APPWRITE_PROJECT_ID=<YOUR_APPWRITE_PROJECT_ID>
NEXT_PUBLIC_APPWRITE_API_KEY=<YOUR_APPWRITE_API_KEY>

# Plaid
NEXT_PUBLIC_PLAID_CLIENT_ID=<YOUR_PLAID_CLIENT_ID>
NEXT_PUBLIC_PLAID_SECRET=<YOUR_PLAID_SECRET>
NEXT_PUBLIC_PLAID_PUBLIC_KEY=<YOUR_PLAID_PUBLIC_KEY>
NEXT_PUBLIC_PLAID_ENV=sandbox

# Dwolla
NEXT_PUBLIC_DWOLLA_KEY=<YOUR_DWOLLA_KEY>
NEXT_PUBLIC_DWOLLA_SECRET=<YOUR_DWOLLA_SECRET>
NEXT_PUBLIC_DWOLLA_ENV=sandbox
```

## Usage

1. Start the development server:

   ```bash
   npm run dev
   ```

2. Open your browser and navigate to `http://localhost:3000`.

3. Follow the on-screen instructions to create a new account, link your bank account using Plaid, and manage your bank account using the Dwolla sandbox.

## Folder Structure

```plaintext
banking-system/
├── public/
├── src/
│   ├── components/
│   ├── pages/
│   ├── services/
│   ├── styles/
│   └── utils/
├── .env.local.example
├── .gitignore
├── README.md
├── next.config.js
├── package.json
└── tsconfig.json
```

- `public/`: Static assets such as images, fonts, etc.
- `src/components/`: React components.
- `src/pages/`: Next.js pages.
- `src/services/`: API service functions.
- `src/styles/`: CSS and styling files.
- `src/utils/`: Utility functions and helpers.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any bugs, feature requests, or improvements.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

