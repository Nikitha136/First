pipeline { 
    agent any 
    tools { 
          maven 'MAVEN' //Ensure name matches with configured  
    } 
    stages { 
        stage('Checkout') {  
            steps { 
                git branch: 'master', url: 
'https://github.com/Nikitha136/first.git'  
            } 
    } 
     stage('Build') {  
            steps { 
                bat 'mvn clean package'  
            } 
      } 
     stage('Test') {  
            steps { 
                bat 'mvn test'  
            } 
      } 
     stage('Run Application'){
         steps{
             bat 'java -jar target/first-0.0.1-SNAPSHOT.jar
         }
     }
    }
}
