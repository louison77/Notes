# GitHub Advanced Security

---

## Principles

---
Github Advanced Security is features suite integrated to GitHub builded for helping companies and development teams in dectecting, preventing and correct security breach in the code, dependencies and CI/CD workflows. This offer is not free.


## Main functionnalities

---
* **Code Scanning** analyses the source code for finding vulnerabilities(SAST). It uses a query engine named CodeQL integrated into GitHub. 
* **Secret Scanning** detects the exposed secrets inside the source code(even in the history and suports around 100 formats). Now the push protection is available for this feature.
* **Dependency Scanning** identifies known vulnerabilities in the code's dependencies(uses the GitHub Advisory database). The alerts are printed in the GitHub Security panel. The tool used is called Dependabot. 
* **Push Protection** blocks secrets adding in a repository with an automated push blocker if a secret is detected.

## Good practices and tips

---

* This feature is not included in the GitHub Free or GitHub Pro. It required either a GitHub Enterprise Cloud nor a GitHub Enterprise Server subscription.
* CodeQL supports a lot of programming languages.
* [GitHub Documentation on Secret Scanning](https://docs.github.com/fr/code-security/secret-scanning/introduction/about-secret-scanning)
* [GitHub Documentation on Push Protection](https://docs.github.com/fr/code-security/secret-scanning/introduction/about-push-protection)
* [GitHub Documentation on Code Scanning](https://docs.github.com/fr/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning)
* [GitHub Documentation on Dependabot](https://docs.github.com/fr/code-security/dependabot/ecosystems-supported-by-dependabot/supported-ecosystems-and-repositories)

## Feedbacks

--- 

### Pros

* Directly integrated into GitHub.
* Really easy and efficient automation.
### Cons

* The cost is rather high for small organizations.
* CodeQL customization required technical knowledge to be efficient. 
* Secret Scanning with push protection required a strict configuration to avoid risks.
  


