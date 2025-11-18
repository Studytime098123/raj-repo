# raj-repo



curl -v -u "username:password" \
  --upload-file yourfile.zip \
  "http://<nexus-host>:8081/repository/<repo-name>/<path-in-repo>/yourfile.zip"







git branch: 'dev', credentialsId: 'nexus-cred', url: 'https://github.com/Studytime098123/raj-repo.git'







pipeline {
    agent any

    options {
        skipDefaultCheckout(true)
    }

    stages {

        stage('Clone Shared Library Repo') {
            steps {
                git branch: 'GSNA-60750',
                    credentialsId: 'YOUR_CORRECT_CREDENTIAL_ID',
                    url: 'https://alm-github.systems.uk.hsbc/GSNA/gcp-jenkins-shared-library.git'
            }
        }

    }
}






                    
