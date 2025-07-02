# DroneMap Route Visualizer

This Jupyter notebook provides an interactive tool for visualizing and validating drone routes on a 12x12 grid. Users can input route instructions, and the notebook will plot the path, display the grid, and check for out-of-bounds errors. This is useful for simulating and debugging drone navigation or similar grid-based movement problems.

## Features
- **Interactive Input:** Enter route instructions or load them from a file.
- **Grid Visualization:** Displays a 12x12 grid with the drone's path marked.
- **Route Validation:** Checks if the route stays within the grid boundaries and reports errors if not.
- **Coordinate Tracking:** Outputs the full list of coordinates traversed by the drone.
- **Customizable:** Easy to adapt for different grid sizes or movement rules.

## How It Works
- The user is prompted to enter route instructions (or a filename containing them).
- The notebook parses the starting coordinates and a sequence of directions (N, S, E, W).
- The path is calculated step by step, and the resulting coordinates are stored.
- The grid is displayed with the path marked, and the coordinates are printed.
- If the route goes outside the grid, an error message is shown.

## Requirements
- Python 3.6+
- Jupyter Notebook
- numpy
- pandas

Install requirements with:
```sh
pip install numpy pandas
```

## Usage
1. Open the notebook in Jupyter:
   ```sh
   jupyter notebook DroneMap.ipynb
   ```
2. Run the cells. When prompted, enter route instructions or a filename containing them.
3. The notebook will display the grid and the route, or report if the route is invalid.

## Example Input Format
- The first two lines: starting X and Y coordinates (1-12)
- Subsequent lines: directions (N, S, E, W), one per line

Example:
```
3
12
N
N
E
E
S
W
```

## Project Structure
- **get_filename:** Handles user/file input for route instructions
- **display_grid:** Draws the grid and marks the route
- **Main loop:** Processes input, calculates the path, and displays results

## Notes
- The notebook is designed for educational and prototyping purposes.
- You can adapt the grid size or movement logic by modifying the code.

## License

MIT
