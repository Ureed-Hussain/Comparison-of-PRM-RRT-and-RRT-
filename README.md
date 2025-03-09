# README: Path Planning in 3D with PRM, RRT, and RRT*

## Overview
This project implements and compares three sampling-based motion planning algorithms—Probabilistic Roadmap (PRM), Rapidly-exploring Random Tree (RRT), and RRT*—in a 3D MATLAB environment. The workspace includes polygonal (cubic) and cylindrical obstacles, simulating a realistic robotic navigation scenario.

## Features
- **3D Environment Setup**: Includes obstacle generation with configurable positions and sizes.
- **PRM Implementation**: Constructs a roadmap and finds a feasible path using graph-based search.
- **RRT Implementation**: Grows a tree from the start position to explore the space and find a feasible path.
- **RRT* Implementation**: Optimized version of RRT that refines the path for efficiency.
- **Visualization**: Plots the 3D workspace, obstacles, and generated paths.

## Requirements
- MATLAB (tested on R2023a and later)
- MATLAB toolboxes:
  - Robotics Toolbox (recommended)
  - Optimization Toolbox (for RRT* performance improvements)

## Installation
1. Clone this repository:
2. Open MATLAB and navigate to the project directory.
3. Run the main script:
   ```matlab
   ```

## Usage
### Configurations
Modify the parameters in `config.m` to customize:
- Start and goal positions
- Number of samples (for PRM)
- Maximum iterations (for RRT and RRT*)
- Step size and rewire radius (for RRT*)

### Running Different Algorithms
Execute the corresponding script for each planner:
```matlab
run_PRM.m   % Runs PRM planner
run_RRT.m   % Runs RRT planner
run_RRTstar.m % Runs RRT* planner
```

## Results
### Test Cases
#### **Test 1: PRM with 500 Nodes**
- Successfully found a path in **0.85s**.
- Generated a smooth, short path with minor detours around obstacles.

#### **Test 2: RRT with Step Size 0.5**
- Successfully found a path in **1.3s**.
- Path was suboptimal, with sharp turns requiring smoothing.

#### **Test 3: RRT* with Step Size 0.5 and Rewire Radius 1.0**
- Successfully found an optimized path in **2.5s**.
- Path length reduced significantly compared to RRT.
- Additional computation time for optimization.

## Future Improvements
- Implement heuristic-based path smoothing for RRT.
- Test with dynamic obstacles.
- Optimize node connections in PRM for faster computations.

## Contributors
- **Ureed Hussain**

## License
This project is open-source.

