XPath Queries and Results : 
<?xml version="1.0" encoding="UTF-8"?>
<moviesList xmlns="http://www.example.org/movies" xsi:schemaLocation="http://www.example.org/movies.xsd" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
        <movie>
                <title>Titanic</title>
                <actors>
                        <actor>Kate Winslet</actor>
                        <actor>Leonardo Dicaprio</actor>
                </actors>
                <director>James Cameron</director>
                <genre>Drama</genre>
                <academyawards>2014</academyawards>
                <goldenglobeawards>2014</goldenglobeawards>
                <playingTimes>
                        <location>Phoenix</location>
                        <time>11AM</time>
                </playingTimes>
                <rating>9</rating>
                <reviews>You won't mind seeing the Titanic sink all over again - in 3D exactly a hundred years from the moment it actually happened.</reviews>
        </movie>
        
        <movie>
                <title>The Hunger Games</title>
                <actors>
                        <actor>Jennifer Laurance</actor>
                        <actor>Liam Hemsworth</actor>
                </actors>
                <director>Gary Ross</director>
                <genre>Comedy</genre>                
                <academyawards>2016</academyawards>
                <playingTimes>
                        <location>Tempe</location>
                        <time>11AM</time>
                </playingTimes>
                <rating>9</rating>
                <reviews>Director Gary Ross has faithfully, lovingly adapted the first installment of Suzanne Collins' riveting dystopian trilogy.</reviews>
        </movie>

        <movie>
                <title>The Shawshank Redemption</title>
                <actors>
                        <actor>Tim Robbins</actor>
                        <actor>Morgan Freeman</actor>
                </actors>
                <director>Frank Darabont</director>
                <genre>Drama</genre>                
                <academyawards>2014</academyawards>
                <goldenglobeawards>2014</goldenglobeawards>
                <playingTimes>
                        <location>Wisconsin</location>
                        <time>11AM</time>
                </playingTimes>
                <rating>9.3</rating>
                <reviews>Two imprisoned men bond over a number of years, finding solace and eventual redemption through acts of common decency.</reviews>
        </movie>
        
        <movie>
                <title>The Dark Knight</title>
                <actors>
                        <actor>Christian Bale</actor>
                        <actor>Heath Ledger</actor>
                </actors>
                <director>Christopher Nolan</director>
                <genre>Drama</genre>                
                <goldenglobeawards>2016</goldenglobeawards>
                <playingTimes>
                        <location>Tenesse</location>
                        <time>11AM</time>
                </playingTimes>
                <rating>7</rating>
                <reviews>When the menace known as the Joker wreaks havoc and chaos on the people of Gotham, Batman must accept one of the greatest psychological and physical tests of his ability to fight injustice.</reviews>
        </movie>

        <userProfiles>
                <user>
                        <name>Liam</name>
                        <moviePreferences>
                                <movie>The Dark Knight</movie>
                                <movie>The Shawshank Redemption</movie>
                        </moviePreferences>
                </user>
                <user>
                        <name>Olivia</name>
                        <moviePreferences>
                                <movie>The Hunger Games</movie>
                                <movie>The Shawshank Redemption</movie>
                        </moviePreferences>
                </user>
                <user>
                        <name>William</name>
                        <moviePreferences>
                                <movie>The Hunger Games</movie>
                                <movie>Titanic</movie>
                        </moviePreferences>
                </user>
        </userProfiles>
</moviesList>

	







1. Find all movies that have been nominated for both Academy and Golden Globe awards.
/moviesList/movie[goldenglobeawards and academyawards]


<movie xmlns="http://www.example.org/movies"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <title>Titanic</title>
  <actors>
     <actor>Kate Winslet</actor>
     <actor>Leonardo Dicaprio</actor>
  </actors>
  <director>James Cameron</director>
  <genre>Drama</genre>
  <academyawards>2014</academyawards>
  <goldenglobeawards>2014</goldenglobeawards>
  <playingTimes>
     <location>Phoenix</location>
     <time>11AM</time>
  </playingTimes>
  <rating>9</rating>
  <reviews>You won't mind seeing the Titanic sink all over again - in 3D exactly a hundred years from the moment it actually happened.</reviews>
</movie>
<movie xmlns="http://www.example.org/movies"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <title>The Shawshank Redemption</title>
  <actors>
     <actor>Tim Robbins</actor>
     <actor>Morgan Freeman</actor>
  </actors>
  <director>Frank Darabont</director>
  <genre>Drama</genre>
  <academyawards>2014</academyawards>
  <goldenglobeawards>2014</goldenglobeawards>
  <playingTimes>
     <location>Wisconsin</location>
     <time>11AM</time>
  </playingTimes>
  <rating>9.3</rating>
  <reviews>Two imprisoned men bond over a number of years, finding solace and eventual redemption through acts of common decency.</reviews>
</movie>



	

























2. Find all directors that won the Academy award since 2015.
/moviesList/movie[academyawards>2015]/director


<director xmlns="http://www.example.org/movies"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">Gary Ross</director>
	







3. Find all movies from “Drama” genre with a rating of 7.5 or greater.
/moviesList/movie[genre="Drama" and rating>=7.5]




<movie xmlns="http://www.example.org/movies"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <title>Titanic</title>
  <actors>
     <actor>Kate Winslet</actor>
     <actor>Leonardo Dicaprio</actor>
  </actors>
  <director>James Cameron</director>
  <genre>Drama</genre>
  <academyawards>2014</academyawards>
  <goldenglobeawards>2014</goldenglobeawards>
  <playingTimes>
     <location>Phoenix</location>
     <time>11AM</time>
  </playingTimes>
  <rating>9</rating>
  <reviews>You won't mind seeing the Titanic sink all over again - in 3D exactly a hundred years from the moment it actually happened.</reviews>
</movie>
<movie xmlns="http://www.example.org/movies"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <title>The Shawshank Redemption</title>
  <actors>
     <actor>Tim Robbins</actor>
     <actor>Morgan Freeman</actor>
  </actors>
  <director>Frank Darabont</director>
  <genre>Drama</genre>
  <academyawards>2014</academyawards>
  <goldenglobeawards>2014</goldenglobeawards>
  <playingTimes>
     <location>Wisconsin</location>
     <time>11AM</time>
  </playingTimes>
  <rating>9.3</rating>
  <reviews>Two imprisoned men bond over a number of years, finding solace and eventual redemption through acts of common decency.</reviews>
</movie>


	

4. Find all movies playing in Phoenix directed by “XYZ”.
/moviesList/movie[playingTimes/location="Phoenix" and director="James Cameron"]


<movie xmlns="http://www.example.org/movies"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <title>Titanic</title>
  <actors>
     <actor>Kate Winslet</actor>
     <actor>Leonardo Dicaprio</actor>
  </actors>
  <director>James Cameron</director>
  <genre>Drama</genre>
  <academyawards>2014</academyawards>
  <goldenglobeawards>2014</goldenglobeawards>
  <playingTimes>
     <location>Phoenix</location>
     <time>11AM</time>
  </playingTimes>
  <rating>9</rating>
  <reviews>You won't mind seeing the Titanic sink all over again - in 3D exactly a hundred years from the moment it actually happened.</reviews>
</movie>
	















5. Find all movies with actor “ABC” and from “Comedy” genre.
/moviesList/movie[actors/actor="Jennifer Laurance" and genre="Comedy"]


<movie xmlns="http://www.example.org/movies"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <title>The Hunger Games</title>
  <actors>
     <actor>Jennifer Laurance</actor>
     <actor>Liam Hemsworth</actor>
  </actors>
  <director>Gary Ross</director>
  <genre>Comedy</genre>
  <academyawards>2016</academyawards>
  <playingTimes>
     <location>Tempe</location>
     <time>11AM</time>
  </playingTimes>
  <rating>9</rating>
  <reviews>Director Gary Ross has faithfully, lovingly adapted the first installment of Suzanne Collins' riveting dystopian trilogy.</reviews>
</movie>