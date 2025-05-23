# Multi-Arms-MRT-Sample-Size-Calculator

**Modified from:** [MRT-SS Calculator: A Sample Size Calculator for Micro-Randomized Trials](https://d3center.shinyapps.io/mrt-ss-calculator/) by Liao et al. (2016)  
**ArXiv:** [MRT-SS Calculator: An R Shiny Application for Sample Size Calculation in Micro-Randomized Trials](https://arxiv.org/abs/1609.00695)

## Key Enhancements

### Enhanced Multi-Arm Flexibility
- The original MRT-SS calculator focused on two-arm trials or assumed equal allocation across arms.  
- This implementation supports any number of arms (K ≥ 2) and automatically computes the variance term for multi-arm comparisons.

## Description

The `mrt_sample_size()` function computes the required sample size for a micro-randomized trial (MRT) focused on a standardized proximal outcome. You provide:

- **Number of intervention arms** (`k`)  
- **Trial duration** (`days`)  
- **Decision points per day**  
- **Expected availability**  
- **Minimum detectable effect size**  
- **Custom randomization probability vector**  

The function then:

1. Derives the variance of the randomized treatment indicator  
2. Applies the large-sample MRT sample-size formula  
3. Optionally adds a “+2” small-sample correction to match the MRT-SS Shiny Calculator  
