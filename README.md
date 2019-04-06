### solrpy
---
https://github.com/search5/solrpy

```py 
import solr

s = solr.SolrConnection('http://example.org:8083/solr')

doc = {
  "id": 1,
  "title": "Lucene in Action",
  "author": ["Erik Hatcher", "Otis Gospodnetic"]
}
s.add(doc, commit=True)

response = s.query('title:lucene')
for hit in response.results:
  print hit['title']

response = s.query('title:lucene', facet='true', facet_field='subject')
response = s.query('title:lucene', facet='true', facet_field=['subject', 'publisher'])
```

```sh
curl -sSL https://raw.githubsercontent.com/moliware/traivs-solr/master/travis-solr.sh | SOLR_VERSION=4.10.3 SOLR_VERSION=4.10.3 SOLR_CONFG=tests bash
```

```
```
