Documentation
=============

Documentation about Perl CI

perlci-web
  perl-ci.pm website

perlci-api
  perl-ci.pm API
  githubhook -> add entry in perlci-db tasks
  
perlci-db
  database for tasks

perlci-orchestrator

perlci-critic

perlci-prove

perlci-coverage


## Container perlci-critic

```
docker run --rm -v /home/perlci/data/<user>/<repository>:/data/<user>/<repository>
  -e gh_user -e gh_repo -e gh_commitid 
  perlci-critic
```

entrypoint:
```
git clone/checkout http... /data/<user>/<repository>/github
cd /data/<user>/<repository>/github
perlcritic -1 --export-json /data/<user>/<repository>/perlcritic/commit_id.json
```
