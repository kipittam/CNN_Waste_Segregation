# **Waste Material Segregation for Improving Waste Management**

## **Objective**
The objective of this project is to implement an effective waste material segregation system using convolutional neural networks (CNNs) that categorises waste into distinct groups. This process enhances recycling efficiency, minimises environmental pollution, and promotes sustainable waste management practices.

The key goals are:

* Accurately classify waste materials into categories like cardboard, glass, paper, and plastic.
* Improve waste segregation efficiency to support recycling and reduce landfill waste.
* Understand the properties of different waste materials to optimise sorting methods for sustainability.

  ## **Data Understanding**

The Dataset consists of images of some common waste materials.

1. Food Waste
2. Metal
3. Paper
4. Plastic
5. Other
6. Cardboard
7. Glass

**Data Description**

* The dataset consists of multiple folders, each representing a specific class, such as `Cardboard`, `Food_Waste`, and `Metal`.
* Within each folder, there are images of objects that belong to that category.
* However, these items are not further subcategorised. <br> For instance, the `Food_Waste` folder may contain images of items like coffee grounds, teabags, and fruit peels, without explicitly stating that they are actually coffee grounds or teabags.


## Results and Analysis

#### Data Insights:
- The given dataset has various categories - ['Cardboard' 'Food_Waste' 'Glass' 'Metal' 'Other' 'Paper' 'Plastic'] that contains images in .PNG format.
- The given dataset is imabalnced as 'Plastic' categorie has highest number of images whereas the lowest recorded in "Cardboard' folder.
- This imbalance in the dataset will affect model performance unless you treat them with other techniques like data augumentation.
- The given categories are encoded into numeric values to process in model.


### Model specifications:
    - Contains 3 Convolutional layers with activation - relu
    - The above layer is followed by the repspective batch normalization and max-pooling layers
    - Fully connected layers were used for classification while softmax activation for multi-class classification.

### Training Specifications:
    - Used ADAM optimizer and Categorical cross-Entropy loss.
    - To prvent overfitting, Early Stopping, model checkpointing and learning rate reduction callbacks were used.

### Performace Metics:
- Accuary  :  ~ 65% on Test set
- Precision:  ~ 66%
- Recall   :  ~ 65%
- F1 Score :  ~ 65%
- Classification Matrix : As per the classification chat, "Plastic" and "Food Waste" are classified more accurately in this model.
- Confusion Matrix : As per the Confusion matrix, "Card board" and "Plastic" are classified more accurately in this model.


## Conclusion

1. **Data-related Improvements**
   - Implement data augmentation to address class imbalance
   - Collect more samples for underrepresented classes (especially Cardboard)
   - Include more diverse images within each category

2. **Model Enhancements**
   - Experiment with deeper architectures or pre-trained models
   - Implement class weights to handle imbalanced data
   - Try different optimization strategies and hyperparameters

3. **Practical Applications**
   - Could be integrated into automated waste sorting systems
   - Potential for mobile applications for consumer waste sorting
   - Useful for recycling facilities and waste management education

This demonstrates the potential of CNN-based approaches for waste segregation while highlighting areas for future improvement in both data collection and model architecture.

## References Used:
1. Upgrads Content & Started Notebook
2. [Image Preprocessing in TensorFlow](https://www.tensorflow.org/tutorials/load_data/images)
3. [Build TensorFlow input pipelines](https://www.tensorflow.org/guide/data)
4. [Understanding One-Hot Encoding](https://towardsdatascience.com/understanding-one-hot-encoding-and-its-importance-in-machine-learning-cf8fb0ab73b4)
5. [Building a CNN in Keras](https://www.tensorflow.org/tutorials/images/cnn)
6. [Evaluating Classification Models](https://machinelearningmastery.com/classification-accuracy-is-not-enough-more-performance-measures-you-can-use/)
   

