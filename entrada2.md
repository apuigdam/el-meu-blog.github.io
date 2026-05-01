**Creant una calculadora de DNI en C#**

En aquesta entrada explico com he realitzat l'activitat 3a fent servir **VSCode**.

#### El Codi Font

He creat un programa que calcula la lletra del DNI utilitzant l'operador mòdul (`%`). Aquí teniu el codi:


```
using System;

class Program {
    static void Main() {
        Console.Write("Introdueix el número del teu DNI (8 xifres): ");
        string entrada = Console.ReadLine();

        if (int.TryParse(entrada, out int numero) && entrada.Length == 8) {
            string lletres = "TRWAGMYFPDXBNJZSQVHLCKE";
            int index = numero % 23; // L'algoritme del residu
            char lletraResultat = lletres[index];
            Console.WriteLine($"El teu DNI complet és: {numero}-{lletraResultat}");
        } else {
            Console.WriteLine("Error: Entrada no vàlida.");
        }
    }
}
```

#### Proves d'execució

- **Prova 1:** Entrada `12345678` -> Sortida: `12345678-Z`.
    
- **Prova 2:** Entrada `87654321` -> Sortida: `87654321-X`.


#### Vídeo del procés (Google Vids)

A continuació podeu veure el vídeo on mostro com s'executa tot el procés al meu VSCode:
https://drive.google.com/file/d/1TPgpyTFgCfoL4ZvLtHIpeXMwc3c_be8x/view?usp=sharing