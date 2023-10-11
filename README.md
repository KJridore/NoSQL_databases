# NoSQL_databases
In this challenge, I undertook a comprehensive task of importing, updating, querying, and analyzing data from a MongoDB collection containing UK food establishments. Initially, I imported the provided data using the command: mongoimport --db uk_food --collection establishments –file /Users/kathia/Desktop/ChallengesFolderCamp/NoSQL_databases/Resources/establishments.json –jsonArray

After importing the data, I established a connection to the MongoDB server using the ‘MongoClient’ from the ‘pymongo’ library. I then confirmed the creation of the database and listed its collections. The ‘uk_food’ database was set to the variable db, and the ‘establishments’ collection was assigned to the variable ‘establishments_collection’. I added a new restaurant named "Penang Flavours" located in Greenwich to the database. This was achieved by creating a dictionary containing the restaurant's details and inserting it into the collection. After the successful insertion, I queried the database to ensure that the new restaurant was added correctly.

Further, I needed to update the ‘BusinessTypeID’ of the newly added restaurant. I fetched an existing ‘BusinessTypeID’ corresponding to the "Restaurant/Cafe/Canteen" type and updated the new restaurant's record with this ID.

I also performed an operation where I counted how many establishments were located under the "Dover" local authority, after which I proceeded to delete all such records. After deleting, I ensured that the data still contained other records.

An important task was data type conversion. Some of the number values, specifically the longitude and latitude under the geocode field, were stored as strings. I converted them to decimal numbers to maintain data consistency and accuracy. Additionally, for the ‘RatingValue’ field, non-rating values were set to ‘None’ and its data type was converted to integer.

Subsequently, I carried out various data analyses:
1.	I queried establishments with a hygiene score of 20 and converted the result into a pandas DataFrame to facilitate a structured display.
2.	I also retrieved establishments in London with a ‘RatingValue’ of 4 or more and similarly used pandas for data visualization.
3.	I identified the top 5 establishments with the highest rating, sorted by the lowest hygiene score, and in close proximity to "Penang Flavours".
4.	Lastly, I ran an aggregation pipeline to find the number of establishments in each Local Authority area with a hygiene score of 0.
5.	
The use of MongoDB allowed for flexible querying and data manipulation and integrating it with pandas provided a seamless way to analyze and present the results. Throughout this challenge, I employed a mix of MongoDB operations, data type transformations, and pandas operations to seamlessly interact with, modify, and visualize the data.
