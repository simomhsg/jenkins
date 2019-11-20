pipeline{ 
        agent any
        stages { 
            stage('Build') { 
                steps { 
                    echo 'Building' 
                    } 
                } 
            stage('Test') { 
                steps { 
                    echo 'Testing' 
                    } 
                }
            stage('Deploy - Staging') {
                steps {
                    echo "Deploy - Staging"
                    }
                } 
            stage('Sanity check') { 
                steps { 
                    input "Does the staging environment look ok?" 
                    }
                } 
            stage('Deploy - Production') { 
                steps {
                    echo "Deploy - Production"
                    }
                } 
            } 
        post { 
            always { 
                echo 'One way or another, I have finished'
                } 
            success { 
                echo 'I succeeeded!' 
                } 
            unstable { 
                echo 'I am unstable :/'
                } 
            failure { 
                echo 'I failed :(' 
                } 
            changed { 
                echo 'Things were different before...'
                } 
            } 
        }
