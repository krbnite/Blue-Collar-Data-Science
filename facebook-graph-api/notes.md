

## How to get a page token
1. Go to business.facebook.com and sign in.
2. Go to the Graph API Explorer
3. Get Token: Click on one of the pages you have page-token rights to

## Comments on a given video object ID
```python
import requests
import json
response = requests.get('https://graph.facebook.com/'+obj_id+'/comments?access_token='+token)
json.loads(response.text)
```

## Likes on a given video object ID
```python
import requests
import json
response = requests.get('https://graph.facebook.com/'+obj_id+'/likes?access_token='+token)
json.loads(response.text)
```

## Reactions on a given video object ID
Note: The Reactions read API requires version v2.6 or higher.
```python
import requests
import json
response = requests.get('https://graph.facebook.com/v2.10/'+obj_id+'/reactions?access_token='+token)
json.loads(response.text)
```

## Shared posts on a given video object ID
```python
import requests
import json
response = requests.get('https://graph.facebook.com/'+obj_id+'/sharedposts?access_token='+token)
json.loads(response.text)
```

## Video Insights on a given video object ID
Note: The video insights API requires version v2.6 or higher.
```python
import requests
import json
response = requests.get('https://graph.facebook.com/v2.10/'+obj_id+'/reactions?access_token='+token)
json.loads(response.text)
```

### Print the list of Video Insight metric names
```python
response_dict = json.loads(response.text)
[item['description'] for item in response_dict['data']]
```



