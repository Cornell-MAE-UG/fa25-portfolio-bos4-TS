---
layout: project
title: Wind Turbine Blade Design
description: MAE4272 Fall 2025 -  Wind Turbine Blade Design Project
technologies: [Fudion 360, Matlab, Excel]
image: /assets/images/blade-profile-pic.jpg
---

MAE 4272 Fluids & Heat Transfer Laboratory Project

![Photo of wind turbine]({{ "/assets/images/blade-profile-pic.jpg" | relative_url }}){: .inline-image-l}

Project Overview

This project involved designing, modeling, fabricating, and experimentally testing a small-scale wind-turbine blade optimized for power generation under fixed wind-tunnel operating conditions. The design had to balance aerodynamic efficiency with structural safety while respecting several engineering constraints:

6-inch maximum blade length
1-inch hub radius compatibility
Material flexural strength limit of 55 MPa
Wind distribution governed by Weibull parameters (k = 5, c = 5)
Maximum safe operating speed of ~ 2000 RPM

Using a combination of aerodynamic modeling and bench-scale experimentation, our team iterated toward a blade design that produced reliable power, avoided free-spin that lead to structural failure, and aligned closely with theoretical performance predictions.

The final design achieved a peak experimental output of 1.33 W at 1664 RPM and operated stably across all tested wind speeds.


Design Process

Our design workflow blended analytical modeling, structural assessment, CAD development, and manufacturability considerations.

1. MATLAB Blade-Element Model

We developed a MATLAB tool to simulate aerodynamic forces and structural loads along the blade span. Key components included:

    Blade-element momentum-style aerodynamic calculations
    Lift/drag evaluation at each radial station
    Integration of tangential forces into torque predictions
    Root bending-moment estimation to check structural safety

The model solved for ree-spin rotational speed by identifying the angular velocity that produces zero net aerodynamic torque—critical for predicting maximum bending stress during overspeed conditions.

![Plot of root bending stress vs wind speed]({{ "/assets/images/BEM1.jpg" | relative_url }}){: .inline-image-l}

![Plots of chord and twist vs radius]({{ "/assets/images/geometry1.jpg" | relative_url }}){: .inline-image-l}


2. Geometry Optimization

We iterated chord and twist distributions—especially in the outer 40% of the span—to reduce root bending stress while maintaining strong aerodynamic performance. This optimization ensured:

    Free-spin stress remained below the PLA material limit
    The blade retained smooth aerodynamic loading
    The blade operated efficiently across the 8–11 Hz test range

3. CAD Development in Fusion 360

To ensure manufacturability:

    We imported NACA 4412 profiles for 11 radial stations
    Applied twist about the quarter-chord point
    Generated smooth lofts using guide curves
    Produced a printable, structurally consistent blade design

This resulted in a clean, accurate 3D model ready for fabrication.

![Photo of CAD]({{ "/assets/images/CAD.jpg" | relative_url }}){: .inline-image-l}

Testing Summary


Pre-test procedure

1. Inspected blade integrity and mounting
2. Installed blades onto the hub using clay to ensure secure fastening
3. Ensuring wind tunnel is clear of obstruction or other electrical/mechanical hazards

Testing

We ramped up the wind tunnel from 0 to 8Hz and recorded data when the turbine began to spin. Next we incrementally increased torque-brake voltage by 0.25V until stall, recording RPM, torque, and electrical power at each operating point.
 
This process was repeated for 9, 10, and 11 Hz wind-tunnel settings (≈4.6–6.3 m/s). 

Performance Results

    Peak power: 1.33 W @ 1664 RPM (11 Hz)
    Average peak across all runs: 0.712 W @ 1557 RPM
    Stable rotation across all frequencies, with no structural failures
    Model predictions aligned with experimental trends, though MATLAB overestimated torque at high tip-speed ratios
    Testing was limited near 2000 RPM due to lab safety protocols

The compiled power-RPM curves showed consistent aerodynamic behavior, with clear and repeatable peak-power points.

![Plot of superimposed power curves]({{ "/assets/images/powercurves.jpg" | relative_url }}){: .inline-image-l}

![Plots of power curves and power+RPM values]({{ "/assets/images/powercurves+power.jpg" | relative_url }}){: .inline-image-l}

My Contribution

In this team project, I contributed to several key phases of the engineering workflow:

    MATLAB Modeling & Analysis

    Helped refine the blade-element model used for torque and bending-stress predictions
    Analyzed free-spin behavior and ensured geometry met material constraints

    Geometry Translation for CAD prep

    Converted optimized chord/twist distributions into a manufacturable Fusion 360 model
    Generated smooth aerodynamic surfaces using multi-section sweeps and guide curves

    Experimental Testing & Data Interpretation

    Executed pre-test inspection for wind-tunnel testing, ensuring safe operation and consistent measurements
    Operated DAQ for error-free data collection 

    Technical Documentation

    Developed clear summaries of results, model assumptions, and design tradeoffs
    Contributed to the final engineering report and visualizations

Overall, my work bridged modeling, CAD, and experimental validation to support a blade design that met performance goals and demonstrated strong agreement with theoretical expectations.


