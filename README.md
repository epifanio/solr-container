# solr-container

Docker container for the SOLR search engine


To ingest example resords run:

´´´
docker exec CONTAINER_ID /bin/bash /ingest.sh

´´´

or (filtering ´docker ps´ for the keyword ´solr´)

´´´
docker exec $(docker ps | grep solr | sed 's/\|/ /'|awk '{print $1}') /bin/bash /ingest.sh
´´´



