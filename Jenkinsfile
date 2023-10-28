pipeline { 
    agent any 
    tools { 
          maven 'mavenprj'
          } 
    stages {
        stage('update Linux server') { 
            steps { 
                sh 'dnf install vsftpd' 
            } 
        } 
        stage('git clone') { 
            steps { 
                git 'https://github.com/Er-rdhtiwari/webservice.git' 
            } 
        } 
         stage ('validate') { 
            steps { 
                sh 'mvn validate'
            } 
        } 
          stage ('clean') { 
            steps { 
                sh 'mvn clean' 
            } 
        } 
        stage ('package') { 
            steps { 
                sh 'mvn package'
            } 
        } 
    } 
} 
