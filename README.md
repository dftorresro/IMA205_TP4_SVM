# Object Tracking Particle Filter

Particle Filter framework for robust object tracking in video sequences, featuring customizable state propagation, resampling techniques, and innovative appearance models based on Mean Squared Error and color histogram comparisons for high-accuracy localization and tracking.

## Features

- **State Propagation**: Models the dynamics of the object movement and updates particle states accordingly.
- **Resampling**: Addresses particle degeneracy and maintains a diverse particle set.
- **Likelihood Calculation**: Employs two methods, MSE and color histogram comparison, to weigh particles based on their resemblance to the target object.
- **Adaptive Tuning**: Allows for dynamic adjustment of parameters like λ to accommodate varying tracking conditions.

## Installation

Ensure that you have Python installed along with the necessary libraries: NumPy, OpenCV, and Matplotlib.

## Usage

1. Initialize the particle filter with the dimensions of the state, the number of particles, and the τ parameter.
2. Set the initial particle states to match the location and size of the object in the first frame.
3. Run the particle filter loop: resample, predict, update with measurements, and compute the state expectation.
4. The likelihood maps can be visualized for different λ values to fine-tune the appearance models.

The provided Jupyter notebook `TP_SVM.ipynb` contains detailed examples and visualizations of the tracking process.

## Appearance Models

- **MSE Model**: Direct pixel value comparison between the template and candidate patches.
- **Histogram Model**: HSV color space histogram comparison discarding the 'Value' channel to reduce sensitivity to lighting.
