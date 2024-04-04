# Trabalho-do-Bill-04-04
grupo: Amyr, João Paulo, Gabriel Felipe, Alan/
     Da ponto ai bill :)

<?php

function imprimirDivisores($numero) {
    echo "Divisores de $numero: ";
    
    for ($i = 1; $i <= $numero; $i++) {
        if ($numero % $i == 0) {
            echo "$i ";
        }
    }
}

$numero = readline("Digite um número inteiro positivo: ");

if (!is_numeric($numero) || $numero <= 0 || floor($numero) != $numero) {
    echo "Por favor, digite um número inteiro positivo válido.";
} else {
    imprimirDivisores($numero);
}

?>
