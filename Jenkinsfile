node{
    stage('Git Clone'){
        git 'https://github.com/narendra9700/calcwebapp.git'
    }
    stage('Maven Package'){
        def mvnHome = tool name: 'Maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deployment'){ 
        sh 'cp target/*.war /opt/apache-tomcat-9.0.34/webapps'
    }    
}
