node {

stage("scmcheckout")
{
git 'https://github.com/sudidelahanu185/game-of-life.git'
}
stage ("compilepackage")
{
def mvnHome=tool name: 'maven', type: 'maven'
sh "mvn clean"
}
stage("mvn package")
{
def mvnHome=tool name: 'maven', type: 'maven'
sh "${mvnHome}/bin/mvnpackage"
}
stage ("EmailNotifaction")
{
mail bcc: '', body: '''Hi
good evening 
The job is success, failure''', cc: '', from: '', replyTo: '', subject: 'hello', to: 'sudidelahanu185@gmail.com'
}
}
