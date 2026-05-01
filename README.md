# Weibull-Based Tephra Decay Models
Inspired by Bonadonna & Costa (2013; https://doi.org/10.1007/s00445-013-0742-1).

## About the model
- Estimate eruption plume height, and plume stability
- An approach to Mass eruption rate (MER)
- Understanding vent location and dispersal axis

## 1. Overview
This repository applies the Weibull (Rosin–Rammler) functional form to describe the spatial decay of three tephra-fall properties:

- Deposit thickness
- Maximum lithic size (ML)
- Median grain size (Mdϕ)

All three variables share the same mathematical structure, differing only in parameter sets.

## 2. Weibull Parameters
Each Weibull curve is defined by three parameters:

- θ : scaling constant (controls magnitude)
- λ : characteristic decay length scale (km)
- n : shape parameter (controls curvature and tail behavior)

These parameters reflect eruption intensity, column height, wind field, and particle settling dynamics.

## 3. Contour Types and Distance Proxy
Field measurements are extracted from three contour types:

- Isopachs → thickness (cm)
- Isopleths → maximum lithic size (cm)
- Isogrades → median grain size (ϕ)

Because contours enclose areas, the distance variable is defined as:

$$ x = \sqrt{A} $$

where A is the area enclosed by the contour. This provides a shape-independent proxy for radial distance.

## 4. Deposit Shapes and Eruption Styles
Different eruption styles produce distinct contour geometries:

- Plinian / Subplinian → elongated isopachs due to strong wind advection
- Vulcanian / small explosive → compact, near-circular isopachs
- Phreatomagmatic → irregular or lobate patterns due to variable column height
- Coarse clast isopleths → typically more circular (less wind influence)
- Mdϕ isogrades → smooth, intermediate shapes reflecting integrated fining trends

Using sqrt(A) normalizes these geometric differences into a single decay coordinate.

## 5. Weibull Equations

### 5.1 Thickness
$$
T(x) = \theta_{th} \left( \frac{x}{\lambda_{th}} \right)^{n_{th}-2}
\exp\left[-\left( \frac{x}{\lambda_{th}} \right)^{n_{th}} \right]
$$

### 5.2 Maximum Lithic Size
$$
ML(x) = \theta_{ML} \left( \frac{x}{\lambda_{ML}} \right)^{n_{ML}-2}
\exp\left[-\left( \frac{x}{\lambda_{ML}} \right)^{n_{ML}} \right]
$$

### 5.3 Median Grain Size
$$
Md\phi(x) = \theta_{Md\phi} \left( \frac{x}{\lambda_{Md\phi}} \right)^{n_{Md\phi}-2}
\exp\left[-\left( \frac{x}{\lambda_{Md\phi}} \right)^{n_{Md\phi}} \right]
$$

where Y is thickness, ML, or Mdϕ.

## 6. Interpretation
- λ increases with eruption size and dispersal power.
- n controls whether the curve behaves more like a power law (low n) or exponential (high n).
- θ scales the overall magnitude of the deposit property.

## Rayleigh Case (n = 2)

When the Weibull shape parameter equals n = 2, the decay law reduces to the
Rayleigh form. In this case, the general Weibull equation becomes:

$$
Y(x) = \theta \exp\left[-\left(\frac{x}{\lambda}\right)^2\right]
$$

This applies to all three variables (thickness, maximum lithic size, and
median grain size), since they share the same Weibull structure.

### Implication
A Rayleigh-type decay indicates smooth, Gaussian-like thinning consistent with
a well-mixed umbrella cloud. This behavior is typical of Plinian or strong
Subplinian eruptions, where turbulent mixing dominates over wind distortion
and ballistic settling.

*Made with ❤️ for the volcanology community*
