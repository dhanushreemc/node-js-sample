pipeline {
    agent any
    stages {
         stage("checkout"){
             steps {
                checkout scm
             }
         }
         stage("build") {
             steps {
                 sh "sudo docker build testapp ."
             }
         }
         stage("run"){
             steps {
                  sh "sudo docker run -d -p 5000:5000 --name testapp testapp"
             }
         }
     }
}
