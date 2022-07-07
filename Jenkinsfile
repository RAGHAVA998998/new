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
            parallel {
                stage('deploy1'){
                    when {
                        expression {
                            BRANCH_NAME == 'feature'
                        }
                    }
                    steps{
                        sh 'echo "-----------------deploy1------------------"'
                    }
            }
                stage('deploy2') {
                    steps{
                        sh 'echo deploy2'
                    }
                    
                    }
                }
        }
        
    }
}
