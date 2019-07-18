node (){
stage('git pero'){
git credentialsId: 'Git-prakashdevops', url: 'https://github.com/prakashdevops27/jenkins/'
}
stage('mvn package'){
def mvnHome= tool name: 'Maven3', type: 'maven'
def mvncomm= "${mvnHome}/bin/mvn"
sh '${mvncomm} clean package'
