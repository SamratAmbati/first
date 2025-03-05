pipeline{
agent any{
stages{
stage('clone'){
steps{
git 'url'
}
}
stage('Build'){
steps{
echo 'Building the project...'
sh 'javac HelloWorld.java'
}
}
stage('Test'){
steps{
echo 'Running tests...'
sh 'java HelloWorld'
}
}
stage('Deploy'){
steps{
echo 'Deploying the project...'
}
}
}
post{
success{
echo 'pipeline completed succesfully'
}
failure{
echo 'pipeline failed.'
}
}
}
}
