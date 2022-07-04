pipeline{
    agent any
    stages{
        stage("build"){
            steps{
                echo "--------build step---------------"
                sh 'ls'
                sh 'pwd'
                sh 'cd /etc/'
                sh 'pwd'
                sh 'cd'
                sh 'pwd'
                
            }
        }
        stage("deploy"){
            steps{
                echo "--------------------deploy step-----------------------------------"
            }
        }
        
    }
}
