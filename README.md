# Trabalho-do-Bill-04-04
grupo: Amyr, João Paulo, Gabriel Felipe, Alan/
     Da ponto ai bill :)

<?php

function cowsay($message) {
    $cow = "
     \\   ^__^
      \\  (oo)\\_______
         (__)\\       )\\/\\
             ||----w |
             ||     ||
    ";
    
    $lines = explode("\n", wordwrap($message, 40));
    $max_length = max(array_map('strlen', $lines));
    
    $bubble_top = " " . str_repeat("_", $max_length + 2) . "\n";
    $bubble_bottom = " " . str_repeat("-", $max_length + 2) . "\n";
    
    $output = $bubble_top;
    foreach ($lines as $line) {
        $output .= sprintf("| %-" . $max_length . "s |\n", $line);
    }
    $output .= $bubble_bottom;
    
    echo "<pre>" . $output . $cow . "</pre>";
}


$message = "Olá, mundo! Venci na vida e hoje sou rico.";
cowsay($message);

?>
