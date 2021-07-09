# Deep Learning Project Proposal

**Question/Need: What is the framing question of your analysis, or the purpose of the model/system you plan to build? Who benefits from exploring this question or building this model/system?**  

Framing Question:
* Problem: Although technology platform are increasingly quickly, often government forms continue to be paper forms. Paper forms increase the risk for lost information and slower processing times.
* Data Science Solution Path: Design a neural network algorithm that takes in a handwritten words and converts them to text representation.
* Initial Impact Hypothesis: Technology to read and convert handwritten text will increase the processing time of paper forms. 
* Measures of success, both technical and non-technical: Quicker processing time, high accuracy in converting written information. 

**Data Description: What dataset(s) do you plan to use, and how will you obtain the data? What is an individual sample/unit of analysis in this project? What characteristics/features do you expect to work with? If modeling, what will you predict as your target?**

The individual unit will be written word image. The dataset includes ~115,00 images. 

[Data Link](https://fki.tic.heia-fr.ch/databases/iam-handwriting-database)

**Tools: How do you intend to meet the tools requirement of the project? Are you planning in advance to need or use additional tools beyond those required?**  

Tools that will be used to process the images:
* Keras
* MongoDB - potentially for the storage of the data

**MVP Goal: What would a minimum viable product (MVP) look like for this project?**  
The MVP will be some a baseline model. 