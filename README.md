# ADSA_SD
ADSA_SD is an optical surface tension measurement tool for Sessile Droplet (PD). The code gets a drop image and physical properties as an input and detecs edge coordinates of a drop, solves the laplace equation numerically and optimizes the laplace solution until it fits the experimental drop profile and gives output of surface tension value.

## Axisymmetric Pendant Drop Shape Analysis (ADSA) for Surface Tension Measurement

ADSA_SD notebook demonstrates the measurement of surface tension from geometric parameters of a pendant drop by analyzing its captured image and fitting the Young-Laplace equation to the experimentally obtained droplet profile.

<a href="https://ibb.co/d4bx5c0L"><img src="https://i.ibb.co/k23vSyg9/Sessile.png" alt="Sessile" border="0"></a><br />|

### Physical Background

A pendant drop at static equilibrium is governed by the balance between gravitational forces and surface tension. This equilibrium state is mathematically described by the **Young-Laplace equation**, which relates the shape of the drop to the forces acting upon it.

### Governing Equations

The theoretical profile of the pendant drop is obtained by solving the following set of ordinary differential equations (ODEs):

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Equations Display</title>
    <script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
</head>
<body>

<!-- Equation (1) -->
<p>
\[
\frac{d\varphi}{d\tilde{s}} = 2 + Bo \cdot \tilde{z} - \frac{\sin(\varphi)}{\tilde{x}} \tag{1}
\]
</p>

<!-- Equation (2) -->
<p>
\[
\frac{d\tilde{x}}{d\tilde{s}} = \cos(\varphi) \tag{2}
\]
</p>

<!-- Equation (3) -->
<p>
\[
\frac{d\tilde{z}}{d\tilde{s}} = \sin(\varphi) \tag{3}
\]
</p>

</body>
</html>

Where:

- $\varphi$ is the angle between the tangent to the drop profile and the horizontal axis.
- $\tilde{x}$ and $\tilde{z}$ are dimensionless coordinates normalized by the drop curvature at the apex.
- $\tilde{s}$ is the dimensionless arc length along the drop profile.
- $Bo$ is the Bond number, which characterizes the ratio of gravitational to surface tension forces.

By solving these equations and fitting the resulting theoretical profile to the experimental image, the surface tension can be accurately determined.
