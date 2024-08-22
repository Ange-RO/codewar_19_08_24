Exo 4 codewar 21/08/2024

function spinWords(string $str): string {
    // Séparation de la chaîne en mots
    $words = explode(' ', $str);
    
    // Parcours des mots pour inverser ceux qui ont cinq lettres ou plus
    foreach ($words as &$word) {
        if (strlen($word) >= 5) {
            $word = strrev($word); // Inversion du mot
        }
    }
    
    // Reconstitution de la chaîne avec les mots modifiés
    $result = implode(' ', $words);
    
    return $result;
}
