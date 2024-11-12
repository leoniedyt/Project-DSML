Overview
You have been given the task of improving the user experience in the university's library platform for renting books. In order to do so, your main task is to build a recommendation system that recommends books to the students and members of the library (users of the platform). An appropriate recommendation system improves the users' engagement with the platform and helps them find the books of their interest based on their personal interests.

THE IDEA
The main idea is to build a recommendation system that can predict future books that a user might like, based on the user's history of book rentals. The recommendation system, as you know, assigns a score to each item (book) in the dataset. For presenting the recommendation, we can only show the top-k scored items by the recommender system. This can be shown in the interface of the platform e.g., under a section called You might also like …, similar to the recommendations you see in online shops like Amazon.

🗄 DATA
You can find the training interactions data, the items (books) metadata, and a sample submission in the Data tab.

🚀 SUBMISSION
As you build your recommender system and train it on the training interactions data, you can generate recommendations for each user ID in the dataset. For this competition, we evaluate the average Precision for the top-10 recommendations, i.e., Precision@10. Therefore, you only need to provide the top 10 recommendations of your model for each user. Make sure that your submission file has the same format as the sample_submission.csv file in the Data tab.

As soon as you submit you can see the average value of the metric Precision@10 among all the users and your ranking on the leaderboard. Note that you can only make 10 submissions per day. To know more about the competition rules, check out the rules tab.

🚚 DELIVERABLES
(One). A project GitHub page. The readme.md is your report. There, report will report in addition to other things the following table. Do hyper-parameter optimization to find the best solution. Your code should justify your results.

user-user CF	item-item CF	Any other technique
Precision@10			
Recall@10			
Report your Exploratory Data Analysis (EDA) on the interactions data and the items metadata.
Which is the best model?
Show examples of recommendations for some users. Do they align with the users' history of book rentals? Report some examples of “good” predictions, and some "bad" predictions. Do they make sense?
Use data augmentation. There exist several APIs (eg Google Books) that bring extra data using the ISBN of a book. Additionally, you may use the metadata available for the items (books).
Have a position on the leaderboard of this competition.

These results (your project report) should be shown in markdown in the readme.md of your GitHub page. Remember to include the link to your video!

(Two). User interface/application: Use Streamlit to make an interface for a recommendation application. Use book covers if you can! You are free to do what you like in this part!

(Three). Video: Create a YouTube video of your solution and add the link in your git readme file. Imagine you are giving a presentation or a tutorial. The video should explain:

The problem, your algorithm, how you make recommendations. (Note: we don't want or need to see your code in the video..! ;).
A demo of your solution (the UI you implemented).
Upload the video on Youtube (set it as unlisted if you don't wish it to be publicly visible) and put the link to the video in the readme of the Github repository of your team.

Tips:
Things you should consider trying are:

Data analysis
Using items metadata, e.g., title, author, subjects, etc.
Using text embeddings (Bert, openAI, etc) to represent items' metadata. You can use these embeddings to initialize the embedding representation of items in your recommender system. You can represent an item and a user as an embedding, and then use cosine similarity.

👩‍💻 LOGISTICS AND DEADLINE
First of all, create an account in Kaggle (if you don't have one already). As you enter the competition page, under the Team tab you can merge your user account with your teammates to create a team. For selecting your team name, please use this template: UNIL_<your team name>.

Your team name will be shown on the leaderboard and you can compare your score with other teams as you submit your solution. Make sure to mention your team name in your notebook.

Evaluation
The evaluation metric for this competition is the mean average precision@10 (MAP@10) score.

Submission File
Solutions should be submitted as a CSV file containing two columns: user_id and recommendation. The file should contain a header.

Each row of the CSV file contains the user id and the item ids of the top 10 recommendations by the model. each item id is separated by a space character. For an example of a solution with the correct format, take a look at the sample_submission.csv file in the data tab.
