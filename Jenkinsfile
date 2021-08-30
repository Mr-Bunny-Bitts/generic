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
        rtUpload (
        serverId: 'artifactory-server',
        spec: '''{
              "files": [
                {
                  "pattern": "C:\\Users\\HP\\Desktop\\test-main.zip",
                  "target": "AUTOSAR-repo"
                }
            ]
        }''',
 
        // Optional - Associate the uploaded files with the following custom build name and build number,
        // as build artifacts.
        // If not set, the files will be associated with the default build name and build number (i.e the
        // the Jenkins job name and number).
        //buildName: 'holyFrog',
        //buildNumber: '42',
        // Optional - Only if this build is associated with a project in Artifactory, set the project key as follows.
        //project: 'my-project-key'
    )
      }
    }
  }
}
        
