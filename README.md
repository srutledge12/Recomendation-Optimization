<div id="top"></div>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
<!-- [![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url] -->



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <!-- <a href="https://github.com/github_username/repo_name">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a> -->

<h3 align="center">Optimizing Social Recommendation: Efficiency vs. Accuracy</h3>

  <p align="center">
    This is an implementation of the Discrete Social Recommendation algorithm in order to compare results to competitive existing algorithms and test accuracy claims of the original DSR authors.
    
  </p>
</div>






<!-- GETTING STARTED -->
## Getting Started

This code was written on a jupiter notebook file and ran within Google Colab. We recommend you run this on Google Colab as well to match or exceed the Google provided computer resources.

### Requirements

The program is made to calculate and evaluate the the user-item recommendation scores for various items within a dataset.

You must provide the algorithm a dataset in the format of 2, mx3 sized matrices representing the User and Trust values, formatted as followed.

User Matrix:
User-id, item-id, rating

Trust Matrix:
user-id (trustor), user-id (trustee), trust-value


### Execution

The first step is to link your google drive if you are running on colab. If you are running locally skip to next step.

After linking to drive or if you are running locally, update the respective filepaths to your user and trust datasets.

Next, chop dataset to designated number of entires based on computing power in the 4th block labeled chop. The default is set to 200 entries if you do not wish to change.

Run all, after running it will perform the creation of these approximated social rankings and print/graph loss between original and a competitive method.

## Acknowledgements

Reused Code:
The function matrix_factorization() is reused code from the link below.  It was slightly modified to fit our decomposition values including steps and coefficients.
https://towardsdatascience.com/recommendation-system-matrix-factorization-d61978660b4b

The function binary() using struct to covert a 32 bit float to a binary string.
https://stackoverflow.com/questions/16444726/binary-representation-of-float-in-python-bits-not-hex

Modified Code
Function hamming_distance and dsr_hamming have been modified in order to fit our user-item dot product approximation.

The adjusted result is to product an estimate by doubling the hamming distance and subtracting the string length.

Original Code found here https://stackoverflow.com/questions/54172831/hamming-distance-between-two-strings-in-python

Original Code
Our code was not file based but written in blocks on a google colab jupiter notebook.  The rest of the blocks other than the 3 described above were the students own code.


<!-- ROADMAP -->
## Datasets

We used a dataset called FilmTrust.

This includes the rankings of 35497, including the users who ranked these and the scores. 
The dataset was obtained from this link: https://guoguibing.github.io/librec/datasets.html

The format of the dataset is as follows:
User Matrix:
User-id, item-id, rating

Trust Matrix:
user-id (trustor), user-id (trustee), trust-value

Within our code we chopped this to 200 and 400 entires for testing purposes with our given computing power.






