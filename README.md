# devops-netology
Будут проигнорирован файлы:
1. все файлы в директории /.terraform/
2. файлы с раширением .tfstate и содержащие в названии .tfstate.
3. файлы crash.log и файлы начинающиеся на crash и имеющие расширение .log
4. файлы с расширением .tfvars и .tfvars.json
5. файлы override.tf и override.tf.json, а также оканчивающиеся на _override.tf и _override.tf.json
5. файлы .terraformrc и terraform.rc
