/*pipeline{
  agent any
  stages {
    stage('Deploy') {
      steps { 
            echo 'hello'
            //curl -u admin:${Jfrog_token} "http://localhost:8081/artifactory/AUTOSAR-repo/" -T "C:\Users\HP\Desktop\test-main.zip"
            bat 'curl -u admin:${Jfrog_token} -T "C:\\Users\\HP\\Desktop\\test-main.zip" "http://localhost:8081/artifactory/AUTOSAR-repo/" '
           }
        }
     }
}*/
pipeline{
  agent any
  stages {
    stage('Deploy') {
      steps {
        /*
        rtUpload (
          serverId: 'artifactory-server',
          spec: '''{
            "files": [
                {
                  "pattern": "C:\\Users\\HP\\Desktop\\Output.zip",
                  "target": "AUTOSAR-repo/b/"
                }
              ]
            }'''
          )*/
        rtDownload (
        serverId: 'Jfrog-server',
        spec: '''{
            "files": [
            {
              "pattern": "AUTOSAR-repo/b/",
              "target": "C:\\Users\\HP\\Desktop\\Output\\"
            }
          ]
        }'''
        )
  
      }
    }
  }
}
        
