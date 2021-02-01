# aws CLI use shared login session.
# boto3
## install
pip install boto3
## table
dynamodb = boto3.resource('dynamodb')
table = dynamodb.Table('tableName')
## Scan
```
done = False
start_key = None
while not done:
    if start_key:
        response = table.scan(FilterExpression=Attr("attrName").eq(attrValue), ExclusiveStartKey=start_key)
    else:
        response = table.scan(FilterExpression=Attr("attrName").eq(attrValue))
    items = response.get('Items', [])
    if len(items) > 0:
        id = items[0]['id']
    start_key = response.get('LastEvaluatedKey', None)
    done = start_key is None
```
## Query with index
```
key_condition_exp = Key('keyName').eq(value)
response = table.query(KeyConditionExpression=key_condition_exp, IndexName='index-name')
items = response['Items']
```
## Query with Partition key
```
key_condition_exp = Key('id').eq(id)
response = table.query(KeyConditionExpression=key_condition_exp)
items = response['Items']
```

# Python
用 `class` 创建类，如果需要转JSON，`__dict__`
可用匿名类直接创建 key-value 形式的对象，可直接序列化`json.dumps()`
## 文件操作
### 读
```
def get_user_emails():
    userEmails = json.loads(loan_json_file('users.json'))
    return userEmails
```

```
def loan_json_file(file_name):
    with open(file_name, 'r') as f:
        data_str = f.read()[0:]
        return data_str
```
### 写
```
    with open(f'./finalResult.json', 'w') as f:
        f.write(json.dumps(object))
```

## for 
- range
```
for i in range(1, last_index, 1):
```
- list with index
```
for index, id in enumerate(application_ids):
```
- list 
```
for item in items:
```