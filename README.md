# Using Archived Comments on Learning Videos

Developed tutoring system based on web learning. Extract the comments data and automated retrieve the textual data. In video-based tutoring systems, users can ask the questions and receive the answers from the system and aim at facilitating a learner in video-based learning. i.e., while watching a tutorial video, the users can enter a question (or some keywords) and retrieve potential helpful comments from the Q/A threads of Khan Academy tutorial videos using the textual overlap between the query and possible answers. It helps to find comments answer regarding tutoring systems. Moreover, this system itself is related to tutoring systems. It can be used to query Khan Academy comments according to some given keywords.

## Pre-configuration for Elasticsearch

Run following codes on kibana (http://localhost:5601) before storing docs

Apply `english` analyzer on `questions` index.

```
PUT questions
{
  "mappings": {
    "_doc": {
      "properties": {
        "question": {
          "type": "text",
          "analyzer": "english"
        }
      }
    }
  }
}
```

### Using virtualenv

Installing venv
`python3 -m venv env`

Activate venv
`source env/bin/activate`

Deactivate venv
`deactivate`

### Running webapp

source env/bin/activate

python web.py

Visit http://127.0.0.1:5000/
