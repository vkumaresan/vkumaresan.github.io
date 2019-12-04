Since I didn’t have much time to write any blog posts this past year, I thought that I would recap all of the various projects that I worked on, as well as highlight some key takeaways that I learned. This year was challenging and intensive, but it was exactly what I was looking for from a graduate school experience.

![Duke Chapel. Photo: [https://duke.edu/contact/](https://duke.edu/contact/)]


**Fall Semester**

### Intro to Text Analysis and Data Scraping

This course was a broad overview of text analysis and NLP techniques in the data science field, primarily through applications in R. We learned about techniques in class and practiced them in various exercises, but the class was centered around the final project. We worked on this project throughout the entire semester, incorporating techniques as we learned them in class and gathering feedback from our professor as we went along. Our team decided to analyze depression sentiment across various social media sources (Reddit, Twitter, Tumblr, and blogs/forums) to find any trends or insights that could inform focused outreach. We scraped/pulled our data from the social media sites and then tested our techniques on each dataset, which was a great learning opportunity for us to deal with messy data. We ultimately shared our insights with the rest of the class at the end of the semester, and our slides can be found here:

[https://github.com/vkumaresan/Text-Analysis-Final-Project/blob/master/Text%20Analysis%20Final_%20Expression%20of%20Depression.pdf](https://github.com/vkumaresan/Text-Analysis-Final-Project/blob/master/Text%20Analysis%20Final_%20Expression%20of%20Depression.pdf)

### Modeling and Representation of Data

This course walked through various modeling techniques, ranging from linear and logistic regression to time-series forecasting. It did not focus on machine learning techniques, since we had a separate class for that later on, but instead focused on considerations to keep in mind when modeling data. We learned theory in class and applied our theory in weekly homework assignments in R, giving us practice with analyzing datasets and interpreting the results. The final project for this class was an individual one of our choosing, so I decided to model nursing home quality indicators. I actually wrote another blog post about that work, which can be found [here](https://datainallthings.wordpress.com/2019/01/10/nursing-home-analysis-cms-data/).

### Database Management Systems

In this course, we were exposed to various database systems and gained an understanding of how they work in production environments. Starting with SQL and then moving through NoSQL and Hadoop frameworks, we learned about the advantages of disadvantages of every system, while also learning about syntax and how to use each language to access data. Our final project consisted of analyzing emergency room admissions for mental health reasons in various North Carolina hospitals, so I can’t share the data or analysis publicly here. We used a PySpark interface to access the data and perform queries upon it, although we also used MapReduce for a couple of larger scale insights that we wanted to gather.

**Spring Semester**

### Data to Decision

This class taught us the fundamentals of information theory, and interesting framework for analyzing the incremental value created by the data science products/models that we create. Using a Bayesian framework, we learned and applied different techniques that allowed us to quantify information gain, entropy, and other model characteristics in order to inform decision-making. We didn’t have a final project in this class, but part of our grade was our attendance at DataFest, a nation-wide data science hackathon.

Universities from all over the country host this event, which is sponsored and led by the American Statistical Association. Duke University happened to host the competition for the North Carolina region, so there were participants from colleges across the state who came to our campus for a weekend. Every team was given the same dataset, which this year came from the Canadian Women’s Rugby Sevens Olympic organization. I can’t share any data or methods here since it is their proprietary knowledge, but their question was related to developing a better method to understand player fatigue and adjust training regimens accordingly. The dataset included a lot of different data types, including survey responses, workout information, and even player GPS data. It would have been easy to get lost in all of this data, but my team chose to focus on what we were learning in our Data to Decision class and compare the information gained from a model w/objective game data vs. subjective data. We also utilized outside data including weather and game flow data, in addition to the features that we created for in-game acceleration. Ultimately, we presented our results twice and ended up winning ‘Best Use of Outside Data’. It was a great learning opportunity for us to be challenged and build a useful model in a limited amount of time.

### Principles of Machine Learning

This course served as an overview of machine learning methods that are currently being used in industry. We covered a lot of material in this class, including supervised learning, unsupervised learning, deep learning, and reinforcement learning. Since we only had one semester to go through all of this material, the lectures were fast-paced and informative, but we also had opportunity to learn from the readings and homework assignments. The readings were from widely-recognized books in the industry, including An Introduction to Statistical Learning (ISL), Deep Learning by Ian Goodfellow, and Reinforcement Learning: An Introduction by Sutton and Barto. Our homework assignments were comprehensive mini-projects focused on a deep dive into an area of machine learning; these assignments were in Python Jupyter Notebooks, where we worked through concepts and built Python programs that would show our understanding in domains including Logistic Regression, Clustering, and Reinforcement Learning. My notebooks can be found on my GitHub repo for the class:

[https://github.com/vkumaresan/ECE590](https://github.com/vkumaresan/ECE590)

We had two projects in this class: the first was focused on image classification of solar arrays on house rooftops using aerial imagery data. Our team tried various approaches including logistic regression, K-Means clustering, and neural networks. Ultimately, the neural network approach worked best on the test dataset, so we tuned our hyperparameters until we achived a performance (AUC) of 0.99161. This project taught us a lot about neural network construction and the various ways of improving model performance.

Our final project was a team project where we could decide on any topic of our choosing. We ultimately landed on analyzing how access to various transportation methods affects urban housing price, specifically in New York City. We obtained publicly available housing data, as well as data about Uber trips, taxi trips, subway stop locations and bike share locations. After cleaning and processing the data, we tried various regression techniques to see which one ultimately achieved the highest performance, including linear regression, K-Means clustering, CART, Random Forest regression, and a neural network. Ultimately, the Random Forest model performed the best, although we probably could have achieved higher performance with a neural network if we had more time to further process the data. But, the Random Forest model was also able to give us feature importance scores, which is useful for interpretation. We wrote a report on our findings (which can be found on my Github repo above), as well as created a video that summarized our findings, which can be found here:

<iframe src="https://medium.com/media/686d25e9dd8714491a2a2c6b474239a7" frameborder=0></iframe>

This project was challenging, especially because we only had two weeks and had to deal with a lot of different types of data, but I am proud of what we were ultimately able to achieve and learn.

### Data Logic, Visualization, and Storytelling

This was a half-semester course that taught us about the fundamentals of data visualization, including how to structure dashboards and graphs, how to integrate stakeholder feedback, and how to craft compelling stories for clients. We performed all class exercises in Tableau, learning about how to use calculated fields and various other Tableau features to create different visualizations. For the final project in this class, we had data from a NASCAR client and were tasked with creating a dashboard that will enable them to better use their current data and improve their race-time decision-making. For customization freedom, our team decided to use RShiny to build this dashboard, and we created various features that we felt would help the team with their pit stop timing. We didn’t have time to directly ask the stakeholder for feedback, which we would have liked to do if this were a longer project, but I learned a lot about RShiny (which I had never used before this project), as well as how to go from data to dashboard.

### Data Science Ethics

This class is relatively self-explanatory, but it is something that is often missed in data science education. We learned about various ethical considerations and challenges in the development of data science products, including bias, discrimination, privacy, and opacity. Through weekly readings and paper assignments, we learned how to dig deep into these issues and form arguments centered around ethical actions. For this class, our team also wrote a white paper that focused on bias and discrimination issues in algorithmic decision-making in the criminal justice system. Overall, I feel that ethics in data science will only grow more important in the future as regulation and oversight becomes more concrete, and it is a vital part of any data science education.

**Takeaways**

After all of this work, there are a few broad takeaways that I will keep with me:

### Diligent teamwork and clear communication is vital to success.

Most people think that programming knowledge and statistical expertise are the most important factors that determine success of a data science project, but that is usually not the case. Through the multiple team projects that we had this year, I not only learned about how to lead and be a part of a team, but also how important constant communication is to ensure that the team is on the same page.

### Domain knowledge and programming are not two separate entities.

If we are building a data science product in a certain industry, or performing an analysis, it is crucial to infuse domain knowledge into all aspects of the process. If we don’t know the data in and out, including how it was collected and how it represents our population, then our programming is useless.

### Learning from others with different backgrounds is powerful.

The MIDS cohort was chosen deliberately to have a diverse set of skills and backgrounds, including a medical student and an Army officer. By bringing an open mindset to every interaction and collaboration, I have learned a lot from my colleagues and teammates. Even if I may not agree with certain viewpoints or opinions, it is important that we have this dialogue so that we can all work together to learn and grow as a class.

As I head towards my summer internship at Verily, I’ll take these insights (and many others) with me, hoping to build upon them and further my journey as a data scientist. It’s been an incredible first year at Duke and I can’t wait for what’s next!

*Originally published at [http://datainallthings.wordpress.com](https://datainallthings.wordpress.com/2019/05/07/masters-year-1-recap/) on May 7, 2019.*
