# trabalho2-av2.txt

#OBS: Ler na edição fica mais facil de compreender

Respostas das perguntas:

1 - Resposta:

cat > verifcarq.sh

#!/bin/bash

arq = $1

if [ -f $arq ]

then

    echo -e "Arquivo existe!"
    
else

    echo -e "Arquivo não existe"
    
fi





2 - resposta:

#!/bin/bash

echo "Digite o número que queria saber o fatorial: "

read cont

fat=1

for ((i=1; i <= $cont ; i++))

do

    fat=$(($fat*$i))
    
done

echo "O fatorial de $cont é: $fat"




3 - Resposta:

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




4 - resposta

 

#!/bin/bash

total=0

txt=0

c=0

py=0

arq=$1

for arq in $(ls)

do

case $arq in

          *.txt)
          
            echo $arq
            
            txt=$(( $txt + 1 ));;

          *c)
          
            echo $arq
            
            c=$(( $c + 1));;
            
          *py)
          
            echo $arq
            
            py=$(( py + 1));;
            
           *)
           
            echo $arq
            
            total=$((total + 1 ));;
    esac
    
done

echo "total de arquivos: $total"

echo "total de arquivos txt: $txt"

echo "total de arquivos c: $c"

echo "total de arquivos py: $py"
