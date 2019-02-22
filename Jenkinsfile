  node{
   stage('SCM Checkout'){
     git 'https://github.com/smandava79/my-app.git'
   }
   stage('Compile-Package'){
    
      def mvnHome =  tool name: 'maven-3', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Email Notification'){
      mail bcc: '', body: '''Hi Welcome to jenkins email alerts
      Thanks
      Sreeni''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'sreeni79.devops@gmail.com'
   }
   
}


