pipeline {
agent {
label {
label "slave ssh"
customWorkspace "/mnt/pipe"
}
}
stages {
stage ("stage 1") {
steps {
sh "sudo yum install httpd -y"
sh "sudo service httpd start"
sh "sudo cp /mnt/pipe/index.html /var/www/html"
sh "chmod -R 777 /var/www/html/index.html"
}
}
}
}
