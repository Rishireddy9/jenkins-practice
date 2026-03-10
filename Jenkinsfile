pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', 
                    url: 'https://github.com/Rishireddy9/jenkins-practice.git'
            }
        }
        stage('Run Script') {
            steps {
                sh '''
                    chmod +x test.sh app.sh
                    echo "Running test.sh:"
                    ./test.sh
                    echo "Running app.sh:"
                    ./app.sh
                    echo "=== test.html ==="
                    cat test.html
                '''
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: '*.html', allowEmptyArchive: true
        }
    }
}
