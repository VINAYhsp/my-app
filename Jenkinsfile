node{
   stage('SCM Checkout'){
    git 'https://github.com/VINAYhsp/my-app'
   }
   stage('Compile=-Package'){
      //Get maven home path
      def mvnHome = tool name: 'maven-3', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Email Notification'){
      mail bcc: '', body: '''hii welcome
      regards
      vinay''', cc: '', from: '', replyTo: '', subject: 'jenkins job', to: 'vinayhp962@gmail.com'
   
   }
   
}
