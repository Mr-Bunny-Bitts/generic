pipeline{
  agent any
  stages {
    stage('Deploy') {
      steps { 
            echo 'hello'
            //curl -u admin:${Jfrog_token} "http://localhost:8081/artifactory/AUTOSAR-repo/" -T "C:\Users\HP\Desktop\test-main.zip"
            bat 'curl -u 'admin:${Jfrog_token}' -T "C:\\Users\\HP\\Desktop\\test-main.zip" "http://localhost:8081/artifactory/AUTOSAR-repo/" '
           }
        }
     }
}
