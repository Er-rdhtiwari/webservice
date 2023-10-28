pipeline { 
    agent any 
    tools { 
          Maven ‘mavenprj’ 
          } 
    stages {
            stage(‘Install dependencies’) { 
            steps { 
                sh ‘apt install git’ 
            } 
        } 
        stage(‘git clone’) { 
            steps { 
                git ‘<repository-url' 
            } 
        } 
         stage ('validate’) { 
            steps { 
                sh ‘mvn validate’ 
            } 
        } 
          stage (‘clean’) { 
            steps { 
                sh ‘mvn clean’ 
            } 
        } 
        stage (‘package’) { 
            steps { 
                sh ‘mvn package’ 
            } 
        } 
    } 
} 
