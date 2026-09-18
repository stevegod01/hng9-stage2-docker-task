# HNG9 Docker exercise - consolidated

The preserved exercise is in [the CI/CD labs collection](https://github.com/stevegod01/cdond-c3-udapeople/tree/master/labs/docker-compose).
This repository is a historical internship exercise; the original Git history and inherited license notices are retained.

Tracked node_modules and Python bytecode have been removed; install from the checked-in manifests/lockfile. Compose now builds the checked-in sources, binds development ports only to localhost, and requires a disposable Django secret from the environment. A committed demo key is no longer used by the code.

## Local learning setup

These historical Python/Django/React/Node versions are obsolete. This is not a production-ready application and no current image-build result is claimed.

~~~sh
export DJANGO_SECRET_KEY=$(python -c "import secrets; print(secrets.token_urlsafe(48))")
docker compose config --quiet
docker compose up --build
docker compose down
~~~

PowerShell: assign the generated value to $env:DJANGO_SECRET_KEY before the Compose commands.

Inspect localhost:3000 and localhost:8000 after successful startup. The Django project is a scaffold, not an integrated marketplace API. No cloud deployment is needed. Do not expose these development servers publicly; modernization is a separate project.

The frontend and API Dockerfiles describe development servers explicitly. Both build contexts exclude dependencies, credentials and generated artifacts. Generated dependency files remain recoverable from Git history.

[Historical submission record](HISTORICAL-README.md) preserves the original server/image references without asserting current availability. LICENSE.md contains inherited public-domain/US-government language; this copy does not assert that newly written material has that provenance. No new license or authorship claim is added.
