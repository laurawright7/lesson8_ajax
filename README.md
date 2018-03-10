## Project Name:  Seminole Movie Connection Application using TMDB API

### Course Title:
LIS 2360:  Web Application Development

### Assignment Date:  
March 7, 2018

### Student Name:  
Laura Wright

### Project Description:
We used a JSON based API key from The Move Data Base so we could access their movie information to display on our website. This enabled us to get movie information onto our site running in the background, without having to reload the page each time a request for information was made. We used the JQuery AJAX method and JSON format to get the information from TMDB back to our website. 

### View Project:
(Replace this statement with your Github Page URL that was created when you 
 published the project.)

### Lessons Learned in the Assignment:
* We learned how to access data from other sites by requesting an API key, that is, a key enabling permission to use that data. We needed movie data to appear when a user typed in a movie name, and so instead of going to a server and having the page reload every time a request was made, we got an API key from The Movie Data Base. This enabled us to access the movie data running in the background, so that this could be quickly displayed to the user, without them having to wait for the page to reload each time. We put the API key into our JS file using this JQuery AJAX method:
$.ajax({
        url:'https://api.themoviedb.org/3/search/movie?api_key=7c809c9f4bc3fa97931451c4ca5b857b',
                data: query
            })
            
The URL in this code connected us to The Movie Data Base. The numbers following the key=, were the API key numbers that I was given to access the data. The 'query' was the parameter I used to search for a movie name.

* We learned how to access various categories of data from The Movie Data Base's API in the format of JSON, and transfer it into our JS file, using the JQuery AJAX method. For example, we wanted to access the overview of each movie, and used the following syntax:
$("#overview").html(json.results[0].overview);   
We called up the id 'overview' from our html, and then connected to the JSON object that contained the overview information we needed from TMDB. 


* We learned how to format the HTML to be able to receive the extra movie information that we requested from TMDB. For example, the following code shows how we created a place in our HTML for the information about the overview of the movie to be displayed.
                        <a href="#" class="list-group-item">
                        <h3 class="list-group-item-heading">Movie Plot:</h3>
                        <p class="list-group-item-text lead text-primary" id="overview"> </p>
                        </a>
We created an h3 heading called "Movie Plot", then we gave the id of "overview" to represent the space on the page that would display the movie plot. This "overview" id was then referenced in the JS file, so that it could call up the overview information we received from TMDB and transfer it to be displayed on the DOM, the HTML display page.
