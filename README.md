
# Synthetic Dataset Generator 📊🚀

## Overview 📝
This project, **Synthetic Dataset Generator**, is a FastAPI-based application designed to generate synthetic datasets tailored to specific needs. I created this project because I participated in a hackathon where I couldn’t find a suitable dataset for my use case. To address this challenge, I developed a tool that leverages the Google Gemini API and Faker library to produce customizable synthetic data, which can be downloaded as a CSV file. This solution empowers developers and data enthusiasts to create datasets on-demand, saving time and fostering innovation.

## Features ✨
- Generate synthetic datasets with user-defined columns, types, and examples.
- Supports multiple data types (string, integer, float) with fallback generation using Faker.
- Integrates Google Gemini AI for advanced data generation.
- Provides downloadable CSV files with a simple API endpoint.
- Secured with API key authentication and CORS support for frontend integration.

## File Structure 📂
```
Synthetic-Dataset-Generator/
├── backend/
│   ├── src/
│   │   ├── config.py          # Configuration management
│   │   ├── logger.py          # Logging setup
│   │   ├── models/
│   │   │   └── schemas.py     # Data models for requests/responses
│   │   ├── routes/
│   │   │   └── dataset.py     # Dataset generation endpoint
│   │   ├── services/
│   │   │   └── data_generator.py  # Data generation service
│   │   ├── utils/
│   │   │   └── helpers.py     # API key validation
│   │   └── main.py            # FastAPI application entry point
│   └── requirements.txt       # Python dependencies
├── frontend/
│   ├── app/
│   │   └── generate/
│   │       └── page.tsx       # React component for generation
│   ├── package.json           # Node.js dependencies
│   └── tsconfig.json          # TypeScript configuration
├── .env                       # Environment variables (e.g., API keys)
├── .gitignore                 # Git ignore file
└── README.md                  # This file
```

## Prerequisites 🛠️
- Python 3.9+
- Node.js and npm (for frontend)
- Google Gemini API key
- pip and pipenv (or virtualenv)

## Installation 🖥️
### Backend
1. Clone the repository:
   ```bash
   git clone https://github.com/tanish-24-git/Data-gen.git
   cd synthetic-dataset-generator/backend
   ```
2. Set up a virtual environment and install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```
3. Configure environment variables in `.env` (e.g., `GEMINI_API_KEY`, `API_KEY`):
   ```bash
   echo "GEMINI_API_KEY=your-gemini-api-key-here" >> .env
   echo "API_KEY=x7k9p2m8q3n5r4t6" >> .env
   echo "LOG_LEVEL=INFO" >> .env
   echo "LOG_FILE=app.log" >> .env
   ```
4. Run the FastAPI server:
   ```bash
   python -m src.main
   ```

### Frontend
1. Navigate to the frontend directory:
   ```bash
   cd ../frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm run dev
   ```

## Usage 🚀
1. Access the frontend at `http://localhost:3000`.
2. Configure the dataset (e.g., columns, examples, row count).
3. Send a request to the backend API at `http://localhost:8000/api/v1/generate` with a valid `x-api-key` header.
4. Download the generated `synthetic_dataset.csv` file.

## API Endpoints 🌐
- `POST /api/v1/generate`  
  - **Description**: Generates and returns a synthetic dataset as a CSV file.
  - **Request Body**: `DatasetRequest` (JSON with columns and row_count).
  - **Headers**: `x-api-key` (required).
  - **Response**: `FileResponse` with `synthetic_dataset.csv`.

## Contributing 🤝
Contributions are welcome! Please fork the repository, create a feature branch, and submit a pull request with your changes. Ensure to follow the existing code style and add tests where applicable.

## License 📜
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments 🙏
- Thanks to the hackathon organizers for the inspiration.
- Special thanks to the Google Gemini API and Faker library teams for their powerful tools.
  


