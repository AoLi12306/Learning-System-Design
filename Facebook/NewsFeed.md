Refer: https://www.youtube.com/watch?v=hykjbT5Z0oE

### What is NewsFeed.
A Facebook page display user's friends or followed pages's post. These posts could be scroll down to update.

### Key Features:
1. Fetch, user can view new posted by their friends and followed page.
2. Post. User can post and like news, new may includes text,images and videos.  
3. Link. User can send friend request to others and follow pages.

###  Design Goals
1. Miniumum Latency
2. High Availability
3. Eventually consistence(Due to CAP Theorem)
4. Read-Heavy Service(compare to write)


### Scale Estimations
1. One Billion Daily Active Users(DAUs)
2. Ten Billion News Feed requests daily
3. Each user posts twice a day on average
4. Each post is liekd five times on average
5. Each user has 200 firends
6. Each user follows about 100 pages


### Feed Generation

Steps Involved
1. Obtain the ID's of all friends and the pages followed by user
2. Retrieve the most recent and popular posts of these entities.
3. Rank these  posts based on  the relevance, and store them in a cache
4. Top posts, about in 30 number, will be returned  and displayed on the UI
5. Whenever user reaches the end of current feed, the next top posts will be fetched from server dispaly to user

Above steps only talk about how first time feed is generated and stored in the cache
Next steps should about how feed wiil be updated continuously 
Posssible solution:
1. Run feed generation process periodically (every five minutes) to add new popular posts to user feed
2. Notify user whenver server have new updates avaiable to fetch


### Feed Publish

#### Pull modal or Fan-out on load
1. Recent feed data is kept in memory on the server
2. User can pull the feed data on a regular basis or manually whenever they need it.
3. Issues with this modal:
    a. Data becomes stale unless a pull request is issued.
    b. Most pull requests may resolve in an empty repsonse if there is no new data, causing waste of resources.


#### Push model or Fan-out on write
1. Server can immediately push new updates to user.
2. Users have to maintain a Long Poll request with the server for receiving the updates.
3. Issue with this model:
    a. Server has to push updates to a lot of people when the user has millions of follwers(celebrity user).

In the interview, we will need to discuss the pros and cons of both the models, and then come up with a hybid approach that can handle feed publishing on a large scale such as Facebook.

