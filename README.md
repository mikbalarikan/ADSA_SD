# ADSA_SD
ADSA_SD is an optical surface tension measurement tool for Sessile Droplet (SD). The code gets a drop image and physical properties as an input and detecs edge coordinates of a drop, solves the laplace equation numerically and optimizes the laplace solution until it fits the experimental drop profile and gives output of surface tension value.

## Axisymmetric Sessile Drop Shape Analysis (ADSA) for Surface Tension Measurement

ADSA_SD notebook demonstrates the measurement of surface tension from geometric parameters of a sessile drop by analyzing its captured image and fitting the Young-Laplace equation to the experimentally obtained droplet profile.

<a href="https://ibb.co/d4bx5c0L"><img src="https://i.ibb.co/k23vSyg9/Sessile.png" alt="Sessile" border="0"></a><br />|

### Physical Background

A pendant drop at static equilibrium is governed by the balance between gravitational forces and surface tension. This equilibrium state is mathematically described by the **Young-Laplace equation**, which relates the shape of the drop to the forces acting upon it.

### Governing Equations

The theoretical profile of the pendant drop is obtained by solving the following set of ordinary differential equations (ODEs):

1.

$$
\frac{d\varphi}{d\tilde{s}} = 2 + Bo \cdot \tilde{z} - \frac{\sin(\varphi)}{\tilde{x}}
$$

2.

$$
\frac{d\tilde{x}}{d\tilde{s}} = \cos(\varphi)
$$

3.

$$
\frac{d\tilde{z}}{d\tilde{s}} = \sin(\varphi)
$$

Where:

- $\varphi$ is the angle between the tangent to the drop profile and the horizontal axis.
- $\tilde{x}$ and $\tilde{z}$ are dimensionless coordinates normalized by the drop curvature at the apex.
- $\tilde{s}$ is the dimensionless arc length along the drop profile.
- $Bo$ is the Bond number, which characterizes the ratio of gravitational to surface tension forces.

By solving these equations and fitting the resulting theoretical profile to the experimental image, the surface tension can be accurately determined.

### Installation & User Guide for ADSA Analysis

This ADSA (Axisymmetric Drop Shape Analysis) code is provided as a Jupyter notebook (`ADSA_SD.ipynb`) and can be executed on any system (Windows, macOS, Linux) with Jupyter installed.

### Execution Guide

1. **Install Dependencies:**
   - Ensure Python is installed (recommended Python 3.7 or newer).
   - Install necessary packages:
   ```bash
   pip install numpy matplotlib pandas scipy jupyter scikit-image opencv-python
   ```

2. **Running the Notebook:**
   - Open a terminal or command prompt in the directory containing `ADSA_SD.ipynb`.
   - Launch Jupyter Notebook by typing:
   ```bash
   jupyter notebook
   ```
   - Select and open `ADSA_SD.ipynb` from your web browser.

3. **Prepare your Drop Images:**
   - Crop images closely around the droplet.
   - Ensure drop edges are sharp and clear to avoid pixel-based measurement errors.

4. **Execute the Analysis:**
   - Follow the notebook cells sequentially and execute each step.

### Required Libraries

The notebook requires the following Python libraries:
- NumPy
- Matplotlib
- Pandas
- SciPy
- scikit-image
- OpenCV (cv2)

Install them all at once with:
```bash
pip install numpy matplotlib pandas scipy scikit-image opencv-python jupyter
```

### Example Images

Example images are provided in the `example_images` folder to assist you in verifying the notebook functionality.
