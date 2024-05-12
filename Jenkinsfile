pipeline{
    agent {
        label 'graphene_spec'
    }
    parameters { 
       choice(name: 'os', choices: ['ubuntu', 'centos'], description: '')
    }
    stages(){
        stage('initialise'){
            steps{
                script{
                    echo "initialization"
                    def jenkinsfile
                    if ( os == "ubuntu" ) {
                        jenkinsfile = load 'ubuntu/Jenkinsfile1'
                    } else {
                        jenkinsfile = load 'centos/Jenkinsfile2'
                    }                    
                }
            }
        } 
    }
}