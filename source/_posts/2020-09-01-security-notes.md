---
title: What everyone must know about security
date: 2020-09-01 08:28:51
tags: security
---

- Never push credential, secrets, password to a public repo or even private repo as plain text

- CIA - confidentiality, integrity, availability

- POLP - principle of least Privilege
	- start with minimum access and permissions, only add permission when it is needed.
	- the access should be temporary. No need to perminently access to production env or database

- Always trouble shoot in the dev environment, do NOT jump straight to the production environment

- Avoid manual access and write to the production env. Use the code to access. The code has to push to build pipeline first. Only when the pipeline is green, the set of code can be used.

- Updating outdated dependencies is very important. The best way is to use some auto checking tools for dependencies, and include it in the pipeline

- Be very careful with logging. Do not log sensitive info. Keep PII in mind.