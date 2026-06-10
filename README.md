# Random Positioning Machine Simulator - Jupyter Python Version

This repository contains the Jupyter/Python version of the Random Positioning Machine (RPM) simulator.

The notebook models a two-axis RPM holding a square agar plate with Arabidopsis seedlings. It computes the gravity vector in the sample frame over time, compares simulation scenarios, checks sample-point accelerations across the plate, and generates review figures and export files.

## File

- `RPM_Simulator_Python_Notebook.ipynb` - main Jupyter notebook simulator

## What The Notebook Includes

- Static, random-walk, microgravity-optimized, and biased partial-gravity scenarios
- Two-axis gimbal kinematics with velocity and acceleration limits
- Sample-frame gravity vector calculations
- Center, corner, grid, or custom sample-point acceleration analysis
- Moving-window gravity validation
- Target checks for microgravity, Moon, Mars, or custom gravity levels
- 3D plots of the gimbal, plate, gravity path, and sampled gravity sphere
- Optional command schedule, pseudocode, CSV, and PDF report exports

## Requirements

The notebook uses common scientific Python packages:

```bash
pip install numpy pandas matplotlib ipywidgets
```

If you use Anaconda, these packages are usually already available.

## How To Run

1. Open `RPM_Simulator_Python_Notebook.ipynb` in Jupyter Notebook, JupyterLab, VS Code, or Google Colab.
2. Run the setup and function-definition cells from top to bottom.
3. Choose a preset scenario in the example run cell, such as:

```python
cfg = preset_config("microgravity")
```

Other useful presets include:

```python
cfg = preset_config("moon")
cfg = preset_config("mars")
cfg = preset_config("static")
```

4. Run the plotting and export cells to generate figures and output files.

## Notes

This repository is specifically for the Python/Jupyter notebook version. It does not include the HTML simulator.

The current notebook uses a horizontal outer RPM axis so both gimbal axes affect the sample-frame gravity vector. This allows the gravity path figure to show a true 3D trace instead of collapsing into a 2D path.
