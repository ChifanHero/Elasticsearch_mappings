# Elasticsearch_mappings

Use the settings and mappings in this repository to create an elasticsearch index.

Create index with settings example:
PUT http://localhost:9200/twitter/
    "settings" : {
        "index" : {
            "number_of_shards" : 3,
            "number_of_replicas" : 2
        }
    }
}'

Define mappings example:
PUT twitter/_mapping/user 
{
  "properties": {
    "name": {
      "type": "string"
    }
  }
}
