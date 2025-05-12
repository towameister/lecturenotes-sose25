## Lecture 5: User Feedback Analysis
Understanding user needs is difficult
- What features do they need? What problems do they face? How do they use our features?
Challenges:
- Lanuage diversity
- Device diversity
- Platform diversity
- Channel diversity
- Amount of feedback
- Users are not trained to give good quality feedback

Types:
Explicit - e.g. reviews, social media
Implicit - e.g. Interaction data

Combining Explicit-Implicit feedback
graphic todo

App-stores
- **Some** users give feedback (numerical rating + description)
- Stakeholders use app descriptions to describe features, often incomplete


Topics in user feedback
requirements: Improvement/content requests, feature requests, bug reports, shortcomings
Community: howtos, questions, recommendations, reference to other apps, reference to other feedback
Rating: Praise/dispraise, promise (do this for more rating)
User experience: Helpfulness, feature information
	- interesting for defining test cases and validating requirements

Major challenges
amount of feedback
feedback channels
languages
reducing noise



### Mining requirements-related feedback

Feedback category examples:
Noise
Problem Report
Feature Request/Inquiry

High-quality data is important
Needed for good classification results
Time vs. budget vs. expert availability
Traditional ML vs Deep learning
- Deep learning does feature engineering on its own
- Neural network

ML Pipeline:
- Data collection
- Feature engineering
- Model Selection and Training
- Evaluation
- Model for Predictions

Some Classification metrics
Precision: of predicted items in a category, how man are actually in that category?
Recall: of possible items in a category, how many were assigned the correct label in the final set?
F1-score: combines precision and recall with harmonic mean
	- Only F1 is not enough

User feedback classification helps RE:
- Filter
- Allocate and assign
- Compare
- Track over time


Identifying and matching app features

Content analysis of categorized user feedback to extract features users talk about

Match talked about features to internally documented features (requirements documentation, issue trackers..)

Yields advanced analytics (frequency of feature mention, sentiment)



Summary: 
Explicit user feedback contains valuable info for RE like problem reports and feature requests
Identify feedback categories using ML 
Content Analysis can help to draw conclusions about data
Continuously analyzing feedback to improve app can help stakeholders