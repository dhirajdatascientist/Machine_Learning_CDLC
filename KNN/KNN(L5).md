**KNN (K-Nearest Neighbors)**
1. **Instance-based:** KNN is an instance-based learning algorithm, meaning it memorizes instances of the training dataset to make predictions.
2. **Non-parametric:** It doesn't make any assumptions about the underlying data distribution.
3. **Lazy learner:** KNN doesn't build an explicit model during the training phase. Instead, it searches for the K-nearest training instances in real-time during the prediction phase.
4. **Distance metric:** Uses a distance metric (e.g., Euclidean distance) to find the closest instances in the training set.
5. **Sensitive to scaling:** The performance of KNN is influenced by the scale of features, so feature scaling (e.g., normalization or standardization) is often required.

**Decision Tree**
1. **Hierarchical Structure:** Decision trees split the dataset into subsets using a tree-like model of decisions. Each node in the tree represents a feature, and each branch represents a decision rule.
2. **Parametric:** Although the tree structure is flexible, the algorithm makes certain assumptions based on the data, and the structure of the tree is parameterized by these decisions.
3. **Eager Learner:** A decision tree is an eager learner, which means it constructs a model during the training phase and uses this model for predictions, as opposed to KNN, which waits until a query is made.
4. **Interpretable:** Decision trees can be visualized, making them highly interpretable and easy to understand, even by non-experts.
5. **Prone to overfitting:** Without constraints or pruning, decision trees can fit very closely to the training data, capturing noise and making them less generalizable to new data.


## Boiled Content By Dhiraj


**KNN (K-Nearest Neighbors)**
1. **Memory-based:** Like remembering faces of your classmates.
2. **Asks neighbors:** "Who do I most look like?" to decide a label.
3. **Needs all data:** Always carries the yearbook to find classmates.
4. **No model:** Doesn't summarize, just checks pictures every time.
5. **Cares about distance:** Sits closer to friends similar to him.

*Example:* Imagine you walk into a room full of people wearing either red or blue shirts. You're unsure about which color shirt you should wear. So, you ask the 5 people closest to you. If 4 out of 5 nearby people wear red shirts, you'll probably choose red too.

**Decision Tree**
1. **Question-based:** Asks "yes" or "no" questions to decide.
2. **Builds a flowchart:** Draws out questions to sort things.
3. **Uses rules:** Follows its chart for every new person or thing.
4. **Summarizes:** Once it draws its chart, doesn't need original data.
5. **Can be specific:** Might overthink and draw a very detailed chart.

*Example:* At a carnival game, you guess the age of participants to give prizes. You start by asking, "Is the person taller than 5 feet?" If yes, your next question might be, "Do they have glasses?" By following a series of such questions, you make your guess.

