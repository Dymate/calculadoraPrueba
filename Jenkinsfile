node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'LocalMAven';
    withSonarQubeEnv() {
      sh "${mvn}/bin/mvn sonar:sonar"
    }
  }
}