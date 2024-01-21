This project is a Movie Recommender System implemented using Streamlit, a web app framework for Python. 
The recommender system suggests movies based on user-selected preferences. 
The underlying recommendation engine relies on a pre-trained model that computes the similarity between movies using their tags. 
The tags are processed using a CountVectorizer and cosine similarity to identify similar movies.

Run the app.py file and access the UI with command:  streamlit run app.py 

Here's a breakdown of the key components and steps:

1.Data Loading:
The project loads pre-processed movie data from a pickle file (movies_list.pkl) containing information about movie titles.

2.User Interface (UI):
The Streamlit app provides a simple UI with a dropdown menu where users can select a movie from the available options.

3.Recommendation Engine:
The system uses a pre-computed similarity matrix (similarity.pkl) to determine the similarity between movies. The similarity is calculated based on the tags associated with each movie.

4.Fetching Movie Posters:
The project utilizes The Movie Database (TMDb) API to fetch movie posters. The fetch_poster function takes a movie ID as input, queries the API, and returns the URL for the movie poster.

5.Recommendation Generation:
When the user clicks the "Show Recommendations" button, the system identifies the selected movie's index, computes the similarity scores, and retrieves the top 5 recommended movies along with their posters.

6.Displaying Recommendations:
The recommended movies and their posters are displayed in a responsive layout using Streamlit's st.columns functionality. Each column contains the title and poster of a recommended movie.
