~~ Implantando um Servidor Web Básico em Flask com Terraform na GCP ~~

~ Passos Realizados:

1. Dentro do Projeto configurar as Permissões de IAM
    - compute.instances*
    - compute.firewalls*
    
2. Ativar a API
    - API Compute Engine
    
3. Acessar o Cloud Shell do Projeto

4. Criação do Diretorio 'tf-tutorial'
    - Dentro dele criar o arquivo main.tf
    - Adicionar os parametros para criar rede e a sub-rede de nuvem privada
    - Serviços:
    - google_compute_network
    - google_compute_subnetwork

5. Criando recurso de VM do Compute Engine
   - No arquivo main.tf adicionar os parametros para criar a VM
   - Executar o comando 'terraform init' para adicionar os plug-ins necessários e criar o diretório .terraform
   - Validando a configuração do Terraform com o comando 'terraform plan'
   - Aplicando as configuração 'terraform apply'

6. Adicionando uma regra de firewall SSH personalizada
   - Adicionar os parametros no arquivo 'main.tf' para criar a regra de firewall personalizada
   - Executar 'terraform apply' para criar a regra

7. Conectar no SSH da VM criada
   
9. Criando APP Flask
   - Criar o arquivo app.py com NANO ou VIM
   - Adicionar a configuração da APP
   - Salvar e Executar o comando python3 app.py para verificar funcionamento..
 
10. Verificando a Saida;
   - Abrir outro terminal da VM e realizar o curl http://localhost:5000

11. Abrindo porta 5000 na VM
    - No arquivos main.tf adicionar os parametros para abertura de porta
    - Executar 'terraform.apply'
   
12. Adicionando uma variável de saída ao URL do servidor da WEB
    - No arquivo 'main.tf' adicionar os parametros..
    - Executar 'terraform.apply'
    - Para retornar a saída executar 'terraform output'

13. Para limpar as configurações executar 'terraform destroy'.

14. Funcionamento da APP;
    
![app-flask](https://github.com/Douglasakawe/deploy-flask-gcp-basic/assets/70275030/7b948e72-6508-4750-882e-8c1069ecb2a7)

   
