pipeline {
    agent any
    stages {
        stage('pull from main branch ') {
            steps {
                git branch: 'main', url: 'https://github.com/PraveenKuber/Amazon-Jenkins.git'
            }
        }
        stage('pull from qa-demo branch ') {
            steps {
                git branch: 'qa-demo', url: 'https://github.com/PraveenKuber/Amazon-Jenkins.git'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('build') {
            steps {
                 sh 'mvn clean install'
            }
        }

    }

  post{

  success{
     echo 'Build success'
  }
    
  failure{
       echo 'Failure in the build'
   }

  }


}
