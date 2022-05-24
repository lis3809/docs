```bash
sqoop import "-Dorg.apache.sqoop.splitter.allow_text_splitter=true" \
    --connect "jdbc:mysql://c-c9qo26aher8lc71ns36p.rw.{{ dns-zone }}:{{ port-mmy }}/db1" \
    --username "user1" \
    --P \
    --table "persons" \
    --target-dir "s3a://my-bucket/import-directory" \
    --split-by "age"
```