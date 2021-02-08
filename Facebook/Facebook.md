# Preparing for Your Software Engineering Interview at Facebook
https://www.facebook.com/careers/life/preparing-for-your-software-engineering-interview-at-facebook?ref=hackernoon.com

Quesiton would be open-ended and feels like a discussion
Interview will be 45 minutes long
Rarely involves coding, most time spending talking and drawing on whiteboard
The purpose of this interview is to assess the candidate's ability to solve a non-trivial engineering design problem.



# Facebook | Google | Top System Design Interview Questions (Part 1)
https://leetcode.com/discuss/interview-question/1002218/top-facebook-system-design-interview-questions

## Design Facebook Status Search
Facebook provides a search bar at the top of its page to enable its users to search posts, statuses, videos, and other forms of content posted by their friends and the pages they follow. In this question,

 - Develop a service to enable the users to search the statuses posted on Facebook by their friends and followed pages.
 - Consider that these statuses will only contain text for this particular question.

## Design Live Commenting
This question is not related to Live Videos. This question is related to the active real-time feed of comments at the bottom of each post. Thus, in this question,

 - Design the backend of a system that can enable real-time commenting on Facebook posts.
 - The users should be able to see the new comments in real-time for the posts visible in front of their screen.

## Design Facebook News Feed
In the Design Facebook News Feed question, design the following key features and their APIs.

 - Facebook users should see the news feed containing posts and statuses from their friends and pages that they have followed.
 - They can post and like statuses that may contain text, images, and videos.
 - They can send friend requests to other users and follow other pages.

## Design Facebook Messenger or WhatsApp
Develop the backend of a messenger system that can,

 - Support 1:1 conversations between two users.
 - Track the online or offline status of the users.
If time remains, discuss more complex features like Group conversations and Push notifications.


## Design Instagram
Design a simpler version of Instagram.

 - Users can upload and share photos.
 - They can follow other users.
 - Like the photos posted on Instagram.
 - Instagram users should get a scrollable feed of photos that are posted by the users they follow.

Learn more about the design goals, scale estimations, high-level design overview, and detailed architecture diagram of these problems in this video.

Source: The article published on Dev.to: https://dev.to/theinterviewsage/top-facebook-system-design-interview-questions-31np






# Facebook | Google | Top System Design Interview Questions (Part 2)
https://leetcode.com/discuss/interview-question/1042229/Facebook-or-Google-or-Top-System-Design-Interview-Questions-(Part-2)
https://www.youtube.com/watch?v=Hq8pZ8G2Lm8


## Design Proximity Server
Proximity servers are used to discover nearby attractions such as places and events, which are then recommended to Facebook users.

- Users can add, update, and delete places.
- Given a location expressed as latitude and longitude, users can query all the nearby places within a given distance.
- Optional Follow-up: Query events near a given place around a particular time. This adds the third dimension of time to the problem.

## Design Typeahead Suggestions
Google predicts and suggests a list of autocomplete queries based on the characters that we have already typed in the search box.

- Suggest the top ten search queries based on the characters already typed by the user in the search box.
- Assume query's popularity can be determined by the frequency of the query being searched in the past.

## Design Privacy Settings at Facebook
We can set different privacy levels for the Facebook posts we publish to be only visible to a specific set of users like public, friends, friends of friends, etc.

- Enable a user to specify the different levels of privacy for a post so that it is only visible to a particular set of users.
- Implement two levels of privacy, Public and Friends.
- Optional Complex Levels: friends of friends, custom groups

## Design Top N Songs
This question is very similar to designing the system for Top N Trending topics.

- Get the top N songs for a user over the past X days.
- Assume popularity of a song can be determined by the frequency of the song being listened to in the past.

## Design Web Crawler
Web Crawler scans the world wide web to download and index all the web pages to be made available for the search queries submitted by the users.

- Given a list of seed web pages, it should download all the web pages and index them for future retrieval.
- The service should handle duplicate web pages so that unique URLs are stored.

Learn more about the design goals, scale estimations, high-level design overview, and detailed architecture diagram of these problems in this video.

Source: Article published on Dev.to - https://dev.to/theinterviewsage/top-facebook-system-design-interview-questions-part-2-1844