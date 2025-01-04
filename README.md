# movie-recommender

## Project Overview
Movies can evoke powerful emotions and offer moments of escape but deciding what to watch next often feels like a challenge. This project takes a straightforward approach to address that—by building a content-based movie recommendation system that suggests similar movies based on features like genres, cast, and storyline.
Using textual, categorical, and numerical data, the system analyzes movies to find connections and deliver tailored suggestions. It incorporates advanced embedding techniques and efficient search algorithms, ensuring a balance between accuracy and practicality. Whether you're revisiting a specific genre or looking for a movie with a similar cast, this system aims to simplify the process of discovering your next watch.

## Key Features

•	*Content-Based Filtering*: Provide recommendations by analyzing the intrinsic features of movies.

•	*Advanced Embedding Techniques*: Employs the state-of-the-art SentenceTransformer to extract meaningful representations of textual data.

•	*Scalable Search with FAISS*: Implements FAISS to make searching for similar movies lightning-fast, even for large datasets.

•	*Visual Exploration*: Features a word cloud to showcase the diversity of genres within the dataset.

## Dataset and Preprocessing
The foundation of this system is built on the MovieLens Latest Small Dataset, a lightweight version of the MovieLens dataset curated by GroupLens Research. This smaller dataset contains around 100,000 ratings across 9,000 movies, contributed by 600 users. the dataset offers a rich mix of information, including movie genres, titles, and user ratings.
Preprocessing Steps:
1.	*Feature Extraction*: Key attributes like cast, crew, genres, production companies, and taglines are carefully curated and cleaned.
2.	*Categorization*:
   
    o	Runtime: Movies are bucketed into "short," "medium," and "long" categories.
  	
    o	Vote Averages and Release Years: Normalized to ensure fairness in comparisons.
  	
These preprocessing steps ensure a high-quality dataset and a solid foundation for generating recommendations.

## Methodology
1.	Feature Engineering:
    o	A unified "content profile" for each movie was crafted by merging features with calculated weightings to highlight their importance.
    o	Text features were meticulously cleaned to enhance their clarity and relevance.
2.	Embedding Generation:
    o	Leveraged the pre-trained SentenceTransformer (all-MiniLM-L6-v2) to produce rich embeddings that capture the essence of each movie.
    o	Combined textual embeddings with scaled numerical features to create a robust feature matrix.
3.	Similarity Search:
    o	Built a FAISS index optimized for L2 distance, enabling efficient similarity queries.
    o	Designed a recommendation function that retrieves the top-N movies similar to any given input title.

## Results
To demonstrate its effectiveness, the system was tested using the beloved classic "Toy Story." The model generated a list of five recommended movies that shared similar themes, storytelling, and overall appeal. The suggestions felt like natural extensions of the "Toy Story" experience, showcasing the system's ability to understand and blend various content features seamlessly. This test highlighted its capability to provide relevant and meaningful recommendations.

## Future Enhancements
This project lays the groundwork for a system with immense potential, and future enhancements could take movie recommendations to the next level:
•	Hybrid Approach: Combine content-based filtering with collaborative filtering for even better recommendations.
•	Real-Time API Integration: Deploy an API to make the system accessible for live use.
•	Personalization: Incorporate user ratings and preferences for a more tailored experience.

## Conclusion
This project demonstrates the potential of data and machine learning to create more personalized and efficient recommendation systems. By leveraging advanced techniques like embedding generation and scalable similarity search, it addresses the challenges of delivering relevant and meaningful suggestions based on user preferences and content features.

