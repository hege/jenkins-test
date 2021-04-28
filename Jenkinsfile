pipeline {
    agent any
    environment {
        ENV1 = credentials('some-global-secret')
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
                sh 'echo "ENV1 is xxx${ENV1}xxx"'
            }
        }
    }
}
