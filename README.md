Light LDA
=========
 Modified based on MSR's Light LDA, added preprocessing scripts.

 Usage (Suppose you are in lightlda/):

 ```
 make
 ```

 ```
 cd datasets
 ```

 ```
 tar zxf 20news-train.tgz
 ```

 ```
 python scripts/pipeline.py etc/params.config
 ```

Note: parameters are defined in `etc/params.config`. The result is put in `output/model/${timestamp}/snapshot.word_topic_table.${iteration}${client_id}`. By using `python scripts/parse_word_topic_table.py` a visualization can be obtained. The `<word-id-file>` is in `output/datablocks/${timestamp}/word_tf.txt`.

Note2: The machine file defined in `etc/params.config` only works on cogito. And the whole pipeline assumes a shared filesystem.
