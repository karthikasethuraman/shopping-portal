pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       nodejs 'nodejs' 
    }
    

    stages{
        stage('Build'){
            steps{
                echo 'Build job invoked'
                sh 'npm install'
                
            }
        }
        stage('Test'){
            steps{
                echo 'Test job invoked'
                sh 'npm test'
                
            }
        }
        stage('Package'){
            steps{
                echo 'Package job invoked'
                sh 'npm run package'
               
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
