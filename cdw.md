function duplicateCount($text) {
    // Convertir tous les caractères en minuscules pour une comparaison insensible à la casse
    $text = strtolower($text);

    // Créer un tableau pour stocker les occurrences de chaque caractère
    $decompteChar = [];

    // Compter les occurrences de chaque caractère
    for ($i = 0; $i < strlen($text); $i++) {
        $char = $text[$i];
        if (ctype_alnum($char)) {
            if (isset($decompteChar[$char])) {
                $decompteChar[$char]++;
            } else {
                $decompteChar[$char] = 1;
            }
        }
    }

    // Compter combien de caractères apparaissent plus d'une fois
    $manyChar = 0;
    foreach ($decompteChar as $count) {
        if ($count > 1) {
            $manyChar++;
        }
    }

    return $manyChar;
}