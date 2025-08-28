pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Running Build Step..."
                echo 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                echo "Running Test Step..."
                echo 'mvn test'
            }
        }

        stage('Deploy') {
            when {
                branch 'main'
            }
            steps {
                echo "Running Deploy Step on main branch..."
            }
        }
    }
}
