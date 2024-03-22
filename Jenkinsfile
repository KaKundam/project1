node {
  stage('SCM') {
    git branch:'main', credentialsId: 'gun', url: 'https://github.com/KaKundam/project1.git'
  }
 stage('SonarQube Analysis') {
 def scannerHome = tool 'SonarQube Scanner';
 withSonarQubeEnv() {
 sh "${scannerHome}/bin/sonar-scanner -Dsonar.java.binaries=. -Dsonar.projectKey=prj1 - Dsonar.login=sqa_450a1a96f23157a7866428db94b91ab822fefcc3"
 }
 }
}
