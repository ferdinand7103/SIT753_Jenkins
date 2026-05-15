// Mock CI/CD pipeline for SIT753 Part 1 Task 1
pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Task: Build the code using a build automation tool to compile and package the application.'
                echo 'Tool: Apache Maven (compile and package artefacts, e.g. JAR/WAR).'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Task: Run unit tests to verify individual units behave as expected; run integration tests to verify components work together.'
                echo 'Tool: JUnit (unit tests) and Mockito (mocking for integration-style tests) — often run via Maven Surefire / Failsafe.'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Task: Analyse source code for style, bugs, and maintainability against common industry rules.'
                echo 'Tool: Checkstyle (Jenkins Checkstyle Plugin or Maven plugin) integrated with Jenkins.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Task: Scan dependencies and/or source for known vulnerabilities and insecure patterns.'
                echo 'Tool: OWASP Dependency-Check (Jenkins plugin or CLI) for CVE reporting on project dependencies.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Task: Deploy the packaged application to a staging server for pre-production validation.'
                echo 'Tool: AWS CLI / EC2 (e.g. copy artefact and restart service on a staging EC2 instance).'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Task: Run integration tests against the staging environment in a production-like setup.'
                echo 'Tool: Postman + Newman (CLI) for API integration tests against the staging endpoint.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Task: Deploy the approved release to the production environment.'
                echo 'Tool: AWS CLI / EC2 (e.g. deploy to production EC2) or AWS CodeDeploy for controlled releases.'
            }
        }
    }
}
