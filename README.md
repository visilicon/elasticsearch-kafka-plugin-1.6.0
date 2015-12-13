## elasticsearch-kafka-plugin-1.6.0
a plugin for sync between elasticsearch and kafka

>elastic search version : 1.6.0   </br>
>kafka version : 0.8.2.2    </br>

## kafka format
kafka message is a json string, you can can unserilized string, and get the related information   </br>

`{
  "_type"  : "web",
  "_index" : "blog",
  "_id"    : "1",
  "_action": "insert",
  "title"  : "this is a paper about the gw",
  "content": "blablablabla......"
  "tag"    : [
      "paper",
      "word",
      "segment"
  ]
}`

when you are using this format,you have posted __http://ip:port/{_type}/{_index}/{_id}__ document;   </br>
`_action` support `insert`, `update`, `delete` action, you can __add__ , __update__ , __remove__ the document in the elasticsearch.  </br>
