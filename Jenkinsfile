pipeline {
agent {
label {
label 'built-in'
customWorkspace "/data/pipeline"
}
}
stages {
stage ('install-apache-httpd') {
steps {
sh "yum install httpd -y"
}
}
stage ('deploy index file') {
steps {
sh "cp -r index.html /var/www/html"
sh "chmod -R 777 /var/www/html/index/html"
}
}
stage ('restart apache httpd') {
steps {
sh "service httpd restart"
}
}
}
}
