## install yc cli

```shell
curl https://storage.yandexcloud.net/yandexcloud-yc/install.sh | \
    bash -s -- -a
    
yc -v
Yandex Cloud CLI 0.145.0 linux/amd64
```

## install terraform

Актуальный релиз: [https://hashicorp-releases.yandexcloud.net/terraform/](https://hashicorp-releases.yandexcloud.net/terraform/)


```shell
wget https://hashicorp-releases.yandexcloud.net/terraform/1.11.2/terraform_1.11.2_linux_amd64.zip
unzip terraform_1.3.3_linux_amd64.zip
sudo mv terraform /usr/local/bin/
vi ~/.bashrc
alias tf=terraform
tf --version
 Terraform v1.11.2
 on linux_amd64
```

Альтернативный вариант (нужно местоположение вне РФ):

[https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli ](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)

```shell
wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg]
https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee
/etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install terraform
```