pipeline {
    agent any
    environment {
        PATH = "/usr/share/maven/bin:$PATH"
    }
    stages {
        stage('clone') {
            steps {
                git branch: 'main', url: 'https://github.com/prasad1613/hello-w.git', credentialsId: 'b54575d8-cde3-49a3-875a-9c143b15f47f'
            }
        }
        stage('build') {
            echo "-------------- build start --------------"
            sh "mvn clean deploy -Dmaven.test.skip=true"
            echo "--------------- build end --------------"

        }
    }
}