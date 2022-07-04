pipeline{
    agent any
    stages{
        stage("build"){
            steps{
                echo "--------build step---------------"
                sh 'ls'
                sh 'pwd'
                sh 'docker image ls'
                
                
            }
        }
        stage("deploy"){
            steps{
                echo "--------------------deploy step-----------------------------------"
            }
        }
        
    }
}
