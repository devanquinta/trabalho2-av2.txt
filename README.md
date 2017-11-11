# trabalho2-av2.txt
Trabalho 2 (AV2) - Valor 2,0 pontos
1-Faça um script shell que receba um nome de arquivo como parametro e 
responde se este arquivo existe ou não.

2-Reescreva o codigo abaixo usando a estrutura for.
#!/bin/bash
cont=$1
fat=1
while [ $cont -gt 0 ] 
do
  fat=$(( $fat * $cont ))
  cont=$(( $cont - 1 ))
done
echo $fat

3-Usando estrutura de repetição, faça um script para exibir todos os arquivos
da pasta atual com tamanho = 0kb (vazio).

4-Usando estrutura de repetição, faça um script para ler a PASTA ATUAL, calcular e exibir:
- O total de arquivos lidos
- O total de arquivos com a extensão .txt 
- O total de arquivos com a extensão .c
- O total de arquivos com a extensão .py


Respostas das perguntas:

1-Resposta
cat > verifcarq.sh

#!/bin/bash
arq = $1
if [ -f $arq ]
then
    echo -e "Arquivo existe!"
else
    echo -e "Arquivo não existe"
fi

