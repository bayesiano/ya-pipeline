pipeline {
  agent {
    node {
    }
  }
  parameters {
    booleanParam(name: "RUN_INTEGRATION_TESTS", defaultValue: true)
  }
  stages {
    stage('Unit Tests') {
      steps {
        ./mvnw test -D testGroups=unit
      }
    }
    stage('Integration Tests') {
      steps {
        ./mvnw test -D
      }
    }
  }
}
