# analyze-youtube-live-chat
The purpose is to get comments in the stream and identify the best scene of the stream

### Get Chat 
Get the json file containing the chat data from the Youtube Live link.
A chat replay is a page of about 50 chats, each with the URL of the next page.
The URL is explored many times until it reaches the end and the chat is obtained.
Save the timestamps and comments of each chat obtained in csv format.

### Chat Analyzer
Calculate the total number of comments per regular interval (in the code I set 15 seconds) from the chats.
Intervals with a high number of comments are considered highlights.
Points are awarded if they contain laughter or words expressing enthusiasm.
The number of comments increases at the end of the transmission or when the transmission has stopped, although it is not a high light.
So, I specified NG words and points are deducted if they are included.
The top 10 places with the highest total number of points are listed as recommended

### Reference
https://github.com/hase-ryo/youtube_livechat_replay_crawler
https://github.com/yousukeayada/youtube-api/blob/master/vtuber/get_chat_replay_info.py
https://note.com/you0832/n/ne85768f9c817
https://note.com/or_ele/n/n5fc139ff3f06
