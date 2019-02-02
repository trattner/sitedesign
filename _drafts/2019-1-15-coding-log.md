---
layout: article
title: 'Coding Log'
date: 2019-1-15
---

1/15/19 10:30-12:30 approx, with location change (nice cafe near mathnasium to starbucks
Google cloud account with 093alt, decided need SQL database
started tutorial for app deployment
https://console.cloud.google.com/appengine/start?project=storied-port-228717&folder&organizationId
installed python dev env: including virtualenv and python3
https://cloud.google.com/python/setup
got own chess-interact folder running with quickstart: https://cloud.google.com/appengine/docs/standard/python/quickstart
HANDY command: to start app locally dev_appserver.py app.yaml

do this in virtualenv:
- setup: virtualenv --python python3 env
- activate: source env/bin/activate
- exit to leave
(for some reason virtualenv and python 2/3 compatibility issue arises, workaround just don't use virtualenv)

debugging virtualenv: FIXED!
1. create env external to directory of project:
virtualenv env
source env/bin/activate
2. cd to project
pip install -t lib -r requirements.txt
THEN dev_appserver.py app.yaml

Successfully deployed:
gcloud app deploy (had to update IAM permission for cloudbuild service account per error msg)
to view page: gcloud app browse

testing update local to deploy with text change: SUCCESS!!!!

next:
- do full stack tutorial https://cloud.google.com/appengine/docs/standard/python/getting-started/creating-guestbook
- OR just dive in:  https://cloud.google.com/appengine/docs/standard/python/getting-started/python-standard-env
