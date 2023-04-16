# Anotações importantes sobre Git/GitHub

Se você deseja verificar o histórico de alterações, as mensagens de commits, o nome do autor daquele commit e outras informações sobre o projeto, existe um comando do git que pode te ajudar. Este comando é o git log.

Como já sabemos, os commits possuem hashs que os identificam de uma forma única, isto é, não existem dois commits com o mesmo hash. Com o git log podemos ver o hash e várias outras informações do commit.

Podemos visualizar todos os commits, um em cada linha com o comando:
````ruby
git log --oneline
````
Se, em vez de menos informações, quisermos ver mais como as alterações do commit, podemos usar:
````ruby
git log -p
````
Também podemos pesquisar as informações do autor daquele commit com o comando:
````ruby
git log --author="user_name"
````
E pesquisar informações por data:
````ruby
git log --since=1.month.ago --until=1.day.ago
````
No comando acima, estamos buscando as informações do commit desde um mês atrás até um dia atrás.
Você também pode formatar a visualização das informações de commit com o comando:
````ruby
git log --pretty="format:%h %s"
````
Você também pode configurar o git clone e clonar o repositório a partir de uma branch específica, diferente da original dessa forma:
````ruby
git clone -branch new_feature <repositorio>
````
Para criar uma nova branch:
````ruby
git checkout -b nome
````
Para voltar para branch anterior:
````ruby
git swit main
````
Para enviar para main especifica digite 
````ruby
git push origin nome 
````
Estamos trabalhando com duas branches: a branch main e a branch title. Fizemos várias alterações na branch title, mas, agora, queremos trazer tudo o que está na title para a main. Como podemos fazer isso?
````ruby
ggit switch main
git merge title
git push origin nome
````
