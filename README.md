# Shortest Path Finding System for DAA

A Python-based graphical application that helps users create a weighted graph and find shortest paths between vertices. It provides an interactive interface built with **Tkinter** and demonstrates two classic graph algorithms: **Dijkstra's Algorithm** and **Floyd–Warshall Algorithm**.

## Features

- **Add vertices:** Create graph nodes using custom names such as `A`, `B`, or `City1`.
- **Add weighted edges:** Connect two existing vertices and assign a numeric weight.
- **Undirected connections:** Each edge can be travelled in either direction.
- **Single-source shortest path:** Use Dijkstra's Algorithm to calculate shortest distances from a selected source vertex.
- **All-pairs shortest paths:** Use Floyd–Warshall Algorithm to calculate shortest distances between every pair of vertices.
- **Graph visualization:** View the graph and its weighted connections in the application.
- **Input validation:** Handles missing vertices, invalid weights, and negative weights with helpful messages.
- **Interactive GUI:** Enter graph details and view results without needing to edit the algorithm code.

## Algorithms Used

### 1. Dijkstra's Algorithm

Dijkstra's Algorithm finds the shortest distance from one source vertex to all reachable vertices in a weighted graph with **non-negative edge weights**. This implementation uses Python's `heapq` priority queue.

**Time complexity:** Typically `O((V + E) log V)` with an adjacency-list representation and a priority queue.

### 2. Floyd–Warshall Algorithm

Floyd–Warshall calculates the shortest distances between **all pairs of vertices** by checking whether travelling through an intermediate vertex gives a shorter route.

**Time complexity:** `O(V³)`  
**Space complexity:** `O(V²)`

Here, `V` is the number of vertices and `E` is the number of edges.

## Technologies Used

- **Language:** Python
- **GUI:** Tkinter
- **Data structure:** Adjacency dictionary (graph representation)
- **Priority queue:** `heapq`
- **Notebook format:** Jupyter Notebook (`.ipynb`)

## Requirements

- Python 3
- Tkinter (usually included with standard Python installations)
- Jupyter Notebook or JupyterLab, if running the `.ipynb` file

No additional pip packages are required by the project.

## How to Run

### Option 1: Run the Jupyter Notebook

1. Download or clone this repository.
2. Open `Shortest_Path_Finding_System_Fixed.ipynb` in Jupyter Notebook or JupyterLab.
3. Run the notebook cells in order.
4. The Shortest Path Finding System window should open.

> **Note:** Tkinter needs access to a desktop display. GUI windows may not open in cloud notebooks or headless environments. If you are using Jupyter and the window does not appear, try running the project in a local Python environment on your computer.

### Option 2: Run as a Python Script

If you save the application code as `shortest_path_finding_system.py`, run it from a terminal:

```bash
python shortest_path_finding_system.py
```

## How to Use

1. **Add vertices** one by one.
2. **Add edges** by entering the source vertex, destination vertex, and a non-negative weight.
3. **Find a shortest path** by selecting or entering the source and destination vertices, then running Dijkstra's Algorithm.
4. **View all-pairs distances** by selecting the Floyd–Warshall option.
5. Review the output shown in the results area and the graph visualization.

### Example Graph

Add these vertices:

`A`, `B`, `C`, `D`

Then add these weighted edges:

| Source | Destination | Weight |
|---|---|---:|
| A | B | 4 |
| A | C | 1 |
| C | B | 2 |
| B | D | 1 |
| C | D | 5 |

For the path from **A to D**, the shortest route is:

`A → C → B → D`

Total distance:

`1 + 2 + 1 = 4`

Use this example to check that the application reports the expected shortest distance.

## Project Structure

```text
Shortest-Path-Finding-System/
├── Shortest_Path_Finding_System_Fixed.ipynb
└── README.md
```

## Important Notes

- This project models an **undirected weighted graph**.
- Edge weights must be numeric and non-negative because Dijkstra's Algorithm does not support negative edge weights.
- If two vertices are disconnected, no path exists between them.
- If the same edge is entered again with a different weight, the latest entered weight is used.
- The example above is intended for testing the algorithm; enter its vertices and edges into the application before checking the result.

## Learning Outcomes

By building and using this project, you can practise:

- Graph representation using adjacency lists
- Priority queues and `heapq`
- Dijkstra's shortest-path algorithm
- Floyd–Warshall's dynamic programming approach
- Tkinter GUI development
- Input validation and displaying algorithm results

## Future Improvements

- Highlight the selected shortest route directly on the graph.
- Support directed graphs as an optional mode.
- Add graph import/export using CSV or JSON.
- Allow users to save and load graph configurations.
- Add more shortest-path test cases and automated tests.

## Author

**Amruta Hanmant Chavan**

---

If you find this project useful for learning graph algorithms, feel free to ⭐ the repository.
