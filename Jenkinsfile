
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
        git clone -b main https://github.com/lazarjak/core-repo.git || exit 1
        
        echo "Cloning frontend-repo..."
        git clone -b develop https://github.com/lazarjak/frontend-repo.git || exit 1
        

		}
            }
        }

        stage('Build Artefacts') {
            steps {
                script {
                    // Generisanje artefakata
                    
        echo "Building core-service..."
        # Build komanda za py
        
        echo "Building frontend-bundle..."
        # Build komanda za zip
        
                }
            }
        }
    }
}

