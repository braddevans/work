# work
stuff

Design Document = Atoro
- Ruxee works on design after that

Global Database:
- Use prepared ststements for anything that accesses the database


Yiffr posts
- Type                          | type can be broken down in to category's and referenced from a database list
- Liked                         | liked posts contain userid's of the people who liked it 
- Reblogs                       | reblogs linked to post by reblog id 
- Content                       | content as in images and text?
- Creator                       | Post ids are tied to the user profile on a posts collum
- Seen number (unique)          | how many times the post has been loaded on the page per user and guest
- Comments                      | comments reference user_id, Post_id and comment_id

- Tags                          
| TAgs can be edited in the database from a most used tags list and custom tags can be in their own table and what tags reference what by linking to their post_ids



User:
- Likes                                 | tied into the same database as the yiffr_posts.liked by the user_id
- Follows                               | Get User_id to > per user database colum for following
- username                              | Username > database using prepared statements so no sql injection can occur
- Name of blog                          | specific charicters will be blocked from use like emojis, ;, if it will apear in the blogslug: [slug].yiffr.com
- email                                 | this would be under the login/signup page and the email reset page needs 
- Activity                              | Sorted User activity By Date And time of posting
- Blog banner                           | blog banners are tied to the blog_id, user_id so something like this would be parsed userid-blogid.png up to 300mB and has to be image
- Xtra info Social Network information  | Database table for each social network
- Avatar                                | avatar is parsed from a folder containing users/userid.png or gif if they are a +member or should we have gifs as default

- Description                           
| in the user database table for the user in a seperate collum so [database.users.userid.discription]

- Posts                                 
| posts would contain the content the content_type, the direct link to images stored on the network, the followers gained from that post and the reblogs in that post from other users, and or the number of posts by the user 

- Login key thing for SSO 
| user access token if they choose to stay logged in saves to their cookies the personal access token could be,
| [234234-ccgsn.ssss222.666-69oilwhat-userid-blogid-somethingelseformoreobfusication]

- Blog theme / appearance
| limmit the blog user to only pictures or gifs for the background but do [prepared statements for everything that may be referenced by the database even picture names]


Search:
- Filtered
| filtered can be from newest to oldest, views over time, ammount of reblogs, and the rating of the post being sfw or not and or tag filtering

Pages:
- Login                 
| this checks for cookies for the site previously set, 
| [prepared statments for username(username can be the name they signed up with or email) and the same for password with prepared statements],
| we would also need to make the same for a sign up page

- Main feed         
| the main feed will be automatical sorted by newest first and [whats hot] will be suggested posts

- Search 
| linked to the same [Filtered] and searches through the post text and the user name/ tag could be referenced in a search bar with #tag:sex

- Blog

- Post (modal)

- Settings 
| Page settings can be a nsfw option boolean [yes, no] page name can be edited in the settings, edit the page slug but remove anthing that would break the database or url
| so removing stuff like [, ; # ! . spaces ]

- Legal bullshit page / contact information:           
| [legal bulshit and terms of service, also DMCA stuff, and the site email]

- Donations page
- Support page


Features:
- Recommendations (not priority)
- DMs
- Block List
- Mentions @name
- Tags #tag
- Staff picks
- Commission post
- If picture, link to artist possible

- Something something, login page pictures
    - Generic sfw stuff 

- Can see only SFW if no account but direct link to picture functional.
