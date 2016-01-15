# Elasticsearch_mappings

Use the settings and mappings in this repository to create an elasticsearch index.

**Create index with settings example:**
```
PUT http://<SEARCH_URL>/twitter/
    "settings" : {
        "index" : {
            "number_of_shards" : 3,
            "number_of_replicas" : 2
        }
    }
}'
```
(twitter is index name)

**Define mappings example:**
```
PUT http://<SEARCH_URL>/twitter/_mapping/user 
{
  "properties": {
    "name": {
      "type": "string"
    }
  }
}
```
(twitter is index name)
(user is type name)

SEARCH_URL = http://elasticsearch.lightningorder.com
Our index name: food
Our types: dish, restaurant, list

elasticsearch documentation    
https://www.elastic.co/guide/en/elasticsearch/reference/current/docs.html
