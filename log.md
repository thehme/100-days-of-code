100 Days Of Code - Log

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

