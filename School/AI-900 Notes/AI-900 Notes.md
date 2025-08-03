Generative AI- branch of AI that enables software applications to generate new content, often natural language dialogs, but can also be images, videos, code, and other things

- ability to generate content depends on the language model
    - LLMs are trained on large volumes of data, which are usually documents from the web or other public sources of information
    - Gen AI models encapsulate semantic relationships and that's how they generate sequences of text
    - there are LLMs and SLMs(small) which differ based on volume they’ve been trained on. LLMs are more powerful but are costly, whereas SLMs are more scenario based and typically cost less
        - Use cases include:
            - implementing chatbots and AI agents to assist human users
            - creating new documents or other content
            - automated translations of text between languages
            - summarizing or explaining complex documents

Computer Vision

- accomplished by using large amounts of images to train a model
    - Image Classification- form of CV where a model is trained with images that are labeled as the main subject of the image, so it can analyze unlabeled images and predict the most accurate label
    - Object detection- form of CV where the model is trained specifically to identify the location of specific objects in an image
    - Semantic segmentation- advanced form where the model identifies the individual pixels in the image that belong to a specific object
    - You can combine language models and CV to create a multi-modal model that combines generative AI and CV capabilities
        - Use cases include:
            - auto-captioning or tag-generation for images
            - visual search
            - security video monitoring
            - facial recognition auth
            - robotics and self-rising cars

  

Speech

- speech recognition is the ability for AI to hear and interpret speech
- speech synthesis - AI ability to vocalize words as spoken language

  

What artificial intelligence technique serves as the foundation for modern image classification solutions?

- Deep learning

  

What AI technique should be used to extract the name of a store from a photograph displaying the storefront?

- optical character recognition (OCR)

  

Extracting data and insights:

- Basis for most document analysis solutions is a computer vision technology called optical character recognition (OCR)
    - OCR model can identify the location of text in an image, advanced models can interpret individual values in the document and extract specific fields
    - Most data extraction models have historically focused on extracting fields from text-based forms, more advanced models can extract information from audio recordings, images, and videos
        - Common uses of AI to extract data and insights include:
            - automated processing of forms and other documents in a business process - for example processing an expensive claim
            - large-scale digitization of data from paper forms; scanning and archiving census records\
            - indexing documents for search
            - identifying key points and follow-up actions from meeting transcripts and recordings

  

Machine learning - to use data from past observations to predict unknown outcomes or values

- Fundamentally a ML model is a software application that encapsulates a function to calculate an output value based on one or more input values
    - process of training a function is known as training
    - after training, you can use it to predict new values in a process called inferencing
- Examples:
    - The proprietor of an ice cream store might use an app that combines  
        historical sales and weather records to predict how many ice creams  
        they're likely to sell on a given day, based on the weather forecast.  
        
    - A doctor might use clinical data from past patients to run automated tests that predict whether a new patient is at risk from diabetes based on factors like weight, blood glucose level, and other measurements.
    - A researcher in the Antarctic might use past observations to automate the identification of different penguin species (such as _Adelie_, _Gentoo_, or _Chinstrap_) based on measurements of a bird's flippers, bill, and other physical attributes.
- Types of Machine Learning:
    - Supervised - where training data includes both feature values and known label values, typically used to train models by determining a relationship between features and labels in past observations, so that unknown labels can be predicted for features in future cases
        - Split the training data randomly to create a dataset with which to train the model while holding back a subset of data that you’ll use to validate the trained model
        - Use an algorithm to fit the training data to a model. In the case of a regression model use a regression algorithm such as linear regression
        - Use the validation data you held back to test the model by predicting labels for the features
        - Compare the actual labels in the validation dataset to the labels that the model predicted. Then aggregate the differences between the predicted and actual label values to calculate a metric that indicates how accurately the model predicted for the validation data
        - Regression: form of supervised ML in which the label predicted by the model is a numerical value
            - Examples:
                - number of ice creams sold on a given day, based on temperature, rainfall, and windspeed
                - selling price of a property based on its size in square feet, number of bedrooms, and socioeconomic metrics for its location
                - fuel efficiency of a car based on engine size, weight, width, height, and length
            - Linear Regression: works by deriving a function that produces a straight line through the intersections of the x and y values while minimizing the average distance between the line and the plotted points
                - Regression Evaluation Metrics
                    - Mean Absolute Error: takes all discrepancies between predicted and actual labels into account equally. However, it may be more desireable to have a model that is consistently wrong by a small amount than one that makes fewer, but larger errors
                    - Root Mean Squared Error: takes the magnitude of errors into account, but because it squares the error values. Which makes the resulting metric no longer represent the quantity measured by the label
                    - Coefficient of determination: used to measure the proportion of variance in the validation results that can be explained by the model as opposed to some anomalous aspect of the validation data
            - Iterative training examples:
                - feature selection and preparation; choosing which features to include in the model, and calculations applied to them to help ensure a better fit
                - algorithm selection
                - algorithm parameters; numeric settings to control algorithm behavior, _hyperparamters_ to differentiate them from the x and y parameters
        - Classification: form of supervised ML in which the label represents a categorization, or class. There are 2 common classification scenarios:
            - Binary classification: label determines whether the observed item is an instance of a specific class
            - used to train a model that predicts one of two possible labels for a single class. Essentially predicting true/false
            - uses an algorithm to fit the training data to a function that calculates the probability of the class label being true and is measure between 0.0 and 1.0
                - logistic regression is one algorithm that can be used with binary classification
                - first step in calculating evaluation metrics for a binary classification model is to create a matrix of the number of correct and incorrect predictions for each possible class label
                    - Accuracy: simplest metric that can be used to calculate from the confusion matrix
                    - Recall: measures the proportion of positive cases that the model identified correctly
                    - Precision: metric similar to recall, but measures the proportion of predicted positive cases where the true label is actually positive
                    - F1-Score: metric that combined recall and precision
                        - Formula: _**(2 x Precision x Recall) ÷ (Precision + Recall)**_
                    - Area Under the Curve: Another name for recall is true positive rate(TPR) and theres an equivalent metric called the false positive rate (FPR) that is calculated as **FP÷(FP+TN).** If changing the threshold above which the model predicts true it would affect the number of positive and negative predictions, which changes the TPR and FPR metrics.
                        - Often used to evaluate a model by plotting a received operator characteristic curve that compares the TPR and FPR for every possible threshold value between 0.0 and 1.0
                - Examples:
                    - Whether a patient is at risk of diabetes based on clinical metrics like weight, age, blood glucose level, and so on
                    - Whether a bank customer will default on a loan based on income, credit history, age, and other related factors
                    - whether a mailing list customer will respond positively to a marketing offer based on demographic attributes and past purchases
                - In those examples the model predicts a binary true/false or positive/negative prediction for a single possible class
                - Multiclass classification: extends binary classification to predict a label that represents one of multiple possible classes, follows the same iterative train, validate, and evaluate process as regression and binary classification since its a supervised ML technique
                    - To train a multiclass classification model you need to use an algorithm to fit the training data to a function that calculates a probability value for each possible class.
                        - One-vs-Rest algorithms (OVR): train a binary classification for each class, each calculating the probability that the observation is an example of the target class. Each function calculates the probability of the observation being a specific class to any other class. Produces a sigmoid function that calculates the probability value between 0.0 and 1.0
                        - Multinomial algorithms: creates a single function that returns a multi-valued output. Output is a vector that contains the probability distribution for all possible classes - with a probability score for each class which when totaled add up to 1.0
                    - You can evaluate a multiclass classifier by calculating binary classification metrics for each individual class
                    - Confusion matrix shows the number of predictions for each combination of predicted and actual class labels
                    - Examples:
                        - the species of a penguin based on its physical measurements
                        - genre of a movie based on its cast, director, and budget
    - Unsupervised Machine Learning: training models using data that consists only of feature values without any known labels. algorithms determine relationships between the features of the observations in the training data
        - Clustering: most common form of unsupervised machine learning, the algorithm identifies similarities between observations based on their features, and groups them into discrete clusters
            - Training a clustering model: Multiple algorithms that can be used but the most common is K-Means Clustering which consists of;
                - The feature (_**x**_) values are vectorized to define _n_dimensional coordinates (where _n_ is the number of features). In the flower example, we have two features: number of leaves (_**x1**_) and number of petals (_**x2**_). So, the feature vector has two coordinates that we can use to conceptually plot the data points in two-dimensional space (_**[x1,x2]**_)
                - You decide how many clusters you want to use to group the flowers - call this value _k_. For example, to create three clusters, you would use a _k_ value of 3. Then _k_ points are plotted at random coordinates. These points become the center points for each cluster, so they're called _centroids_.
                - Each data point (in this case a flower) is assigned to its nearest centroid.
                - Each centroid is moved to the center of the data points assigned to it based on the mean distance between the points.
                - After the centroid is moved, the data points may now be closer to a  
                    different centroid, so the data points are reassigned to clusters based  
                    on the new closest centroid.  
                    
                - The centroid movement and cluster reallocation steps are repeated  
                    until the clusters become stable or a predetermined maximum number of  
                    iterations is reached.  
                    
            - Evaluating a clustering model: based on how well the resulting clusters are separated from one another
                - Metrics to use:
                    - Average distance to cluster center: How close on average each point in the cluster is to the centroid of the cluster
                    - Average distance to other center: How close on average each point is to the centroid of all other clusters
                    - Maximum distance to cluster center: The furthest distance between a point in a cluster and its centroid
                    - Silhouette: A value between -1 and 1 that summarizes the ratio of distance between points in the same cluster and points in different clusters ( closer to 1, the better the cluster separation)
            - Examples:
                
                - group similar flowers based on their size, number of leaves, and number of petals
                
                ![[image.png]]
                
                - identify groups of similar customers based on demographic attributes and purchasing behavior

  

Deep Learning: advanced form of machine learning that tries to emulate the way the human brain learns. Works by creation of artificial neural networks that simulate the electrochemical activity in biological neurons by using mathematical functions

- Made up of multiple layers of neurons, basically a deeply nested function
    - reason the technique is called deep learning and the models produced are referred to as deep neural networks
        - You can use DNNs for many ML problems such as regression, classification, and more specialized models for NLP and computer vision
- Deep Learning for Classification:
    
    - A classification model accomplishes this by predicting a label that  
        consists of the probability for each class. In other words, y is a  
        vector of three probability values; one for each of the possible  
        classes: _**[P(y=0|x), P(y=1|x), P(y=2|x)]**_.
    
    The process for inferencing a predicted penguin class using this network is:
    
    - The feature vector for a penguin observation is fed into the input  
        layer of the neural network, which consists of a neuron for each _**x**_ value. In this example, the following _**x**_ vector is used as the input: _**[37.3, 16.8, 19.2, 30.0]**_
    - The functions for the first layer of neurons each calculate a weighted sum by combining the _**x**_ value and _**w**_ weight, and pass it to an activation function that determines if it meets the threshold to be passed on to the next layer.
    - Each neuron in a layer is connected to all of the neurons in the next layer (an architecture sometimes called a _fully connected network_) so the results of each layer are fed forward through the network until they reach the output layer.
    - The output layer produces a vector of values; in this case, using a _softmax_ or similar function to calculate the probability distribution for the  
        three possible classes of penguin. In this example, the output vector  
        is: _**[0.2, 0.7, 0.1]**_
    - The elements of the vector represent the probabilities for classes  
        0, 1, and 2. The second value is the highest, so the model predicts that the species of the penguin is **1** (Gentoo).
- How does a Neural Network learn:
    - training and validation datasets are defined, and training features are fed into the input layer
    - neurons in each layer of the network apply their weights and feed the data through the network
    - output layer produces a vector containing the calculated values for y
    - Loss function is used to compare the predicted Y values to the known y values and aggregate the difference(Loss)
    - Since the entire network is one large nested function, an optimization function can use differential calculus to evaluate the influence of each weight in the network on the loss, and determine how they could be adjusted to reduce the amount of overall loss. Optimization technique can vary, but usually involves a gradient descent approach in which each weight is increased or decreased to minimize the loss
    - changes to the weights are back propagated to the layers in the network, replacing the previously used values
    - process is repeated over multiple iterations (epochs) until the loss is minimized and the model predicts the accepted accurately

  

You want to create a model to predict the cost of heating an office building based on its size in square feet and the number of employees working there. What kind of machine learning problem is this?

- Regression

  

You need to evaluate a classification model. Which metric can you use?

- precision

  

In deep learning, what is the purpose of a loss function?

- to evaluate the aggregate difference between predicted and actual label values

  

Which is the best description of generative AI?

- generative ai uses a language model to create original content in response to a prompt

  

A wildlife conservation app uses AI to locate one or more animals in photos. Which computer vision capability is being used?

- object detection

  

An AI application reads email aloud to a user. Which AI speech capability is being used?

- speech synthesis

  

  

  

Which computer vision solution provides the ability to identify a person’s age based on a photograph?

- facial detection

  

Which process allows you to use optical character recognition(OCR)?

- digitizing medical records

  

Which process allows you to use object detection?

- tracking livestock in a field

  

You have a set of images, each image shows multiple vehicles. What allows you to identify different vehicle types in the same traffic monitoring image?

- object detection

  

Which analytical task of the Azure AI Vision service returns bounding box coordinates?

- object detection

  

Which additional piece of information is included with each phrase returned by an image description task of the Azure AI Vision?

- confidence score

  

When using the Azure AI Face service, what should you use to perform one-to-one or one-to-many face matching?

- Face identification - because it matches one face to many in an image to a set of faces in a secure repository
- face verification - has the capability of 1:1 matching to verify it's the same faces as the individual

  

Which service can you use to train an image classification model?

- Azure AI Custom Vision

  

Which natural language processing technique assigns values to words such as plant and flower, so they are considered closer to each other than a word such as airplane?

- vectorization

  

What is the first step in the statistical analysis of terms in a text in the context of natural language processing?

- removing stop words

  

what is the confidence score returned by Azure AI Language detection service of natural language processing for an unknown language name?

- NaN -not a number, which designates an unknown confidence score.

  

Which part of speech synthesis in natural language processing involves breaking text into individual words such that each word can be assigned to phonetic sounds?

- transcribing

  

which two features of azure AI services allow you to identify issues from support question data, as well as identify any people and products that are mentioned?

- key phrase extraction - used to extract key phrases to identify the main concepts in a text, which enables a company to identify main talking points from the support question data and allows them to identify common issues
- named entity recognition - can identify and categorize entities in unstructured text, such as people, places, orgs, and quantities

  

which azure AI service for language feature allows you to analyze written articles to extract information and concepts, such as people and locations, for classification purposes?

- named entity recognition

  

for which two scenarios is the universal language model used by the speech-to-text API optimized?

- dictation
- conversational

  

which azure resource provides direct access to both Azure AI Translator and Azure AI Speech services through a single endpoint and authentication key?

- Azure AI Services

  

which three features are elements of the azure ai language service?

- entity linking
- personally identifiable information detection (PII)
- Sentiment analysis

  

_____ use plugins to provide end user with the ability to get help with common tasks from a generative AI model

- Copilots

  

at which layer can you apply content filters to suppress prompt and response for a responsible generative AI solution?

- **safety system** - includes platform-level configurations and capabilities that help mitigate harm. Azure OpenAI service includes support for content filters that apply criteria to suppress prompts and responses based on the classification of content into 4 severity levels (safe, low, medium, and high) for 4 categories of potential harm (hate, sexual, violence, and self-harm).

  

________ can return responses, such as natural language, images, or code, based on natural language input

- Generative AI

  

______ can be used to identify constraints and styles for the responses of a Generative AI model.

- system messages - used to set the context for the model by describing expectations. Based on system messages, the model knows how to respond to prompts

  

as per the NISTA AI Risk Management Framework, what is the first stage to consider when developing a responsible generative AI solution?

- identify potential harms

  

what two capabilities are examples of a GPT model?

- create natural language
- understand natural language

  

which three capabilities are examples of image generation features for a generative AI model?

- creating a variation of an image
- editing an image
- new image creation

  

which generative AI model is sued to generate images based on natural language prompts?

- DALL-E, can generate images from natural language. GPT-4 and GPT-3 can understand and generate natural language and code, but not images.

  

______ can search, classify, and compare sources of text for similarity

- Embeddings - an Azure AI OpenAI model that converts text into numerical vectors for analysis.

  

Which type of service provides a platform for conversational artificial intelligence?

- Azure AI Bot Service

  

Which AI service can be integrated into chat applications and generate content in the form of text?

- Azure OpenAI

  

Which type of artificial intelligence workload has the primary purpose of making large amounts of data searchable?

- knowledge mining

  

which 2 artificial intelligence workload scenarios are examples of natural language processing?

- performing sentiment analysis on social media data
- translating text between different languages from product reviews

  

which two artificial intelligence workload features are part of the Azure AI Vision service?

- Optical character recognition
- spatial analysis

  

which principles of AI have the objective of ensuring that AI solutions benefit all parts of society, regardless of gender or ethnicity?

- inclusiveness

  

which principle of responsible AI plays the primary role when implementing an AI solution that meets qualifications for business loan approvals?

- fairness

  

a bank is developing a new AI system to support the process of accepting or rejecting mortgage applications. Which 2 issues should be considered as part of the responsible AI principle of fairness to avoid biased decision-making?

- gender
- ethnicity

  

which principle of responsible AI ensures that an AI system meets any legal and ethical standards it must abide by?

- accountability

  

a company is currently developing driverless agriculture vehicles to help harvest crops. the vehicles will be deployed alongside people working in the crop fields, and as such, the company will need t carry out robust testing. Which principle of AI is most important in this case?

- reliability and safety

  

you need to identify numerical values that represent the probability of humans developing diabetes based on age and body fat percentages. Which type of machine learning model should you use?

- logistic regression

  

which type of machine learning algorithm groups observations are based on the similarities of features?

- clustering

  

which type of machine learning algorithm finds the optimal way to split a dataset into groups without relying on training and validating label predictions?

- Clustering

  

predicting rainfall for a specific geographical location is an example of which type of machine learning?

- regression

  

a healthcare organization has a dataset consisting of bone fracture scans that are categorized by using predefined fracture types. The organization wants to use machine learning to detect the different types of bone fractures for new scans before the scans are sent to a medical practitioner. Which type of machine learning is this?

- classification

  

an electricity utility company wants to develop a mobile app for its customers that monitor theri energy use and to display their predicted energy use for the next 12 months. the company wants to use a machine learning model to provide a reasonably accurate prediction of future energry use by using the customers’ previous energy-use data

What type of machine learning is this?

- regression

  

Regression- a machine learning scenario that is used to predict numerical values

  

Multiclass clasification- used to predict categories of data

  

Clustering- analyzes unlabeled data to find similarities present in the data

  

Classification - used to predict categories of data

In a regression machine learning algorithm, what are the characteristics of features and labels in a training dataset?

- known feature and label values

  

a company is using machine learning to predict house prices based on appropriate house attributes. for the machine learning model which attribute is the label?

- price of the house

  

you need to use Azure Machine Learning to trains a regression model. what should you create a machine learning studio?

- a job

  

Workspace- must be created before you can access machine learning studio

Container and Azure Kubernetes Service cluster - can be created as a deployment target, after training a model is complete

  

You need Azure Machine Learning designer to deploy a predictive service from a newly trained model. What should you do first in the Machine Learning designer?

- create an inference pipeline

  

What 3 data transformation modules are in the Azure Machine Learning designer?

- Clean missing data
- normalize data
- select columns in dataset

  

What is an unsupervised machine learning algorithm module for training models in the Azure Machine Learning designer?

- K-Means Clustering

  

K-Means Clustering - unsupervised machine learning algorithm component used for training clustering models, and can use unlabeled data with this algorithm.

  

Linear Regression and Classification - supervised machine learning algorithm components, need labeled data for these algorithms

  

Natural Language Processing(NLP) - part of AI that deals with understanding written or spoken language, and responding. NLP might be used to create:

- social media feed analyzer that detects sentiment for a product marketing campaign
- document search application that summarizes documents in a catalog
- application that extracts brands and company names from text

  

Azure AI Language - cloud based service that includes features for understanding and analyzing text. It has various features such as support sentiment analysis, key-phrase identification, text summarization, and conversational language understanding

  

Tokenization- first step is when analyzing a corpus, breaks down into tokens. Basically each word is 1 token, but they can be generated for partial words or combinations of words

  

Text normalization - before generating tokens, you may choose to normalize the text by removing punctuation and changing all words to lowercase, which improves overall performance if the analysis relies on word frequency.

  

Stop word removal - stop words are words that should be excluded from the analysis

  

n-grams - multi-term phrases such as “I have” or “he walked”

unigrams- single word phrase

bi-grams - 2 word phrase

tri-grams - 3 word phrase

  

Stemming - technique where algorithms are applied to consolidate words before counting them, so that words with the same root, like “power”, “powered”, and “powerful” are interpreted as the same token

  

Frequency analysis - a count analysis to count number of occurrences of a token. most commonly used tokens can provide a clue towards the main subject of the corpus.

  

simple frequency analysis - effective way to analyze a single document

  

term frequency - inverse document frequency(TF - IDF) - common technique in which a score is calculated based on how often a word or term appears in one document compared to its more general frequency across the entire collection of documents

  

Logistic regression - used to train a ML model that classifies text based on a known set of categorizations. common application of the technique is to train a model that classifies text as positive of negative in order to perform sentiment analysis or opinion mining.

  

Common NLP tasks supported by language models

- text analysis
- sentiment analysis and opinion mining to categorize text as positive or negative
- machine translation, in which text is automatically translated from one language to another
- summarization, in which main points of a large body of a text are summarized
- bots or digital assistants in which the language model can interpret natural language and return an appropriate response

  

Key Elements of AI:

- Machine Learning - the foundation of an AI system, learn and predict like a human
- Anomaly detection - detect outliers or things out of place like a human
- Computer Vision - be able to see like a human
- Natural Language Processing - be able to process human languages and infer context
- Conversational AI - be able to hold a conversation with a human

  

Dataset - logical grouping of units of data that are cloesly related and/or share the same data structure

- there are publicly available data sets that are used in stats, data anlysis, and machine learning

  

MSINT database - images of handwritten digits used to test classification, clustering, and image processing algorthms

- commonly used when learning how to build computer vision machine learning models to translate handwriting into digital text

  

COCO dataset - contains many common images using a JSON file in coco format that identify objects or segments within an image

Features:

- object segmentation
- recognition in context
- superpixel stuff segmentation
- 329k images
- 0.5 million object instances
- 79 object categories
- 90 stuff categories
- 4 captions per image
- 249,000 people with keypoints

  

Azure AI Studio - platform that integrates Azure AI services, including Azure OpenAI, Azure Machine Learning, and Cognitive Services

- provides a centralized environment for developing, deploying, and managing AI solutions
- facilitates prompt engineering and model customization
- supports the creating of AI applications without extensive coding

  

Azure AI Foundry - suite within Azure AI Studio designed for building, training, and deploying AI models

- offers tools for model development and experimentation
- includes a model catalog for accessing pre-trained models
- enables seamless integration with other Azure services

  

Transformer Architecture - deep learning model architecture that relies on self-attention mechanisms, enabling the processing of sequential data

- Trained with large volumes of text, enabling them to represent semantic relationships between words and use those relationships to determine probable sequences of text that make sense
- Consist of two blocks:
    
    - Encoder: creates semantic representations of the training vocabulary
    - Decoder: generates new language sequences
    
    ![[image 1.png]]
    
    - sequences of text are broken into tokens and the encoder block processes these token sequences using a technique called attention to determine the relationships between tokens
    - output from the encoder is a collection of vectors in which each element of the vector represents a semantic attribute of the tokens referred to as Embeddings
    - decoder block works on a new sequence of text tokens and uses the embeddings generated by the encoder to generate and appropriate natural language output
        - Example: input sequence “==When my dog was”,== the model can use attention technique to analyze the input tokens and the semantic attributes encoded in the embeddings to predict an appropriate completion of the sentence, such as ==“a puppy”==

- Significance:
    - forms the foundation of LLMs like GPT-4
    - Allows for parallel processing of data, improving efficiency
- First step in training a transformer model is to decompose the training text into tokens; identify each unique text value
    - I (1)
    - heard (2)
    - a (3)
    - dog (4)
    - bark (5)
    - loudly (6)
    - at (7)
    - ("a" is already tokenized as 3)
    - cat (8)
- Attention: examines a sequence of text tokens and tries to quantify the strength of the relationships between them. Self-Attention involves considering how other tokens around one particular token influence that token’s meaning

  

Responsible AI Considerations

- Key Principles
    - Fairness - ensuring AI systems don't exhibit bias
    - Reliability & Safety - AI systems should function reliably and safely under all conditions
    - Privacy & Security - protecting user data and ensuring secure operations
    - Inclusiveness - AI should be accessible and beneficial to all users
    - Transparency - Operations of AI systems should be understandable
    - Accountability - Clear responsibility for AI system outcomes

  

  

Azure AI Language - can perform advanced natural language processing over unstructured text.

  

You want to use Azure AI Language to determine the key talking points in a text docuement. Which feature of the service should you use?

- Key phrase extraction

  

You use Azure AI Language to perform sentiment analysis on a sentence. The confidence scores .04 positive, .36 neutral, and .60 negative are returned. What do these confidence scores indicate about the sentence sentiment?

- the document is negative

  

When might you see **NaN** returned for a score in language detection?

- when the language is ambiguous

  

Azure AI services:

- prebuilt and ready to use
- accessed through APIs
- Available and secure on Azure
- cloud based
- 2 types of AI service resources:
    - Multi-service resource: provides access to multiple Azure AI services with a single key and endpoint
    - Single-service resource: provides access to a single Azure AI service such as Speech, Vision, Language, etc. Has a unique key and endpoint for each service

  

An application requires three separate AI services. To see the cost for each separately, what type of resource(s) should be created?

- A single-service resource for each AI service

  

What is an Azure AI services resource?

- A bundle of several AI services in one resource

  

A law firm wants to process large volumes of legal documents to automaticall extract key information such as, names of involved parties, case numbers, and relevant legal terms. Which capability of Azure AI Language should they use?

- Entity recognition: extracts meaningful elements from text such as names, numbers, and specialized terms

  

A retail company wants to use computer vision to automate product identification at checkout. The system should recognize different products placed on the counter and classify them accordingly. Which type of computer vision solution is best suited for this task?

- Image classification: assigns category labels to entire images, making it useful for recognizing products

  

Which scenario would most likely require a deep learning model instead of traditional machine learning techniques?

- Identifying objects in images with high accuracy: typically requires deep learning, such as convolutional neural networks

  

An online education platform wants to use gen AI to create personalzied study materials for students based on their performance history. The AI should generate relevant practice questions and explanations tailored to each student’s needs. Which feature of Gen AI enables this capability?

- Text generation: allows AI models to create new educational content based on contextual input

  

Which type of machine learning model is best suited for predicting continuous numerical values, such as forecasting sales revenue?

- Regression: predicts continuous numerical values, making them suitable for forecasting sales revenue

  

Ensuring AI systems are understandable and that their decisions can be interpreted by users aligns with which responsible AI principle?

- Transparency: involves making systems understandable and their decisions interpretable by users

  

A multinational customer service team needs to deploy an AI-driven voice interpreter that enables agents to communicate with customers in different languages in real-time. Which NLP feature is required?

- Interactive conversion: enables real-time multilingual conversation by integrating speech recognition and text transformation

  

Which machine learning technique is best suited for discovering natural groupings in a dataset without error labels?

- Clustering: groups data points into clusters based on similarity

  

Which of the following is a primary benefit of using Azure Automated Machine Learning (AutoML)

- It automatically selects the best model and hyper-parameters for a given dataset

  

A chatbot is being developed to assist users with booking travel arrangements. The chatbot should be able to understand user requests and generate relevant responses in a conversational format. Which NLP feature is crucial for this capability?

- Language modeling: enables the chatbot to understand and generate coherent responses

  

Which Azure service is best suited for deploying machine learning models as scalable web services?

- Azure Kubernetes Service (AKS): enables scalable and containerized deployments of machine learning models

  

An AI system that provides loan approvals shows a pattern of approving loans for one demographic group more frequently than others with similar credit profiles. Which responsible AI principle is most directly violated in this scenario?

- Fairness: treat all individuals equally, and a bias in loan approvals indicates a violation

  

Which Azure service is designed to generate human-like text based on input prompt in generative AI workloads?

- Azure OpenAI service: provides access to advanced language models capable of generating human-like text based on input prompts

  

What is the primary function of a dataset in machine learning?

- to evaluate the final performance of a trained model: how well the trained model performs on unseen data before deployment

  

A mobile banking application wants to implement a feature where users can scan and deposit checks using their phone cameras. The app must recognize check details, including the amount and recipients name. Which computer vision solution should be used?

- Optical character recognition (OCR): extracts and processes text from images, making it ideal for scanning checks

  

A healthcare provider wants to analyze patient feedback surveys to determine common concerns and frequently mentioned topics. Which NLP feature should they use?

- Key phrase extraction: identifies the most relevant words or phrases in patient feedback, allowing the provider to recognize common concerns

  

A business intelligence team wants to analyze customer support tickets to determine trends related to product issues, location, and customer types. Which NLP feature would help categorize these data points?

- Entity recognition