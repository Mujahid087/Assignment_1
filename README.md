# Google Sheets Clone:

> A spreadsheet editing app build using Reactjs.


## Features:

1. Editing cells.
2. Applying styles to cells.
   1. Bold.
   2. Italic.
   3. Underline.
   4. Alignment (left, center, right)
   5. Font Family.
   6. Font Size.
   7. Color.
   8. Background Color.
3. Creating and Editing multiple sheets.
4. Formula Evaluation.
   1. Dependent cell value change causes other cell which are dependent on this to update as well.
   2. Changing the cell contents of a cell directly removes the formula from the content cell directly.
   3. Formula Evaluation does not support unary operators. eg to do 10 _ (-20) write the formula as 10 _ (0 - 20) {unary '-' is not supported}
5. Conversion of sheets to json and reading from json.
6. Copying and Pasting of a Single Cell (including formula and styles if any)

#### Maybe in Future (Raise PR if you want to do it.):

1. Multi-cell copy paste.
2. Export/Import CSVs.
3. App currently passes down state and dispaatch function as props modify so that it uses context
4. App currently has two different kind of states, merge into one.
5. Remove hacky ways to show alert.
6. Maybe possible to optimize rerendering using useCallback, useMemo, React.memo. (I am not sure how.)

#### Some Insights:

- Optimization:
  - A lot of optimizations were made to how each component should render so as to avoid re rendering of complete app whenever a single cell is being edited.
  - Multiple changes were made to how the state was being stored so as to make the optimizations.
  - React.memo was used to make sure re rendering is done properly and when required.
- CSS:
  - Flexbox is used heavily.
  - Some tricks involving opacity set to 0, to hide a component but make sure it's clickable etc were used to display icons for color changing.
- Using infix to postfix conversion and postfix evaluation to parse and evaluate the formula.
- DFS Cycle detection was used to detect if some formula is recursive in nature or not.



# Project Setup and Running Instructions

## How to Run the Project

Follow these steps to set up and run the project:

### 1. Navigate to the Project Directory
First, move to the `Assignment_1` folder:
```sh
cd Assignment_1
```

### 2. Navigate to the React App Directory
Then, go to the `my-app` directory:
```sh
cd my-app
```

### 3. Install Dependencies
Install all the required dependencies:
```sh
npm install
```

### 4. Start the Development Server
To run the project in development mode:
```sh
npm start
```

This will start the React application, and you can view it in your browser at:
```
http://localhost:3000
```

## Additional Commands

### Build the Project
To create a production build:
```sh
npm run build
```

### Deploy with GitHub Pages
If using `gh-pages` to deploy:
```sh
npm run deploy
```

Happy coding! 🚀

