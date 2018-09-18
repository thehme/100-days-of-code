100 Days Of Code - Log

### Day 34: September 17, 2018

**Today's Progress**: I re-implemented the cursor adapter and got rid of the error from yesterday. I also implemented the insert method and enabled notifications, so when I add dummy date, it is refreshed in the UI.

**Thoughts**: I couldn't find any obvious differences in my new implementation of the cursor adapter today and the one from yesterday. The only thing I noticed that was different was that in the working code, I had "import android.net.Uri", but in the non-working code I had "import java.net.URI" and I am not sure why. I did not confirm this, but it is something I can look back at, if I see the same error.

### Day 33: September 16, 2018

**Today's Progress**: Merge my fix to the cursor provider today. I started to work on my curser adapter and got everything setup, but I encountered a new error today. The error says "java.lang.NullPointerException: Attempt to invoke virtual method 'android.database.Cursor com.example.android.storeinventoryapp.InventoryCursorAdaptor.swapCursor(android.database.Cursor)' on a null object reference". It seems similar to yesterday's error, so I need to spend some time debugging it again.

https://github.com/thehme/StoreInventoryApp/tree/bc-cursor-loader

**Thoughts**: I wanted to fix my code yesterday, so even though I traveled to NYC to Childrish Gambino's concert, I still took my laptop and coded all the day there. I am proud of my self for having worke on my code on  my way to a concert!

### Day 32: September 15, 2018

**Today's Progress**: I encountered an issue with my cursor provider implementation and kept getting an error about "Attempt to invoke interface method 'void android.database.Cursor.close()' on a null object reference". I had spent a lot of time, deconstructing my code, but I finally figured out that my query implementation was not returning the cursor. 

https://github.com/thehme/StoreInventoryApp/tree/master

**Thoughs**: It took me little bits of time throughout two days to figure this out and now I feel much better knowing my work was correct, but that I had left the return unchanged after auto inserting the methods.

### Day 31: September 14, 2018

**Today's Progress**: continued to work on my app, today I started to implement the cursor adapter.

**Thoughts**: I think I should have ran my update more ofter to see if it still works. I will check tomorrow when I have more brain enegy.

https://github.com/thehme/StoreInventoryApp

### Day 30: September 13, 2018

**Today's Progress**: I started to work on my store inventory app again. Today I started work on the cursor adaptor I need to retreive data from the db using the contenct provider.

**Thoughts": I feel like I know how to do this project, but I am only at the start.

https://github.com/thehme/StoreInventoryApp

### Day 29: September 12, 2018

**Today's Progress**: I spend fixing some issues with my app, first it was crashing due to an error that was not very clear:

java.lang.RuntimeException: An error occurred while executing doInBackground()

I was not using AsyncTask, so it was very weird. It turned out to be related to where in my code I was calling invalidateOptionsMenu().

**Thoughts**: I wish the Android errors gave better guidance as to how to solve the issues.

### Day 28: September 11, 2018

**Today's Progress**: Today I implemented rendering the current URi's data into a view, which will later be the view in which you can edit the data.

**Thoughts**: I had to be careful with setting the text of an input field when the value is an integer, but a string is expected. Also, i had issues figuring our the uri value, I thought I had to build it, but then realized this is defined in the onCreate method when the data item is selected from the list and this triggers the intent to be called.

### Day 27: September 10, 2018

**Today's Progress**: Today I implemented a cursor loader to load cursor data into ListView, also added an empty view to display when no data is available, added notifications, added cursor notifications to content provider to alert the main activity when a db change has occurred and the UI needs to be updated, and started to work on making my current add item view into an edit item view.

**Thoughts:** Lost happening today, but it has been nice to see everything come together. I specially liked being able to create a CursorAdapter, similar to a previous ArrayAdapter I created. The only this is that I noticed that CursorLoader may have been discontinues after API 28, so I probably have to learn how to do this diffently - https://developer.android.com/reference/android/content/CursorLoader

https://github.com/thehme/PetsShelterApp

### Day 26: September 9, 2018

**Today's Progress**: Today I implemented a cursor adapter and populated the ListView with the cursor's data.

https://github.com/thehme/PetsShelterApp

**Thoughts**: Defining the newView and bindView methods for the cursor adapter was really easy and replacing all the lines of code that were needed to populate a text view with the code to populate a ListView was nice too.

### Day 25: September 8, 2018

**Today's Progress**: Today I finished implementing a content provider and defined the delete and update methods; insert and read methods had already been done before.  

**Thoughts**: I find it really interesting to have this new design pattern. Initially I was updating the db directly, but the content provider allows for an indirect way to interact with the db that allows input validation and helps avoid type errors.

### Day 24: September 7, 2018

**Today's Progress**: Added content provider to app and started adding contacts that will be used to communicate with the content provider.

**Thoughts**: Learning about URi's and currently seems pretty complex, but hopefully I will figure out.

### Day 23: September 6, 2018

**Today's Progress**: Learning about content providers and added first content provider. 

 https://github.com/thehme/StoreInventoryApp

**Thoughts:** I like that content providers not only add an abstraction layer between the db and the UI code, but the the updating of the UI is automatically done by the content provider when a db change occurs.

### Day 22: September 5, 2018

**Today's Progress**: Started to learn about content providers to add a layer between the db and my app's activity to validate data before it is stored in the db. 

### Day 21: September 4, 2018

**Today's Progress**: Today I implemented a method to read from my app's db using a cursor. I used the cursor's data to display it in a text view and confirm that the dummy data I was inserting into the db was correct.

https://github.com/thehme/StoreInventoryApp

**Thoughts**: I learned that prices should be stored in integers and formatted later for display to avoid rounding errors. I convered an integer into a double and then used a formatter to converte it to String with a two decimal precious. 

### Day 20: September 3, 2018

**Today's Progress**: I am working on my new app and today a tried to create the INSERT method for my db. I have some issues and was not able to get dummy data saved to the db, so I will need to continue trouble shooting this tomorrow.

**Thoughts:** It seems like the INSERT sql string needs to be exact to work well and right now something seems to be wrong with my inivital attempt.

### Day 19: September 2, 2018

**Today's Progress**: Today I create the db contract for my inventory app as well as the inventory db helper class. I did not test it yet, but will do tomorrow.

**Thoughts:** I have not created a db contract with floats before, but I think that price of a product should be a float or double. I will have to figure this out once I want to print data to the UI.

### Day 18: September 1, 2018

**Today's Progress**: Today I learned how to insert date into an SQLite db using a cursor and how to read data from the cursor to display in a text view - https://github.com/thehme/PetsShelterApp/tree/starting-point. I also started a new project, which I have saved at - https://github.com/thehme/StoreInventoryApp

**Thoughts:** I now know about the C and R in CRUD, so I still need to learn how to update data or delete data from a db in SQLite, bu tfirst, I need to implement adding and reading data from my new app.

### Day 17: August 31, 2018

**Today's Progress**: Attempted to get db insert to work when input is entered by user on app.

**Thoughts:** I didn't have much luck with the insert method, need to debug something that is causing my app to crash on insert.

### Day 16: August 30, 2018

**Today's Progress**: Today I implemented the db helper for my app and added a method to add dummy date to the db.

**Thoughts**: Using the ContentValues in Android allows one to avoid typos when inserting data into a db. One should use contants to build the CREATE db method.

### Day 15: August 29, 2018

**Today's Progress**: I implemented my apps schema contract and started to work on the pet db reader class - https://github.com/thehme/PetsShelterApp/tree/starting-point 

### Day 14: August 28, 2018

**Today's Progress**: I setup a sample app called pets into my local app called https://github.com/thehme/PetsShelterApp and debugged the gradle issues and got it up and running. I also continues to learn about SQLite, specifically about contracts.

**Thoughts**: I am looking forward to adding what I am learning on my own project.

### Day 13: August 27, 2018

**Today's Progress**: Today I finished the 3rd video on using the terminal to work with GitHub and was able to complete publishing the videos. Videos can be found at https://www.youtube.com/channel/UCwxhcoHOmhD_2lXnTmD6Q5A?view_as=subscriber

**Thoughts**: Videos were recorded at convenient times, some in the morning, some at night, and it was hardest at night. The video for this day was actually published after midnight so on the morning of Aug. 28. 

### Day 12: August 26, 2018

**Today's Progress**: I promised I'd create a few videos on using the GitHub desktop app, most commonly used terminal commands, and using the terminal to work with GitHub. On this day a recorded 2 and finished editing one. https://www.youtube.com/channel/UCwxhcoHOmhD_2lXnTmD6Q5A?view_as=subscriber

**Thoughts**: Recording videos, specially for tutoring/teaching, is not that easy.

### Day 11: August 25, 2018

**Today's Progress**: Again, I spent the day playing around with SQLite in my terminal in preparation for project that requires db.

**Thoughts**: Practicing SQL commands and writing them down helps to familiarize yourself better with the language and have better expextations.

### Day 10: August 23, 2018

**Today's Progress**: I will need to create a database so this day was to play with SQLite in the terminal.

**Thoughts**: You have to be very precise with the SQLite command and very careful with the DELETE command.

### Day 9: August 22, 2018

**Today's Progress**: My goal was to get the user to be able to enter a date that I could use to make an API request for some articles on this date. At first I thought it would be great to use a calendar or date dialog, but neither solution was attainable in the time frame I have. Therefore, today I saved my work on those options and solved my issue by implementing a date type EditText view for now. I am able to enter a date, assummed to be correctly formatter, and I am able to make the HTTP request to the API and get articles I need for the single date. In the next version, I would like to implement my own custom Preference.

**Thoughts**: I still think the Android documentation is too dense, but I also just started to read it fore my projects, so maybe I need to get used to they format and style. I saved my work for the custom Preference classes that extend Date dialog and Date picker separately, so maybe I can pick up on this next time. For now, I needed to meet a deadline and so I need to move on, if I can.

**Link to work**: [Tech News App](https://github.com/thehme/TechNewsApp)

### Day 8: August 21, 2018

**Today's Progress**: found a good implementation of a custom Preferences class, but it was more than I can fully grasp at the moment, so I looked into other options. I found that there is a date dialog that I can probably display when clickin on an EditText field, so I will try this tomorrow.

**Thoughts**: I suppose it is expected that there are many ways to do one thing, but I find the documentation very dense and the google search results too old. In one case, I saw getYear and then read tthat it was deprecated, so this does not help. It would be nice if the examples in the documentation was clearer and end to end.  

**Link to work**: [Tech News App](https://github.com/thehme/TechNewsApp)

### Day 7: August 20, 2018

**Today's Progress**: Today I reverted all my preferences changes from yesterday because something was not working properly. I attempted to add the plain preferences page and once that worked, I implemented a radio button categories options pane. I then used this to build the query string to make my API request for the article objects needed for my news articles app. All is working and then spent time trying to figure out what a date picket preference would work like, but I would not get it to work.

**Thoughts**: The preferences widget is a bit involved, a simple mistyped key will break the simplest of implementations. If I were to do this over, I would always start with getting the preferences widget to first load without any options at all. Then only work on one widget and confirm the string value is retreivable, usable, and displayed in the option within the preferences.

### Day 6: August 19, 2018

**Today's Progress**: Today I spent time looking into how adding a settings menu works when using the PreferenceScreen and settings activity with a fragment. I added some of the files that will allow me to add different options for creating the query string to fetch articles from the API.

**Thoughts**: I was expecting to have something displayed, event if not completely working, but I got stuck. I am not quite sure what the connections are yet, so I need to review these concepts a bit more.

**Link to work:** [Tech News App](https://github.com/thehme/TechNewsApp)

### Day 5: August 18, 2018

**Today's Progress**: I finished learning about parsing a JSON response and properly displaying data into my android app. I then implemented a menu widget to allow the user to set preferences, which I use in the URL to make HTTP request and fetch the appropriate data.

**Thoughts:** There is lots to learn about parsing a JSON response and properly displaying data into an android app. It's pretty cool Android also provides these menu widgets to allow the user to set preferences within an app, which can then be used to update the URL via a query string. A lot of moving parts, but makes the app more interactive.  

**Link to work:** [Tech News App](https://github.com/thehme/TechNewsApp)



### Day 4: August 17, 2018

**Today's Progress**: Today I was able to parse the JSON reponse from my API request to the Guardian API. I also learned to format a String date and how to show HTML in a TextView for my Android project. I also started to look into adding a menu using a menu resource file.  

**Thoughts:** It took me some time to format the String date, which was in UTC format. Apparently you need to parse the string in its source format pattern and then also parse it again to the format you want to format it in. I also had an issue when displaying text in the TextView because it was HTML, so I looked up how to show HTML and found that I could HTML.fromHTML and it worked ok. I still have some issues with how it is displayed, but I think it works ok for now. 

**Link to work:** [Tech News App](https://github.com/thehme/TechNewsApp)



### Day 3: August 16, 2018

**Today's Progress**: Today I created a utilities class to help request data from the guardian api and parse it for use in my news app. I also added the Article Loader class and the implementation of the LoaderManager callback methods.  

**Thoughts:** I thought I had created each of my project files carefully, but I am getting an error that is not very easy to understand. My current error occurs when I try to build the app and says something about "ArticleLoader is not abstract and does not override abstract method loadInBackground() in AsyncTaskLoader". I will need to fix this tomorrow. 

**Link to work:** [Tech News App](https://github.com/thehme/TechNewsApp)



### Day 2: August 15, 2018

**Today's Progress**: Started new Android app to view a news list. Today I setup the layout files and the Article class. 

**Thoughts:** I was happy to find that creating the layour and class for the Article objects came naturally after having done this for other apps. Looking forward to feeling comfortable about other concepts.

**Link to work:** [Tech News App](https://github.com/thehme/TechNewsApp)


### Day 0: August 14, 2018

**Today's Progress**: Refactored android app to use an AsyncTaskLoader instead of an embedded AsyncTask 

**Thoughts:** This is related to the android course in Udacity and even though I am not 100% about the AsyncTask, I do see that using the AsyncTaskLoader is a great way to run multiple processes for an app. 

**Link to work:** [Earthquake App](https://github.com/thehme/EarthquakeApp)

