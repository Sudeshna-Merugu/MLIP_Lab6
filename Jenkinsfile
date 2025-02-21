pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat '''
                echo "In C or Java, we can compile our program in this step"
                echo "In Python, we can build our package here or skip this step"
                '''
            }
        }
        stage('Test') {
            steps {
                bat '''
                echo "Test Step: Running pytest"
                
                :: Initialize conda with full path
                call C:\\Users\\naras\\anaconda3\\condabin\\conda.bat init cmd.exe
                
                :: Run pytest in our conda environment with full path
                call C:\\Users\\naras\\anaconda3\\condabin\\conda.bat run -n mlip pytest
                '''
            }
        }
        stage('Deploy') {
            steps {
                bat '''
                echo "In this step, we deploy our project"
                echo "Depending on the context, we may publish the project artifact or upload pickle files"
                '''
            }
        }
    }
}