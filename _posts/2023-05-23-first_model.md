## My first Fast.ai Model

This morning, I trained a model in fast.ai that does a surprisingly decent job of differentiating between 10 different animals. 

[Here’s my animal classifier notebook!](https://colab.research.google.com/drive/1f7c881ImRZC4xVS6VUMfh-2akrpRVFPq#scrollTo=QRzAlHhYSedH)

Through a series of iterative experiments, I carefully adjusted the search parameters to generate specific search strings. 
so that I could fine-tune my model with a reasonable error rate. My quest for enhanced accuracy began with the deployment of a `ResNet18` model with `vision_learner()`, paving the way for precise fine-tuning of my model. The table below showcases the evolution the trained model over ten epochs:

| epoch | train_loss | valid_loss | error_rate | time  |
|-------|------------|------------|------------|-------|
| 0     | 0.255739   | 0.212580   | 0.064865   | 00:11 |
| 1     | 0.144847   | 0.174920   | 0.064865   | 00:11 |
| 2     | 0.090092   | 0.178747   | 0.051351   | 00:09 |
| 3     | 0.058564   | 0.171632   | 0.045946   | 00:10 |
| 4     | 0.039806   | 0.157395   | 0.043243   | 00:11 |
| 5     | 0.026106   | 0.148672   | 0.043243   | 00:10 |
| 6     | 0.017356   | 0.141785   | 0.043243   | 00:09 |
| 7     | 0.012272   | 0.138629   | 0.043243   | 00:16 |
| 8     | 0.008557   | 0.137629   | 0.045946   | 00:11 |
| 9     | 0.005860   | 0.136397   | 0.043243   | 00:10 |

With each passing epoch, I observed a consistent decrease in both training and validation losses. This reduction in losses is a strong indicator of the model's ability to better understand and classify from the training data, translating into improved accuracy. Remarkably, by the ninth epoch, the training loss had dwindled to an impressive 0.005860, with a validation loss of 0.136397. Surprisingly, the error rate remained steady at 0.043243 from the fifth to the ninth epoch, underscoring the model's capacity to maintain its newfound accuracy. From my trained model, I was able to analyse the results with confusion matrices and T-SNE, which I will explain further in my assessment report. 

[Here is the link to my notebook GUI that can use the images to determine what animal it is!](https://colab.research.google.com/drive/1f7c881ImRZC4xVS6VUMfh-2akrpRVFPq#scrollTo=SBnJD5JJZclE&line=1&uniqifier=1)
The GUI shows the probability of the animal it has chosen as the predicted animal. 

![Notebook cell output](images/cell.png)

![Chloe](images/Snapseed.jpg)

I still feel a little uncomfortable to run so much code that I don’t fully understand yet (as I am still in the early stages of the fast.ai course), 
but I am taking Jeremy’s advice and went ahead with building my animal classifier model. I'm sure as I get further ahead in the course, the code will begin to make sense. What I know so far though is that fast.ai is very, very neat code!
