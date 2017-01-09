# speed-search-application
I built this for those of us (*raises hand*) who have trouble speeling and want a more adequate desktop application for helping us over come our spelling problems. Also works as a dictionary and in the future will be used for data analysis on an individuals spelling habbits to predict what words they will spell correctly/ incorrectly and possibly be used for Natural Language Processing 

# How it Works
Upon a user request in the GTK+3 GUI application, an xml parser built into Python searches a dictionary website for a definition, then scraps the results, formats it, and stores it in an SQLite3 database. The results are displayed to the user. When the user begins to type a word, the application will search the data base for similar words and suggest them to the user on a character by character basis. If the user can't find the word in the database, the application will scrap the website and then store the result in the database for easier lookup next time, else it will just retrieve the definition in the database. It can also look up each word in a sentence if the application is passed more than just a single word.

# Underneath 
I enjoyed making this because it allowed me to "flex" a lot of the programming muscles I learned in 61a. I built this about 3 weeks into the course and got to use some cool concepts. For instance, all the text retrieved from the website is stored in a special data type that can be created on command and allows the application to keep a level of abstraction. Only the text data type knows how to look its own definition up and pass it to the GUI. Each component only knows as much information as it needs to, relying heavily on the new text data type to do all the work. 
