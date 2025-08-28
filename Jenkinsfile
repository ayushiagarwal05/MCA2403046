Pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Running Build Step..."
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                echo "Running Test Step..."
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            when {
                branch 'main'
            }
            steps {
                echo "Running Deploy Step on main branch..."
                sh './deploy.sh'
            }
        }
    }
}
