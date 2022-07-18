pipeline{
    agent any
 
    parameters {
    string defaultValue : 'Jenkinsfile', description : '', name: 'jenkinsfileParameter',trim : false
    }
    environment{
    NEW_VERSION = '1.3.0'
}
    stages{
        stage("build"){
            steps{
                echo "--------build step--------$NEW_VERSION-------${jenkinsfileParameter}"
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
                            BRANCH_NAME == 'gh-pages'
                        }
                    }
                    steps{
                        sh 'echo "-----------------deploy1------------------"'
                        sh 'minikube start'
                        sh 'helm list'
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
