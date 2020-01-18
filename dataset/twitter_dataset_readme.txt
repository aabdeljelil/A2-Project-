Twitter Elections Integrity Datasets Readme
Version 1.0
October, 2018

For information about Twitter's election integrity efforts, as well as updates to these datasets, please see https://about.twitter.com/en_us/values/elections-integrity.html#data.

I. Dataset Structure Description

The dataset contains user accounts from the following organizations:

* ira (3,613 users)
* iranian (770 users)

Note that not all of the accounts we identified as connected to these campaigns actively Tweeted, so the number of accounts represented in the datasets may be less than the total number of accounts listed here.

Each folder includes 6 types of files / folder, comprising the full archive of information disclosed about that information operation:
* _tweets_csv_hashed.zip - all tweets and metadata
* _users_csv_hashed.zip - list of users and profile metadata
* _profile_banner_hashed.zip - profile photos and profile banners. Users with the default Twitter profile pic and/or banner are not included
* _tweet_media_hashed - folder containing tweet media. Within the folder, there are a number of .zip files where each contains a number of users' tweet media (Number of .zip files varies based on the volume of media; See _tweet_media_hashed_README files for details about which users are in which numbered .zip file)
* _tweet_media_hashed_README - file that details which users' tweet media are in which numbered .zip file
* _periscope_hashed.zip - Periscope broadcasts, where each sub-folder contains the users' broadcasts (users without a Periscope account are not included; users with a Periscope account with no broadcasts have an empty sub-folder)


II. Tweet Dataset Field Descriptions

* csv files in _tweets_csv_hashed.zip and _users_csv_hashed.zip contain a number of fields listed below

tweetid - tweet identification number
userid - user identification number (anonymized for users which had fewer than 5,000 followers at the time of suspension) 
user_display_name - the name of the user (same as userid for anonymized users)
user_screen_name - the Twitter handle of the user (same as userid for anonymized users)
user_reported_location - the user's self-reported location (*)
user_profile_description - the user's profile description (*)
user_profile_url - the user's profile URL (*)
follower_count - the number of accounts following the user (*)
following_count - the number of accounts followed by the user (*)
account_creation_date - date of user account creation
account_language - the language of the account, as chosen by the user
tweet_language - the language of the tweet
tweet_text - the text of the tweet (mentions of anonymized accounts have been replaced with anonymized userid)
tweet_time - the time when the tweet was published (UTC)
tweet_client_name - the name of the client app used to publish the tweet
in_reply_to_tweetid - the tweetid of the original tweet that this tweet is in reply to (for replies only)
in_reply_to_userid - the userid of the original tweet that this tweet is in reply to (for replies only)
quoted_tweet_tweetid - the tweetid of the original tweet that this tweet is quoting (for quotes only)
is_retweet - True/False, is this tweet a retweet
retweet_userid - for retweets, the userid who authored the original tweet
retweet_tweetid - for retweets, the tweetid of the original tweet
latitude - geo-located latitude, if available 
longitude - geo-located longitude, if available 
quote_count - the number of tweets quoting this tweet
reply_count - the number of tweets replying to this tweet
like_count - the number of likes that this tweet received (^)
retweet_count - the number of retweets that this tweet received (^)
hashtags - a list of hashtags used in this tweet
urls - a list of urls used in this tweet
user_mentions - a list of userids who are mentioned in this tweet (includes anonymized userids)
poll_choices - if a tweet included a poll, this field displays the poll choices separated by |

(*) - at the time of suspension
(^) - these engagement counts exclude engagements from users who are suspended, deleted or otherwise actioned against by Twitter at the time of this data release