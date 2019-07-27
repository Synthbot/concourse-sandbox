#Author: Synthbot

Start Concourse by

docker-compose up -d

fly -t tutorial login -c http://127.0.0.1:8080 -u admin -p admin

fly -t tutorial set-pipeline -p my-pipeline -c pipeline.yml -l pipeline-params.yml

Notes:
Make sure that when you add a script to your pipeline you run chmod+x.sh, git does not change the executable flag once it's been committed.

Make sure the docker image being used has the ping package installed.

More information available at:
https://concourse-ci.org/
