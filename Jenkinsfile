pipeline { 
    agent any  
    stages { 
        stage('Code Repo') { 
            steps { 
              bat 'git clone https://github.com/moh-nis/Mav.git'
              bat 'mvn clean -f Mav'
            }
        }
        stage('Test') { 
            steps { 
                bat 'mvn test -f Mav'
            }
        }
        stage('Deploy') { 
            steps {  
               bat 'mvn package -f Mav'
            }
        }
    }
}