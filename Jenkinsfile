pipeline {
    agent { label 'slave_node' }

      stages {
         stage ('Build'){
             steps {
                 script{
                  checkout scm

                  docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {

                  def customImage = docker.build("maniengg/jersy-maven").withRun('-p 9090:9090','exec-java') {
                   
                    }  
                  }
                 }
             }
         }
      }
}
