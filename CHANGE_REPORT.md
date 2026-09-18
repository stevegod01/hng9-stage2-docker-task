# Change report - 18 September 2026

Baseline: `6efae0dab5d9bbe2afae4ba94da9b583540cebcf`.

## Changes

- Added a successor notice linking to the preserved exercise in [Udapeople's CI/CD labs](https://github.com/stevegod01/cdond-c3-udapeople/tree/master/labs/docker-compose), with baseline provenance and the original submission record retained.
- Removed 21,302 tracked generated dependency/bytecode files. Source manifests and lockfiles remain; original Git history and a verified local Git bundle preserve the earlier snapshot.
- Changed Compose to build the checked-in frontend and API, bind development ports to localhost, and require a disposable Django secret from the environment. The code no longer uses the committed demo key.
- Added or updated Docker build exclusions and explicit development-server commands. Corrected SQLite's path with `os.path.join(BASE_DIR, 'db.sqlite3')` in both source and consolidated copies.
- Normalized README punctuation and preserved inherited attribution/license text without inventing new authorship or licensing claims.

## Verification and limits

Both source and consolidated Compose files passed `docker compose config --quiet` with exit 0 using a new empty `DOCKER_CONFIG` directory and a disposable placeholder. The SQLite path expressions were parsed and checked against the API project directory; both READMEs passed strict UTF-8 decoding.

No image build, running container, external service, deployment, or remote CI run was attempted. Python/Django/React/Node versions remain deliberately historical and obsolete. This is a preserved internship exercise with development servers, not a production-ready application or integrated marketplace API. Original server/image references describe the historical submission only.
