pipeline{
    agent any
    properties{
        VERSION = '1'
    }
    environment{
    NEW_VERSION = '1.3.0'
}
    stages{
        stage("build"){
            steps{
                echo "--------build step--------$NEW_VERSION-------"
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
