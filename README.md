# en0027-ci-dacpac-demo

Demo repository for the EN-0027 CI/CD auto-consumption E2E evidence.

Shape (mirrors Azure-Samples/sql-projects-devops-samples `main-PR-publish.yml`
and common `Azure/sql-action` deploy pipelines, deploy-only variant):
every PR targeting `main` automatically runs the fixed workflow in
`.github/workflows/db-deploy.yml`, which publishes `deploy/db.dacpac` with
SqlPackage against the preview SQL Server, using the repository secret
`CONTAINER_SQL_PASSWORD` on the command line.

Base `deploy/db.dacpac` is a clean data-tier package (no contributors declared).
