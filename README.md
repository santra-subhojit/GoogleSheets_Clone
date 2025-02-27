# Google Sheets Clone

A web application mimicking the Google Sheets UI and core functionalities. This project focuses on replicating the look and feel of Google Sheets along with key functionalities such as mathematical operations, data quality functions, drag selection, cell formatting, and more.

## Table of Contents

- [Objective](#objective)
- [Features](#features)
- [Tech Stack and Data Structures](#tech-stack-and-data-structures)
- [Installation](#installation)
- [Usage](#usage)
- [Commands](#commands)
- [Testing](#testing)
- [Bonus Features](#bonus-features)
- [Evaluation Criteria](#evaluation-criteria)
- [Contributing](#contributing)
- [License](#license)

## Objective

Develop a web application that closely mimics the user interface and core functionalities of Google Sheets. The main focus areas include:

- Mathematical and data quality functions
- Data entry and validation
- Key UI interactions (drag selection, cell dependencies, and formatting)

## Features

1. **Spreadsheet Interface:**
   - **Google Sheets UI Mimicry:** Closely replicates the visual design, layout, toolbar, formula bar, and cell structure.
   - **Drag Functions:** Implements drag functionality for cell content, formulas, and multi-cell selections.
   - **Cell Dependencies:** Formulas reflect and update based on cell dependencies.
   - **Cell Formatting:** Support for bold, italics, font size, color, and alignment.
   - **Row/Column Operations:** Ability to add, delete, and resize rows and columns.

2. **Mathematical Functions:**
   - **SUM:** Calculates the sum of a range of cells.
   - **AVERAGE:** Calculates the average of a range of cells.
   - **MAX:** Returns the maximum value from a range of cells.
   - **MIN:** Returns the minimum value from a range of cells.
   - **COUNT:** Counts the number of cells containing numerical values.

3. **Data Quality Functions:**
   - **TRIM:** Removes leading and trailing whitespace from a cell.
   - **UPPER:** Converts cell text to uppercase.
   - **LOWER:** Converts cell text to lowercase.
   - **REMOVE_DUPLICATES:** Removes duplicate rows from a selected range.
   - **FIND_AND_REPLACE:** Finds and replaces specific text within a range of cells.

4. **Data Entry and Validation:**
   - Supports multiple data types (text, numbers, dates).
   - Basic validation to ensure numeric cells contain numbers.

5. **Data Visualization:**
   - Charting functionality that visualizes data from selected cells.

6. **Persistence:**
   - Ability to save and load spreadsheets using local storage.

7. **Undo/Redo:**
   - Basic history tracking for reverting changes and reapplying undone actions.

## Tech Stack and Data Structures

- **Frontend Framework:** React  
  _Chosen for its component-based architecture, efficient state management with hooks, and strong community support for building interactive UIs._

- **Charting Library:** Chart.js (via react-chartjs-2)  
  _Used for creating dynamic data visualizations (charts/graphs) within the spreadsheet._

- **Styling:** Custom CSS  
  _The styling is carefully crafted to mimic Google Sheets with responsive design, custom scrollbars, and smooth transitions._

- **Data Structures:**
  - **Grid State:**  
    The spreadsheet grid is stored as an object where each key is in the format "row,col" (e.g., "0,0"). Each cell object contains:
    - `value`: The current displayed value.
    - `formula`: The formula used to calculate the value.
    - `style`: An object for cell styling (font properties, color, alignment, etc.).
    - `dataType`: The type of data (e.g., "text", "number", "date").  
    _This structure allows fast lookup and granular updates to individual cells, which is key for managing cell dependencies and efficient rendering._

- **Local Storage:**  
  Used to persist spreadsheet data across sessions.

- **Version Control:** Git

## Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/your-username/google-sheets-clone.git
cd google-sheets-clone
npm install
```

or if you use Yarn:

```bash
yarn install
```

## Usage

Start the development server:

```bash
npm start
```

or

```bash
yarn start
```

Then, open [http://localhost:3000](http://localhost:3000) in your browser.

## Commands

- **Start Development Server:**
  ```bash
  npm start
  ```
- **Build for Production:**
  ```bash
  npm run build
  ```
- **Run Tests:**
  ```bash
  npm test
  ```
- **Lint Code:**
  ```bash
  npm run lint
  ```

## Testing

- **Data Entry:**  
  Enter numbers, text, and dates into cells.
  
- **Formulas:**  
  Use formulas (e.g., `=SUM(A1:A5)`, `=AVERAGE(B1:B5)`) to test mathematical functions.
  
- **Formatting:**  
  Apply bold, italics, underline, font size, color, and alignment using toolbar buttons.
  
- **Row/Column Operations:**  
  Add, delete, and resize rows/columns.
  
- **Save/Load:**  
  Save your spreadsheet to local storage and load it back.
  
- **Charts:**  
  Select cells and click the chart button to view data visualizations.

## Bonus Features

- Additional mathematical and data quality functions.
- Support for complex formulas with relative and absolute cell references.
- Enhanced cell dependency management.
- Undo/Redo functionality.

## Evaluation Criteria

- **UI Fidelity:**  
  The application’s look and feel closely replicate Google Sheets, including drag selection and cell dependency handling.

- **Functionality:**  
  All features—from basic cell editing to advanced formula calculations—should work as expected.

- **Code Quality:**  
  The code is modular, maintainable, and well-documented.

- **Usability:**  
  The user interface is intuitive, responsive, and accessible.

- **Bonus Features:**  
  Extra functionalities (e.g., complex formulas, dynamic charts, save/load) further enhance the user experience.

## Contributing

Contributions are welcome! Please fork the repository and open a pull request. For major changes, please open an issue first to discuss your ideas.

## License

This project is licensed under the [MIT License](LICENSE).

