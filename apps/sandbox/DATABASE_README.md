# Simple Database Example

This is a simple database application built with Expo and SQLite. It demonstrates basic CRUD (Create, Read, Update, Delete) operations using the `expo-sqlite` package.

## Features

- **Add Items**: Create new items with a name and optional description
- **View Items**: See all stored items in a list
- **Delete Items**: Remove individual items from the database
- **Clear All**: Delete all items at once with confirmation
- **Persistent Storage**: Data is stored locally using SQLite and persists between app sessions

## Database Schema

The app uses a simple SQLite table:

```sql
CREATE TABLE items (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  name TEXT NOT NULL,
  description TEXT
);
```

## Technologies Used

- **Expo**: Framework for building React Native apps
- **expo-sqlite**: SQLite database integration for Expo
- **expo-router**: File-based routing for navigation
- **React Native**: UI components

## Running the App

1. Install dependencies:
   ```bash
   yarn install
   ```

2. Start the development server:
   ```bash
   yarn start
   ```

3. Run on your preferred platform:
   - iOS: Press `i` or run `yarn ios`
   - Android: Press `a` or run `yarn android`
   - Web: Press `w`

## Code Structure

- `app/index.tsx`: Main component with database logic and UI
- `app/_layout.tsx`: Root layout configuration for expo-router
- Database operations include:
  - Initialize database and create table
  - Insert new items
  - Query all items
  - Delete specific items
  - Clear all items

## How It Works

1. **Database Initialization**: On app load, the database is opened and a table is created if it doesn't exist
2. **Adding Items**: Users can enter a name and description, which are inserted into the database
3. **Displaying Items**: All items are fetched from the database and displayed in a list
4. **Deleting Items**: Users can delete individual items or clear all items at once
5. **Data Persistence**: All data is stored locally using SQLite, so it persists even when the app is closed

## Example Usage

1. Open the app
2. Enter an item name (e.g., "Buy groceries")
3. Optionally add a description (e.g., "Milk, eggs, bread")
4. Tap "Add Item"
5. The item appears in the list below
6. Tap "Delete" to remove a specific item
7. Tap "Clear All" to remove all items (with confirmation)

This example demonstrates the basics of working with a local SQLite database in an Expo app, providing a foundation for building more complex data-driven applications.
