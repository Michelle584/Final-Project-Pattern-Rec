<!-- PROJECT LOGO -->
<br />
<p align="center">
  <h3 align="center">Scene Classificiation with Aerial Images</h3>


<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
    </li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#dependencies">Dependencies</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
   </li>
    <li><a href="#license">License</a></li>
    <li><a href="#authors">Authors</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

Aerial scene classification aims to automatically label an image taken above the Earth and place it into a category. These images can be anything from an urban setting to a mountain. Using some of the classes from the Aerial Image Dataset (AID), which contains more than ten thousand aerial scenes and their corresponding labels, a classification framework is developed.

Transfer learning and a CNN neural network built from TensorFlow are used and compared. The Transfer learning network showed significantly more accuracy over the CNN built from scratch, likely due to amount of neurons. In addition, to see the impact on the accuracy, 50% and 80% of the data was removed randomly from the transfer learning model, resulting in about a 7% decrease in accuracy with 50% removed and a 11% decrease in accuracy with 80% removed. Finally, the LIME technique is applied to some custom test images to explain the prediction of five of the different classes. The method is able to extract the areas that were most important in classification and for the most part, correctly isolated important areas in the images.

<!-- GETTING STARTED -->
## Getting Started
### Dependencies
This was implemented in Jupyter notebook through HiPergator. The training notebook Training.ipynb uses the Tensorflow-2.7.0 kernel. The test notebook, Test.ipynb, uses UFRC Python-3.10. 

To make the labels from the images, I simply used a regular Python 3 kernel. The labels are already generated in .npy files for use though. 

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/Michelle584/Final-Project-Pattern-Rec.git
   ```
<!-- USAGE EXAMPLES -->

You will also need the training models in a separate zip folder I attatched the assignment (unless you want to retrain. Yuck) There should be three models, as well as the scratch_trained_cnn.hdf5 that is within the repository already. They couldn't be added because they were too large. 

## Usage

1. My_Custom_Images contains 6 images from Google Earth that I took myself. They are implemented in the project in the Test.ipynb. 

2. Make Labels is responsible for creating all the .npy arrays of the original images and their labels. Thus, this doesn't need to be touched to run the training unless you want to add more data. 

3. Test.ipynb is where all testing of the neural networks are done. It uses the .npy files. It is also where LIME is implemeted on my 6 custom images.

4. Training.ipynb is where all training occurs for the neural networks. It uses the .npy files 

5. All .npy arrays are labeled according to what they are. The labels are 1D arrays of labels of training and test. The training and test data are the RGB images of the terrain, thus they are 4D arrays. 

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.


<!-- Authors -->
## Authors

Michelle Lorini

Project Link: [https://github.com/your_username/repo_name](https://github.com/Michelle584/Final-Project-Pattern-Rece)


<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

You can acknowledge any individual, group, institution or service.
* [Catia Silva](https://faculty.eng.ufl.edu/catia-silva/)

## Thank you

<!-- If this is useful: [![Buy me a coffee](https://www.buymeacoffee.com/assets/img/guidelines/download-assets-sm-1.svg)](https://www.buymeacoffee.com/catiaspsilva) -->
