node {
    
    stage('git-clone'){
     git credentialsId: 'github', url: 'https://github.com/blrdevopstraining/java-web-app-docker.git'   
    }
    stage('maven-build'){
      def mavenHome =  tool name: "Maven-3.8.4", type: "maven"
      def mavenCMD = "${mavenHome}/bin/mvn"
      sh "${mavenCMD} clean package"
    }
}
