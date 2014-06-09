##Tim's notes on dogs HW Second
######This homework was intended for me to understand for loops and how to upload a CSV. I need to study this more, because my understanding of for loops is shaky and I need to remember how to import CSV's into Python. 
1. ##### How many dogs are registered in New York City? Hint: if you check out the IPython notebook above, it talks about how to convert the csv.reader variable into a list, which might give you an easy way to do it
This question was asking us to find the number of dogs registered in NYC. To do this, we needed to import the CSV that had the information, convert the CSV into a list of lists that Python can read (at least that is my understanding), and then count the number of rows in the list. First we needed to import the CSV that had the information, which we knew was at the url [I am an inline-style link]("http://jonathansoma.com/lede/dogs.csv", "dogs.csv"). To this we used this code: 
```
import urllib
urllib.urlretrieve("http://jonathansoma.com/lede/dogs.csv", "dogs.csv")
``` 
This code was used to get the CSV which is "dogs.csv" out of the URL. After this we used ```dogs = open("dogs.csv", "rb")```to have the the file read we use "rb", which does this, according to this video: [![IMAGE ALT TEXT HERE](https://www.youtube.com/watch?v=jQ9aDyBWCXI)we make it equal to dogs because we want the dogs to be easier to write, and because we need to make what is being read in the CSV a list that Python can read and we can parse. we then write this ```dogcsv = csv.reader(dogs, delimiter=',')``` which sets the delimiter as a comma. We can then save dogscsv as a list doing this ```rows = list(dogcsv)``` we can then count the rows in the list that we created from the csv by using the len() function. ```len(rows) - 1``` We subtract one because we do not want to include the header row. We get ```81524``` 

2. #####How many dogs are in Brooklyn? 
we set a vairable up, ```count```,to equal ```=``` zero ```0``` in the list we set up above "dogscsv".we then use a for loop to loop through that file that we imported. ```for row in nycdogs_list:``` "row" is a temporary variable that represents everything in the list. We then use a conditional statement to apply to the list if ```row[9] == "Brooklyn":``` then we say  ```count = count + 1``` we then print county ```print count``` and we get ```19333```the whole code block should look like this: 

```
count = 0 
for row in nycdogs_list:
    if row[9] == "Brooklyn":
        count = count + 1 
print count
```















