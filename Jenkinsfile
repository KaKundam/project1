node {
  stage('SCM') {
    git branch:'main', credentialsId: 'Project1', url: 'https://github.com/KaKundam/project1.git'
  }
 stage('SonarQube Analysis') {
 def scannerHome = tool 'SonarQube Scanner';
 withSonarQubeEnv() {
 sh "${scannerHome}/bin/sonar-scanner -Dsonar.java.binaries=. -Dsonar.projectKey=Project1 -Dsonar.login=sqa_c808b51e8e69d14adafe6c710dc95bcaaeecc622"
 }
 }
}
