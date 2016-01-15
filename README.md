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

SEARCH_URL = http://elasticsearch.lightningorder.com

elasticsearch documentation    
https://www.elastic.co/guide/en/elasticsearch/reference/current/docs.html
