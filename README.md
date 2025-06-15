# Software.Architecture.Packages
# Rockae AI Package Catalogue

A comprehensive Django-based system for managing and evaluating AI packages and tools in the Rockae ecosystem. This platform helps developers discover, integrate, and track the performance of various AI-related packages.

## Features

- **AI Package Management**: Catalog and organize AI packages with detailed metadata
- **Categorization**: Classify packages by AI functionality (NLP, Computer Vision, Generation, etc.)
- **Integration Types**: Support for various integration methods (API, Library, Plugin)
- **Performance Tracking**: Store and monitor performance metrics for each package
- **Popularity Metrics**: Track package adoption and usage statistics
- **Model Compatibility**: Document supported AI models and versions

## System Requirements

- Python 3.x
- Django
- Database (SQLite by default, configurable)

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd Backend.AIGenerator.WebJob
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run migrations:
   ```bash
   python manage.py migrate
   ```

4. Start the development server:
   ```bash
   python manage.py runserver
   ```

## Project Structure

```
Backend.AIGenerator.WebJob/
├── apps/
│   ├── catalogue/        # Package catalog management
│   ├── new_package/      # New package integration
│   └── shared/           # Shared utilities and models
├── Software.Architecture.Packages/
│   └── models.py         # Core package catalog models
└── manage.py
```

## Package Model

The core `RockaePackageCatalogue` model includes:

- `name`: Package/tool name
- `description`: Detailed functionality description
- `repository_url`: Source code repository link
- `ai_category`: AI functionality category
- `integration_type`: Integration method
- `supported_models`: Compatible AI models
- `popularity_score`: Usage popularity metric
- `performance_metrics`: Benchmarks and metrics data

## API Usage

The system provides RESTful APIs for package management:

- GET `/api/packages/`: List all packages
- POST `/api/packages/`: Register new package
- GET `/api/packages/<id>/`: Get package details
- PUT `/api/packages/<id>/`: Update package
- DELETE `/api/packages/<id>/`: Remove package

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the terms specified in the MIT LICENSE file.

## Support

For support and questions, please open an issue in the repository.

## Recent Improvements

- Added enhanced search functionality for AI packages
- Implemented a new search algorithm for improved relevance.

- Updated package compatibility documentation
- Updated dependencies to the latest stable versions.
