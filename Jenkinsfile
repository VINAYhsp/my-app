node{
   stage('SCM Checkout'){
    git 'https://github.com/VINAYhsp/my-app'
   }
   stage('Compile=-Package'){
      //Get maven home path
      def mvnHome = tool name: 'maven-3', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Slack Notification'){
       slackSend baseUrl: 'https://hooks.slack.com/services/',
       channel: '#jenkins',
       color: 'good',
       message: 'welcome all.... to jenkins',
       tokenCredentialId: 'slack-demo',
       username: 'HALAGUR'  
   }
   
   
}
