import tweepy

# 替换以下变量的值
consumer_key = '你的consumer_key'
consumer_secret = '你的consumer_secret'
access_token = '你的access_token'
access_token_secret = '你的access_token_secret'

# 认证并创建API对象
auth = tweepy.OAuthHandler(consumer_key, consumer_secret)
auth.set_access_token(access_token, access_token_secret)

api = tweepy.API(auth)

# 要发布的推文内容
tweet = "这是我自动发布的推文！"

# 发布推文
api.update_status(status=tweet)

print("推文已发布！")
