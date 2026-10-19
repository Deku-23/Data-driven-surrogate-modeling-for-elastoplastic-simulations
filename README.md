# Data-driven-surrogate-modeling-for-elastoplastic-simulations

This repository contains the final academic report for a Master's-level project exploring the integration of deep learning with high-fidelity physics-based simulations. The study focuses on constructing fast, highly accurate surrogate models to predict the path-dependent temporal dynamics and spatial field distributions of a 2D non-linear elastoplastic system.

## Project Overview
Traditional finite element method (FEM) simulations for non-linear solid mechanics are computationally expensive, often creating bottlenecks in iterative engineering design and optimization. This project bridges conventional solid mechanics and artificial intelligence by utilizing Recurrent Neural Networks (RNNs) and Convolutional Neural Networks (CNNs) to bypass these computational limitations.

## Key Methodologies
### Physics-Based Data Generation: 
A 2D plane strain elastoplastic model implemented via the FEniCSx framework. The solver employs a radial return mapping algorithm to unconditionally stabilize plastic stress corrections across successive pseudo-time increments.

### Bayesian Active Learning: 
A multi-objective optimization routine formulated using the Ax platform and Gaussian Process (GP) surrogates to efficiently explore the design space and map the trade-off between structural stiffness and maximum deformation.

### Deep Learning Surrogates:

LSTM Network: Designed to capture the inherently path-dependent accumulation of plastic strain, predicting scalar quantities (maximum force and peak von Mises stress) across temporal loading increments.

Time-Distributed Dilated CNN: Employs exponentially increasing dilation rates to expand the receptive field without downsampling, predicting high-dimensional spatial von Mises stress contours while preserving localized stress gradients.

## Performance Highlights
The trained machine learning surrogates successfully matched the physical fidelity of the FEniCSx solver ($R^2 > 0.998$) while delivering massive computational gains. Inference times were reduced from several seconds/minutes to a few milliseconds, achieving an approximate $10^3$ acceleration factor.

## Academic Integrity Notice & Repository Contents
To comply with university academic integrity policies for active coursework, the underlying Python source code (including FEniCSx, PyTorch, and Ax implementation scripts) has been intentionally withheld from this public repository.

However, the complete methodology, mathematical formulations, network architectures, and performance analyses are fully documented in the attached project report.

https://github.com/Deku-23/Data-driven-surrogate-modeling-for-elastoplastic-simulations/blob/3654995e42af0618d33f87b4a40e444e84568e17/utlkq_DAINS_Report.pdf
