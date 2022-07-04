pipeline {
    agent any
    stages {
        stage('CHECKOUT SOURCE') {
            steps {
                script {
                    if (env.BRANCH_NAME ==~ /^[\$\#\[\*\s\@\-\&]$/) {
                        //cleanWs()
                        //result = 'FAILURE'
                        //CODE_DIR="${WORKSPACE}/FDM"
						echo $env.BRANCH_NAME
                        //dir("${CODE_DIR}") {
                            checkout scm
                        //    sh 'npm install'
                        }
                    } else {
                        error ("In-valid Branch Name ${env.BRANCH_NAME} which contains Special characters and Spaces in branch name which is not allowed")
                        
                    }                    
                }
            }
        }
}
}
