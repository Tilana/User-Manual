###Getting Started

After uploading a collection of documents to Uwazi,  a metadata scheme with the relevant document properties such as the topic, related organizations and institutions, information about persons, and results or conclusions of discussions. Take a look at the [Uwazi user guide](https://github.com/huridocs/uwazi/wiki) for more information. 

The next step is to show the algorithm what is important for you:

​	(1) Search for a category by keywords and open a corresponding document

​	(2) Mark a sentence that is relevant to categorize a document.
​	     *had carnal knowledge of XX without her consent* indicates the topic *rape*.

​	(3) Click *Add as evidence*

<img src="imgs/addEvidence.png" width="550">

​	(4) Choose the category and the specific value the sentence is an evidence of.
​	Your predefined list of categories will pop up.

<img src="imgs/selectCategory.png" width="550">





Congratulations, you added your first sentence to the training data.



Go to the machine learning panel  <img src="imgs/ml_panel.png" width="50">

The machine learning panel shows you for each category the provided sentences.
On the right side panel you can filter per category.

Select a category and click the green *Toggle Predict* button. Be aware, that you need at least one sample sentence as the underlying algorithm is looking for similar phrases within other documents of the collection. So one by one, documents are processed and if semantically similar content is found, suggestions, sorted by probability pop up.

Be patient! The processing time per documents is (currently) at about 3s. Especially for topics that are rare within the collection, it might take some time to find related content.

​			<img src="imgs/suggestions.png" width="650">



The probability indicates how similar the suggestions are to the provided sample sentences for this category. The higher, the better.

The underlying approach is the Universal Sentence Encoder. [Here](https://www.tensorflow.org/hub/modules/google/universal-sentence-encoder/1) you can find out more on how it works.



Some suggestions might not fit perfectly the category you are looking. However, you can teach a classifier what is important for a category by accepting (green button) correct suggestions and rejecting (red button) wrong suggestions. You will see, that the suggestion turn into positive and negative sample sentence. 

<img src="imgs/samples.png" width="650">



To update the algorithm press the *Retrain* button next to the corresponding category. With *Toggle Predict'* new suggestions are obtained within the collection of documents.

Please be aware that to train a good classifier, you need positive and negative sample sentences. Best is to have at least five of both categories when pressing *Retrain* for the first time. And don't worry if the first results are not exactly what you are looking for. The sentence classifier is still learning. 

Click predict again to get sentence suggestions from other documents

Repeat the process of accepting and rejecting evidences to further refine the classifier and obtain better samples.

Accepting, also, automatically adds the specific category to the document the suggestion belongs to. 



###Want more details?

Find out about the Universal Sentence Encoder and the Convolutional Neural Network.

[What are Convolutional Neural Network and how to use them for Sentence Classification?](...)

Daniel Cer, Yinfei Yang, Sheng-yi Kong, Nan Hua, Nicole Limtiaco, Rhomni St. John, Noah Constant, Mario Guajardo-Céspedes, Steve Yuan, Chris Tar, Yun-Hsuan Sung, Brian Strope, Ray Kurzweil.
[Universal Sentence Encoder](https://arxiv.org/abs/1803.11175). arXiv:1803.11175, 2018.

Yoon Kim. [Convolutional Neural Networks for Sentence Classification](https://arxiv.org/abs/1408.5882). arXiv:1408.5882, 2014.





