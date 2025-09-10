pipeline {
  agent any

  triggers {
    pollSCM('H/2 * * * *')
  }

  stages {
    stage('Stage 1: Build') {
      steps {
        echo 'Task: Compile and package the source code.'
        echo 'Tool: Maven'
      }
    }

    stage('Stage 2: Unit and Integration Tests') {
      steps {
        echo 'Task: Run unit tests for code correctness and integration tests to verify components work together.'
        echo 'Tool: JUnit (unit), Maven Failsafe or Testcontainers (integration)'
      }
    }

    stage('Stage 3: Code Analysis') {
      steps {
        echo 'Task: Perform static code analysis to check quality, standards, and detect issues.'
        echo 'Tool: SonarQube'
      }
    }

    stage('Stage 4: Security Scan') {
      steps {
        echo 'Task: Scan code and dependencies for known vulnerabilities.'
        echo 'Tool: Snyk'
      }
    }

    stage('Stage 5: Deploy to Staging') {
      steps {
        echo 'Task: Deploy the packaged application to a staging server (e.g., AWS EC2).'
        echo 'Tool: Ansible'
      }
    }

    stage('Stage 6: Integration Tests on Staging') {
      steps {
        echo 'Task: Execute end-to-end/integration tests in a production-like environment.'
        echo 'Tool: Postman/Newman'
      }
    }

    stage('Stage 7: Deploy to Production') {
      steps {
        echo 'Task: Deploy the application to the production environment.'
        echo 'Tool: Ansible'
      }
    }
  }
}



