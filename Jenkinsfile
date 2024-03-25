node {
  stage('SCM') {
    git branch:'main', credentialsId: 'Project1', url: 'https://github.com/KaKundam/project1.git'
  }
 stage('SonarQube Analysis') {
 def scannerHome = tool 'SonarQube Scanner';
 withSonarQubeEnv() {
 sh "${scannerHome}/bin/sonar-scanner -Dsonar.java.binaries=. -Dsonar.projectKey=Project1 -Dsonar.login=sqa_fe54b4dc36720f3e640c294b47e5b10c8957915a"
 }
 }
}
