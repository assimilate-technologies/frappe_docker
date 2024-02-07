# 07.02.2024

Demo instances

```
export APPS_JSON='[
  {
    "url": "https://github.com/assimilate-technologies/erpnext",
    "branch": "version-15"
  },
  {
    "url": "https://github.com/assimilate-technologies/payments",
    "branch": "version-15"
  },
  {
    "url": "https://github.com/assimilate-technologies/hrms",
    "branch": "version-15"
  },
  {
    "url": "https://github.com/assimilate-technologies/health",
    "branch": "develop"
  },
  {
    "url": "https://github.com/assimilate-technologies/lms",
    "branch": "main"
  },
  {
    "url": "https://github.com/assimilate-technologies/helpdesk",
    "branch": "main"
  },
  {
    "url": "https://github.com/assimilate-technologies/india-compliance",
    "branch": "version-15"
  },
  {
    "url": "https://github.com/assimilate-technologies/insights",
    "branch": "develop"
  },
  {
    "url": "https://github.com/assimilate-technologies/CSF_TZ",
    "branch": "version-15"
  },
  {
    "url": "https://github.com/assimilate-technologies/PropMS",
    "branch": "master"
  },
  {
    "url": "https://github.com/assimilate-technologies/copilot",
    "branch": "main"
  }
]'


docker build --build-arg=FRAPPE_PATH=https://github.com/frappe/frappe  --build-arg=FRAPPE_BRANCH=version-15 --build-arg=PYTHON_VERSION=3.10.12 --build-arg=NODE_VERSION=20.11.0 --build-arg=APPS_JSON_BASE64=$APPS_JSON_BASE64 --tag=ghcr.io/assimilate-technologies/at-erpnext:2.0.0 --file=images/custom/Containerfile .


docker push ghcr.io/assimilate-technologies/at-erpnext:2.0.0



"hrms-demo.assimilate.co.in",
"crm-demo.assimilate.co.in",
"ams-demo.assimilate.co.in",
"helpdesk-demo.assimilate.co.in",
"hms-demo.assimilate.co.in",
"erp-demo.assimilate.co.in",
"rms-demo.assimilate.co.in",
"all-demo.assimilate.co.in"



python3 easy-install.py --prod --email developer@assimilatetechnologies.com -n at-erpnext -i ghcr.io/assimilate-technologies/at-erpnext -v 2.0.0

```
