# kettle-permid-ntriples
Processing PermId n-triples files POC

To make this sample work take care of a few things:

* Download the ntriples files from https://permid.org/
* uncompress (gzip -d) the files
* Create a new project with a local graph in Neo4j Desktop
* Configure the project base folder in parameter BASE_FOLDER in main-job.kjb
* Make sure your graph project is stopped in Neo4j desktop

After that just run main-job.kjb

WARNING: It will clear out ${BASE_FOLDER}/import and temp/.
WARNING: It will remove the graph database stored in ${BASE_FOLDER}/data/databases/graph.db

After that it will create large files in ${BASE_FOLDER}/import containing nodes and relationships
Finally it will run a neo4j-import statement to load the data into database graph.db: ${BASE_FOLDER}/data/databases/graph.db

