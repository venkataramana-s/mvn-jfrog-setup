pipeline {
agent any
tools{
maven 'maven'
jdk 'java'
}
 
stages {
stage ("initialize") {
steps {
sh '''
echo "PATH = ${PATH}"
echo "M2_HOME = ${M2_HOME}"
'''
}
}


stage ('Build project') {
steps {
dir("project_templates/java_project_template"){
sh 'mvn clean verify'
 
}
}
}
}
}
