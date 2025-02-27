# Google Sheets Clone

> A spreadsheet editing app built using React.js.

## Tech Stack

- **Frontend:** React.js, HTML, CSS
- **UI Library:** Material-UI (MUI)
- **State Management:** Immer
- **Testing:** React Testing Library, Jest

## Dependencies

```json
"@emotion/react": "^11.14.0",
"@emotion/styled": "^11.14.0",
"@mui/icons-material": "^5.16.14",
"@mui/material": "^5.16.14",
"@testing-library/dom": "^10.4.0",
"@testing-library/jest-dom": "^5.17.0",
"@testing-library/react": "^13.4.0",
"@testing-library/user-event": "^13.5.0",
"immer": "^10.1.1",
"react": "^18.3.1",
"react-dom": "^18.3.1",
"react-scripts": "^5.0.1",
"web-vitals": "^2.1.4"
```

## Features

1. Editing cells.
2. Applying styles to cells.
   1. Bold.
   2. Italic.
   3. Underline.
   4. Alignment (left, center, right).
   5. Font Family.
   6. Font Size.
   7. Color.
   8. Background Color.
3. Creating and Editing multiple sheets.
4. Formula Evaluation.
   1. Dependent cell value change causes other cells that depend on it to update as well.
   2. Changing the contents of a cell directly removes the formula from that cell.
   3. Formula evaluation does not support unary operators (e.g., to compute `10 * (-20)`, write `10 * (0 - 20)`).
5. Conversion of sheets to JSON and reading from JSON.
6. Copying and pasting of a single cell (including formulas and styles if any).

## Future Enhancements (Contributions Welcome!)

1. Multi-cell copy-paste.
2. Export/Import CSVs.
3. Refactor state management using React Context API.
4. Merge two different state types into one.
5. Improve alert handling (remove hacky implementations).
6. Optimize re-rendering using `useCallback`, `useMemo`, and `React.memo`.

## Insights

- **Optimization:**
  - Optimized rendering to ensure minimal re-renders when editing a single cell.
  - Improved state management to enhance performance.
  - Utilized `React.memo` to prevent unnecessary re-renders.
- **CSS Tricks:**
  - Heavy use of Flexbox.
  - Used `opacity: 0` to hide elements while keeping them interactive (e.g., color picker icons).
- **Formula Parsing:**
  - Used **infix-to-postfix conversion** and **postfix evaluation** to parse formulas.
  - Implemented **DFS Cycle Detection** to detect recursive formulas.

## Project Setup and Running Instructions

### How to Run the Project

1. Navigate to the project directory:
   ```sh
   cd Assignment_1
   ```
2. Move to the React app directory:
   ```sh
   cd my-app
   ```
3. Install dependencies:
   ```sh
   npm install
   ```
4. Start the development server:
   ```sh
   npm start
   ```
   The app will be available at:
   ```
   http://localhost:3000
   ```

### Additional Commands

- **Build the Project:**
  ```sh
  npm run build
  ```
- **Deploy with GitHub Pages:**
  ```sh
  npm run deploy
  ```

Happy coding! 🚀


