# Meals - Recipe Discovery & Management App

A modern Flutter application for discovering, organizing, and managing meal recipes. Built with clean architecture principles and state management best practices, Meals offers an intuitive interface for food enthusiasts to explore recipes, save favorites, and apply dietary filters.

## Key Features

- **Categorized Recipe Discovery** - Browse meals by categories (Italian, Asian, Quick & Easy, etc.)
- **Favorites Management** - Save and organize your favorite recipes with one tap
- **Advanced Filtering** - Filter recipes by dietary preferences (Gluten-free, Vegan, Vegetarian, Lactose-free)
- **Detailed Recipe Views** - Complete ingredient lists and step-by-step cooking instructions
- **Modern UI/UX** - Material Design 3 with smooth animations and transitions
- **Responsive Design** - Optimized for various screen sizes and orientations
- **Offline Support** - Access recipes without internet connectivity
- **Dark Theme** - Beautiful dark mode interface

## Technology Stack

- **Framework:** Flutter 3.x
- **Language:** Dart
- **State Management:** Flutter Riverpod
- **UI Framework:** Material Design 3
- **Typography:** Google Fonts (Lato)
- **Architecture:** Provider Pattern with Clean Architecture principles
- **Navigation:** Flutter Navigator 2.0

## Project Architecture

```
lib/
├── data/
│   └── dummy_data.dart          # Local meal and category data
├── models/
│   ├── category.dart            # Category data model
│   └── meal.dart               # Meal data model with enums
├── providers/
│   ├── favorites_provider.dart  # Favorites state management
│   ├── filters_provider.dart    # Filtering logic
│   └── meals_provider.dart      # Meals data provider
├── screens/
│   ├── categories.dart          # Category grid view
│   ├── filters.dart            # Filter settings screen
│   ├── meal_details.dart       # Recipe detail view
│   ├── meals.dart              # Meals list view
│   └── tabs.dart               # Main navigation tabs
├── widgets/
│   ├── category_grid_item.dart  # Category card component
│   ├── main_drawer.dart        # Navigation drawer
│   ├── meal_item.dart          # Meal card component
│   └── meal_item_trait.dart    # Meal metadata component
└── main.dart                   # App entry point
```

### Architecture Overview

The app follows a **layered architecture** with clear separation of concerns:

- **Data Layer**: Local dummy data (easily extensible to remote APIs)
- **Provider Layer**: State management using Riverpod providers
- **Presentation Layer**: Screens and reusable UI components
- **Models**: Data structures and business logic entities

## Getting Started

### Prerequisites

- Flutter SDK (>=3.0.0)
- Dart SDK (>=2.17.0)
- Android Studio / VS Code with Flutter extensions
- iOS Simulator / Android Emulator

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/AliAhmed015/Meals.git
   cd Meals
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Run the app**
   ```bash
   # For development
   flutter run
   
   # For specific platform
   flutter run -d ios
   flutter run -d android
   ```

4. **Build for production**
   ```bash
   # Android APK
   flutter build apk --release
   
   # iOS
   flutter build ios --release
   ```

## Usage

### Core User Flows

1. **Browse Categories**
   - Launch app to see animated category grid
   - Tap any category to view filtered meals

2. **Explore Recipes**
   - Browse meal cards with images and metadata
   - Tap meal cards to view detailed recipes

3. **Manage Favorites**
   - Tap star icon on any recipe to add/remove favorites
   - Access favorites via bottom navigation tab

4. **Apply Filters**
   - Open drawer menu and select "Filters"
   - Toggle dietary preferences (Gluten-free, Vegan, etc.)
   - View filtered results across all screens

5. **Recipe Details**
   - View complete ingredient lists
   - Follow step-by-step cooking instructions
   - See cooking time, complexity, and cost information

## Contributing

We welcome contributions! Please follow these guidelines:

### Development Workflow

1. **Fork the repository**
   ```bash
   git https://github.com/AliAhmed015/Meals.git
   cd Meals
   ```

2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```

3. **Make your changes**
   - Follow Flutter/Dart style guidelines
   - Add tests for new functionality
   - Update documentation as needed

4. **Commit your changes**
   ```bash
   git add .
   git commit -m "feat: add amazing feature"
   ```

5. **Push to your branch**
   ```bash
   git push origin feature/amazing-feature
   ```

6. **Open a Pull Request**
   - Provide clear description of changes
   - Include screenshots for UI changes
   - Ensure all tests pass

### Code Style

- Follow [Dart Style Guide](https://dart.dev/guides/language/effective-dart/style)
- Use meaningful variable and function names
- Add comments for complex logic
- Maintain consistent formatting with `dart format`

### Commit Convention

- `feat:` New features
- `fix:` Bug fixes
- `docs:` Documentation updates
- `style:` Formatting changes
- `refactor:` Code refactoring
- `test:` Adding tests

## Future Enhancements

- **Remote API Integration** - Connect to recipe databases
- **Search Functionality** - Search recipes by name or ingredients
- **Meal Planning** - Weekly meal planning features
- **Shopping Lists** - Generate shopping lists from recipes
- **Social Features** - Share recipes and meal plans
- **Analytics** - Track cooking habits and preferences

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

**Note**: This app currently uses local dummy data for demonstration purposes. The architecture is designed to easily extend to remote APIs by modifying the providers in the `providers/` directory.
