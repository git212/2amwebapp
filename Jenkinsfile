node{
  stage('SCM Checkout'){
    def mvn Home = tool name 'maven3',type:'maven3'
    git url
  }
  stage('compile - package'){
    sh'mvn package'
  }
}
