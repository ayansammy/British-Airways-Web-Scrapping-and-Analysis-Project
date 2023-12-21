# British Airways Customer Reviews Analysis
Web scraping project to gain company insights

# Introduction
British Airways (BA) is the flag carrier airline of the United Kingdom (UK). Every day, thousands of BA flights arrive to and depart from the UK, carrying customers across the world. Whether it’s for holidays, work or any other reason, the end-to-end process of scheduling, planning, boarding, fuelling, transporting, landing, and continuously running flights on time, efficiently and with top-class customer service is a huge task with many highly important responsibilities.

# Objective
As a data scientist at BA, it will be your job to apply your analytical skills to influence real life multi-million-pound decisions from day one, making a tangible impact on the business as your recommendations, tools and models drive key business decisions, reduce costs and increase revenue.

Customers who book a flight with BA will experience many interaction points with the BA brand. Understanding a customer's feelings, needs, and feedback is crucial for any business, including BA.

This first task is focused on scraping and collecting customer feedback and reviewing data from a third-party source and analysing this data to present any insights you may uncover.

# Analysis
**Sentiment Analysis**

Overview

- In the initial phase of my analysis, I conducted sentiment analysis on customer reviews to gauge the overall sentiment towards British Airways. The sentiment scores were derived using the TextBlob library in Python. This library provides a simple and intuitive way to analyze the sentiment of text data, assigning polarity scores to indicate the positivity or negativity of the content. Additionally, the analysis includes subjectivity scores, which measure the degree of objectivity or subjectivity in the reviews. The sentiment scores were then used to categorize each review into one of three categories: 'Positive,' 'Neutral,' or 'Negative,' based on the polarity scores.

## Findings

**Positive Sentiment:**

- The sentiment analysis revealed a significant prevalence of positive sentiments among the customer reviews for British Airways. Key insights from the positive sentiment analysis include:
***High Satisfaction Rates:**
- The predominant height of the positive sentiment bar in the distribution plot indicates a majority of favorable evaluations. This suggests that a substantial number of customers express high satisfaction with their experiences with British Airways.
  
**Positive Customer Experiences:** 
- The overall distribution implies a favorable perception by reviewers, indicating positive experiences with the airline's services. Positive sentiments could be associated with various aspects such as excellent customer service, comfortable flights, and overall pleasant travel experiences.

**Negative Sentiment:**
- While the majority of sentiments are positive, the analysis also revealed noteworthy insights from the negative sentiment category. Key findings from the negative sentiment analysis include:

**Areas of Improvement:** 
- The less frequent but significant volume of negative reviews highlights specific areas where improvements could be beneficial. Identifying these pain points is crucial for addressing customer concerns and enhancing overall service quality.

**Common Concerns:** 
- The negative sentiment category may point to common concerns raised by customers. These concerns could include issues related to flight delays, customer service experiences, or other aspects that negatively impact the customer journey.

**Visualization Reference:**
- The visuals supporting these findings, including the sentiment distribution bar plot, can be viewed in detail in the attached Jupyter Notebook. The notebook provides a comprehensive overview of the sentiment analysis, offering a visual representation of customer sentiments towards British Airways.

## Word Clouds Analysis
I utilized word cloud visualizations to identify the most frequent words associated with customer reviews. This visual approach allowed me to pinpoint dominant themes and topics across the dataset.

**Key Insights**

**Positive Sentiment Word Cloud:**

The positive sentiment word cloud provides valuable insights into the aspects of British Airways' service that resonate positively with customers:

**Service Excellence:** 
- The prominent inclusion of the word "service" underscores the critical role that high-quality service plays in creating positive customer experiences. Customers appreciate and highlight the airline's commitment to service excellence.
**Comfortable Seating:**
- The conspicuous presence of "seat" indicates that seating comfort, along with available options, significantly contributes to passenger satisfaction. This suggests that customers find the airline's seating arrangements to be comfortable and accommodating.

**Food and Beverage Appreciation:** 
- The terms "food" and "drink" stand out, indicating that customers generally appreciate the food and beverage offerings on board. This contributes positively to the overall travel experience.
  
**Positive Flight Experiences:** 
- The central placement and size of the word "flight" suggest that customers frequently praise the general flight experience. This likely encompasses factors such as punctuality, smoothness of the journey, and overall comfort during the flight.

**Commendable Crew Interactions:** 
- The inclusion of "crew" suggests favorable interactions or experiences with the airline's staff. This highlights the impact of personal service on the overall flight experience.

**Brand Perception:** 
- The presence of "British Airways" (BA) in the word cloud associated with positive reviews indicates that customers have a favorable perception of the brand. The airline's name is often linked with positive sentiments in customer feedback.

**Premium Class Satisfaction:** 
- The distinct mention of "business class" within the cloud points to a higher level of satisfaction among passengers traveling in this premium category. It reflects positive experiences and perceptions associated with premium-class services.
***These insights provide a comprehensive understanding of the areas where British Airways excels from the perspective of its customers, offering valuable feedback for maintaining and enhancing service quality.***

**Negative Sentiment Word Cloud:**
The negative sentiment word cloud sheds light on common concerns expressed by customers in unfavorable reviews:
**Time and Delay Issues:** 
- The prominence of "time" and "delayed" indicates that customers frequently express dissatisfaction regarding flights not adhering to schedule. This encompasses complaints about flights leaving late or taking longer than expected.

**Seating Discomfort:**
- The repeated appearance of "seat" in negative reviews suggests that customers are not always satisfied with their seating arrangements. Issues related to comfort, space, or difficulties in securing desired seats contribute to negative sentiments.

**Food Challenges:** 
- While "food" appears in both positive and negative reviews, its presence in the negative cloud suggests that there are instances where customers express displeasure with the meals on the plane.

**Staff Interactions:** 
- The inclusion of "staff" in negative reviews indicates that interactions with personnel on the plane or at the airport may contribute to customer dissatisfaction. This could be attributed to perceived unhelpfulness or unfriendliness.

**London-Related Problems:** 
- The appearance of "London" hints at potential issues linked to flights to or from London or experiences at London's airports. Identifying and addressing these specific concerns is crucial for improving customer satisfaction.
***These insights draw attention to operational and service areas where British Airways could focus its efforts to enhance customer satisfaction and mitigate negative feedback effectively.***

**Common Insights from Word Clouds:**
**Service and Staff Importance:** 
- Words like "service" and "staff" are consistently prominent, indicating their significant mention across both positive and negative reviews. This emphasizes the critical role that service quality and staff interactions play in shaping customer perceptions.

**Importance of Seating:** 
- The recurring theme of "seat" in both positive and negative contexts underscores its importance in customer expectations. Seating comfort and related experiences are key considerations for passengers.

**Operational Challenges:** 
- Terms like "cancelled," "delayed," "refund," and "baggage" highlight specific operational challenges and pain points that customers frequently mention. Addressing these issues is crucial for improving overall service reliability.

**Positive and Negative Sentiments Coexisting:** 
- The presence of both positive and negative terms in the word clouds reflects the varied sentiment landscape. Customers have diverse experiences, with positive aspects often coexisting with areas that need improvement.

**Customer Expectations:** 
- The recurrence of words like "booking," "London," and specific travel-related terms indicates that customer expectations are influenced by the booking process, travel routes, and locations. Addressing these expectations is vital for a positive customer experience.

**Focus on Premium Class and Lounges:** 
- Terms like "business class" and "lounge" are distinct within the clouds, suggesting that premium services contribute significantly to both positive and negative sentiments. Focusing on enhancing these premium experiences could further elevate customer satisfaction.
***These common insights provide a holistic view of customer sentiments and areas of focus for British Airways to continue delivering exceptional service while addressing specific challenges.***


## Topic Modeling Using CountVectorizer and LatentDirichletAllocation
*Text vectorization**
- This is the process of converting textual data into a numerical representation, allowing machine learning algorithms to work with text. It involves transforming text documents into feature vectors. We will be using Count Vectorizer to perform this operation.
**CountVectorizer**
- This is a feature extraction technique used in natural language processing (NLP) to convert text data into numerical feature vectors. It is a part of the scikit-learn library in Python. CountVectorizer operates by tokenizing text documents, converting them into a matrix of token counts.
**Latent Dirichlet Allocation (LDA)**
- LDA is often categorized as a topic modeling technique, it can also be considered a form of feature engineering. It processes the features created by CountVectorizer (or another vectorizer) to discover the underlying topics in a text corpus. In doing so, it generates a new set of features related to the topics within the documents. Each document is then described by its distribution of topics, and each topic is characterized by its distribution of words. These topic distributions can be used as features in downstream tasks, such as document classification, clustering, or as part of a recommendation system.

## Topic Modeling Results
**Latent Dirichlet Allocation (LDA)**
I applied Latent Dirichlet Allocation (LDA) to identify underlying topics within the customer reviews.
**Identified Topics:**
- Topic #1: class, flight, food, good, seat, ba, business, service, crew, seats
- Topic #2: flight, ba, tokyo, british, airways, tour, service, crew, heathrow, lhr
- Topic #3: flight, ba, service, london, time, british, airways, staff, hours, heathrow
- Topic #4: flight, ba, airline, hours, time, luggage, help, airport, nov, airways
- Topic #5: flight, heading, seats, ba, airways, british, flights, london, glory, airport

## Using word cloud
**Topic 1: Premium Class Experience**

**Dominant words:**
- class, flight, food, good, seat, BA, business, service, crew, seats.
Customers appreciate the quality of service, good food, and comfortable seats associated with flying in business class. Positive sentiments are linked to premium class travel.
**Topic 2: Flights to Tokyo**
  
**Dominant words:**
- flight, BA, Tokyo, British, Airways, tour, service, crew, Heathrow, LHR.
Centered around flights to Tokyo, customers discuss service quality, crew interactions, and experiences at Heathrow Airport. The term "tour" suggests potential discussions about travel activities associated with these flights.

**Topic 3: Flights to and from London**
**Dominant words:** 
- flight, BA, service, London, time, British, Airways, staff, hours, Heathrow.
Focuses on flights to and from London, particularly Heathrow. Customers discuss service quality, staff interactions, and flight duration. Heathrow is emphasized, suggesting a connection to the London airport.

**Topic 4: General Airline Experiences**
**Dominant words:** 
- flight, BA, airline, hours, time, luggage, help, airport, Nov, Airways.
Covers various aspects of flying with British Airways, including discussions about the airline itself, luggage assistance, and airport experiences. "Nov" might be related to specific events or experiences in November.

**Topic 5: Overall Flight Experiences and Destinations**
**Dominant words:** 
- flight, heading, seats, BA, Airways, British, flights, London, glory, airport.
Encompasses discussions about flights with British Airways, focusing on seat comfort, heading to different destinations, and overall experiences at airports. The term "glory" suggests positive or memorable experiences associated with flying.

**General insights from Topic Modeling:**
- Each topic represents a different facet of the flying experience, offering nuanced insights into customer sentiments and preferences.
- Addressing specific areas highlighted in each topic can contribute to a more tailored and satisfying customer experience with British Airways.
- The detailed sentiment, word cloud, and topic analyses, along with the associated visualizations, can be explored in the Jupyter notebook attached. These findings provide a comprehensive understanding of customer feedback, enabling British Airways to enhance positive aspects, address concerns, and further improve the overall flying experience.

# Recommendation
**Operational Challenges Require Attention:**
- Negative sentiments often revolve around operational issues, especially flight delays. Addressing these challenges can significantly enhance overall service reliability.

**Seating Comfort is Paramount:**
- Both positive and negative sentiments consistently highlight the importance of seating comfort. Emphasizing this aspect can contribute to overall customer satisfaction.

**Premium Class Experiences Stand Out:**
- Positive sentiments associated with business class indicate a strong positive perception. Investing in and promoting premium services can further elevate customer satisfaction.

**Customer Feedback Loop:**
- Establish a robust customer feedback loop for continuous monitoring. Regularly collect and analyze customer feedback to identify evolving trends, address emerging concerns, and maintain a proactive approach to customer satisfaction.

**London-Specific Improvements:**
- Address concerns related to flights to and from London, especially Heathrow Airport. Implement improvements or adjustments that enhance the overall experience for customers traveling through London.

**Continuous Improvement Culture is Vital:**
- The importance of ongoing improvements is emphasized. Establishing a culture of continuous enhancement based on customer feedback ensures sustained positive experiences.


# Conclusion
- In conclusion, this comprehensive analysis of British Airways customer reviews offers a detailed perspective on passenger sentiments and key areas of concern. This wealth of insights equips British Airways with the tools needed for strategic decision-making aimed at boosting customer satisfaction. By proactively addressing identified pain points, capitalizing on positive aspects, and instituting continuous monitoring practices, British Airways can foster a customer-centric approach. This, in turn, has the potential to solidify the airline's standing in the competitive aviation industry. The findings from this analysis serve not only as a roadmap for immediate enhancements but also as a foundational resource for ongoing improvements. It underscores the impactful role of data-driven insights in steering operational excellence and shaping a positive customer experience.
