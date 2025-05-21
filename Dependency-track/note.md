# Dependency-track

---

## Principles

---

* It is an Component Analysis platform that allows organizations to identify and reduce risks in the Software Supply Chain.
* It can be used with the tool dependency-check which can scan for vulnerabilities.

## Main commands

---

Terraform is a command line tool. The main commands used to manage the resources are:

1. ` curl -X "POST" "localhost:8081/api/v1/bom" \
                                                              -H "Content-Type: multipart/form-data" \
                                                              -H "X-Api-Key: [TO CHANGE]" \
                                                              -F "autoCreate=true" \
                                                              -F "projectName=[NAME]" \
                                                              -F "projectVersion=[version]" \
                                                              -F "bom=@[bom-location]"`: It exists also request with PUT parameter.
                                                        

## Good practices and tips

* The default account is admin:admin. At the first login the password has to be changed.
* The application is easily deployable with a docker-compose file. Different options can be changed to configure the api-server and frontend of Dependency-track containers.
* It is important to note that in the last versions(~4.10) the users' API-keys can be generated in team panel.
* [Link to the dependency-track documentation](docs.dependencytrack.or)
* [Link to the dependency-track GitHub](https://github.com/DependencyTrack/dependency-track)
* The application uses only CycloneDX's SBOM format.
* The application includes H2 database enabled by default. It is used for quick evaluation, testing and demonstration but **it can't be used in production**. It is recommended to use a PostgreSQL(>=12).
* It requires at least **4.95GB RAM and 2 CPU cores** but it is recommended to have **16GB RAM and 4 CPU cores** for the api-server and at least **512MB RAM and 1 CPU cores** but it is recommended to have **1GB RAM and 2 CPU cores** for the frontend.

## Feedback outil

### Pros

* Easily deployable thanks to the docker-compose file.
* The continuous analysis of the dependencies allows to quicly detect the vulnerabilities.
* Easily integrable into DevSecOps/SecDevOps pipelines thanks to the CycloneDX format.
* Monitores the components even after initial deploiement.
* Easily integrable with Gitlab CI, Github action ans Jenkins -> good automation.
* It is totally open source -> free, actively maintain and transparent.
* Possibility to configure alerts.
* 
### Cons

* Required specific databases' configuration on large dependencies project to have good performances.
* This is not a SAST.
* Can be difficult to include into non-mature environments.
* It depends on vulnerabilities databases(There are few sources) and if they lack some updates the detection will be limited.
* Required a good alerts filtering.

