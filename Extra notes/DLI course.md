Computers were made to complete human tasks, it seemed possible, but was harder than expected.

##### Neural networks
- inspired by human biology
- created in the 1950s
- outclassed by Von Neumann Architecture

##### Expert Systems
- Highly complex
- Programmed by hundreds of engineers
- don't work comprehensively

How Children learn
- Expose them to lots of data
- Give them the "correct answer"
- They will pick up the important - patterns on their own

#### The deep learning revolution
- we have lots of data now
	- 90% of the worlds data was generated in the last 18 months
- We have lots of computing power
- We can use the matrix math acceleration of the gpu to do deep learning good


Traditional programming: Define rules, program rules, feed it examples, and program uses rules to compute

Machine learning: Show model the examines with the answer of how to classify, Model takes guesses, we tell it if its right or not, model learns to categorize...

If rules are clear and straightforward, often better to just program it. If rules are nuanced, complex, difficult to discern, use deep learning.

#### Deep learning compared to other AI
- Depth and complexity of networks
- up to billions of parameters 
- ...

Computer vision is main example for today.
	Robotics, object detection, self driving cars, real time translation, voice recognition, virtual assistants, 
Recommender systems:
	content curation, advertising, shopping recommendations. 

The gradient is the direction that the loss decreases the most
Lambda: learning rate... how far to travel
Epoch a model update with the full dataset (repetition)
batch: a sample of the full dataset
Step: the update to the weight parameters

##### Optimizers (of the step size)
- Adam
- adagrad
- rmsprop
- sgd
- many more

We add activation functions to every node
##### Activation functions
![[20230924_151202.jpg|500]]

#### Overfitting
- Why not have a super large neural network?
![[Pasted image 20230924151456.png]]
- Can't apply things to new data...
- Applying more datapoints is good so splitting data
- Validation data to see if it truly can generalize
- 