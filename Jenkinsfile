pipeline {
    agent any

    environment {
        PROJECT_NAME = "MyProject"
        TECHNOLOGY = "Python"
    }

    stages {
        stage('Checkout Repos') {
            steps {
                script {
                    // Kloniranje repozitorijuma
                    echo "Cloning core-repo..."
                    sh 'git clone -b main https://github.com/lazarjak/core-repo.git || exit 1'

                    echo "Cloning frontend-repo..."
                    sh 'git clone -b develop https://github.com/lazarjak/frontend-repo.git || exit 1'
                }
            }
        }

        stage('Build Artefacts') {
            steps {
                script {
                    // Generisanje artefakata
                    echo "Building core-service..."
                    // Build komanda za Python (ako ima neki specifičan build, npr. setup.py ili sl.)
                    sh 'python3 setup.py build'

                    echo "Building frontend-bundle..."
                    // Build komanda za frontend (ako je potrebno)
                    sh 'zip -r frontend-bundle.zip ./frontend-repo'
                }
            }
        }
    }
}

