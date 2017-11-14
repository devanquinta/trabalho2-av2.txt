# trabalho2-av2.txt

#OBS: Ler na edição fica mais facil de compreender

Respostas das perguntas:

1-Resposta:
cat > verifcarq.sh

#!/bin/bash
arq = $1
if [ -f $arq ]
then
    echo -e "Arquivo existe!"
else
    echo -e "Arquivo não existe"
fi

2-resposta:

#!/bin/bash

echo "Digite o número que queria saber o fatorial: "
read cont

fat=1

for ((i=1; i <= $cont ; i++))
do
    fat=$(($fat*$i))
done

echo "O fatorial de $cont é: $fat"


3-Resposta:

#!/bin/bash

for vazio in $(ls)
do

   if ! [ -f $vazio  ]
   then
       echo -e "Arquivo está vazio: $vazio"
   fi
done

#OBS: no meu Ubumtu não funcionou com -s, mesmo com "if -f" depois "if -s", mas roda correto dessa forma

<# resposta certa seria: 

#!/bin/bash

for vazio in $(ls)
do
   if ! [ -s $vazio  ]
   then
       echo -e "Arquivo está vazio: $vazio"
   fi
done
#>

4-resposta

#!/bin/bash

for pesqfile in $(ls)
do
  case $pesqfile in
                 *.txt)
                 totaltxt=$(cat "$pesqfile" | wc -l *.txt)
                 echo -e "total de Arquivos txt: $totaltxt";;
                 *.py)
                 totalpy=$(cat "$pesqfile" | wc -l *.py)
                 echo -e "total de Arquivos py: $totalpy";;
                 *.c)
                 totalc=$(cat "$pesqfile" | wc -l *.c)
                 echo -e "total de Arquivos c: $totalc";;
                 *)
                  total=$(cat "$pesqfile" | wc -l )
                  echo -e "total de Arquivos : $total";;
    esac
 done
                  
                 
                 
                 


