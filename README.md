# Ejercicios-1-programaci-n-competitiva
Ejercicios para la practica de programación competitiva


#1. Función existeSumaK
Esta función toma como argumentos un vector de enteros array y un entero k, y devuelve un valor booleano que indica si existen dos números en el arreglo que sumen k:


        bool existeSumaK(std::vector<int>& array, int k) {

#2. Conjunto de complementos
Se crea un conjunto no ordenado llamado complements, que almacenará los complementos de los números en el arreglo mientras se itera sobre ellos:

    
    std::unordered_set<int> complements;



#3. bucle for-each  
Se utiliza un bucle for-each para iterar sobre cada número num en el arreglo array. Para cada número num, se calcula su complemento restando num de k. Este complemento es el número que necesitaríamos encontrar en el arreglo para que num y el complemento sumen k.
Se verifica si el complemento calculado ya está presente en el conjunto complements. Si lo está, significa que se ha encontrado una pareja de números en el arreglo que suman k, por lo que la función devuelve true.
Si el complemento no está presente en el conjunto, se inserta el número num en el conjunto. Esto se hace para que se pueda buscar su complemento en futuras iteraciones.
Si se completa la iteración sobre todo el arreglo y no se encuentra ninguna pareja de números que sumen k, la función devuelve false.



    for (int num : array) {
        int complement = k - num;
        if (complements.find(complement) != complements.end()) {
            return true;  // Si encontramos el complemento, entonces hay una pareja que suma k
        }
        complements.insert(num);
    }
    return false;  // Si no encontramos ninguna pareja que sume k

#4. Impresión del resultado:




