# Deep Learning-Driven Classification of Urban Road Network Morphology in Colombo, Sri Lanka
## Objective
This project aims to classify and analyze the road network morphology of Colombo, Sri Lanka, using a deep learning-driven methodology adapted from Chen et al. (2024). By customizing and applying the open-source codebase developed by the Urban Analytics Lab of NUS, this study employs a Convolutional Neural Network (ResNet-34) to automatically recognize and categorize urban road patterns at multiple spatial scales.

Unlike traditional manual classification methods, this data-driven and scalable approach extracts learned spatial features from thousands of street layouts across global cities, enabling a systematic, transferable framework for exploring embedded planning logics. The model classifies road morphology into six typologies: Gridiron, Linear, Nopattern (irregular), Organic, Radial, and Tributary, offering insights into the historical, functional, and spatial dynamics of Colombo’s urban fabric.

By adapting this novel method to the Sri Lankan urban context, the study contributes to the growing body of work applying AI-powered spatial analysis tools in the Global South, where such automated urban morphology classifications remain limited.

<img width="1040" height="1390" alt="image" src="https://github.com/user-attachments/assets/34c972d9-b258-4019-ac61-3bbd8624755d" />

## Methodology
The workflow consists of two main phases:

### 1. CRHD Generation
Gridded vector tiles of Colombo were generated and used to extract road networks using OpenStreetMap data. CRHD images were created by plotting road segments with varying widths and colors depending on road hierarchy. These images capture the spatial configuration of roads within each grid.

**Tools Used:**
- `osmnx`
- `geopandas`
- `matplotlib`
  

### 2. Morphology Classification
The generated CRHD images were classified using a pretrained **ResNet-34** model trained on 144 global cities. The model outputs class probabilities and assigns each grid cell to the most likely road pattern.

**Tools Used:**
- TensorFlow 2.7.0
- OpenCV
- Keras-based classification models
- Pretrained weights: `ResNet-34-6class-aug5.h5`

## Reference
This implementation is based on the methodology and code developed by:

**Chen, W., Huang, H., Liao, S., Gao, F., & Biljecki, F. (2024).**  
*Global urban road network patterns: Unveiling multiscale planning paradigms of 144 cities with a novel deep learning approach.*  
_Landscape and Urban Planning, 241, 104901._  
[https://doi.org/10.1016/j.landurbplan.2023.104901](https://doi.org/10.1016/j.landurbplan.2023.104901)

The codebase is available at the Urban Analytics Lab’s GitHub repository:  
[https://github.com/ualsg/urban-road-morphology](https://github.com/ualsg/urban-road-morphology)


## Notes

1. This project showcases the adaptability of global urban morphology modeling techniques in the context of Sri Lankan cities.
2. The outputs can support urban planning, comparative spatial analysis, and further research into spatial configurations of cities in the Global South.



