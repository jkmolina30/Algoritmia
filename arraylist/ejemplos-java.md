# Ejemplos en Java: ArrayList

## Presentación

Este archivo contiene ejemplos básicos de `ArrayList` en Java.

La idea es que el estudiante comprenda cómo crear listas dinámicas, agregar datos, recorrerlos, buscarlos, modificarlos y eliminarlos.

---

# Ejemplo 1. Crear un ArrayList de nombres

```java
import java.util.ArrayList;

public class ListaNombres {
    public static void main(String[] args) {
        ArrayList<String> nombres = new ArrayList<>();

        nombres.add("Ana");
        nombres.add("Carlos");
        nombres.add("María");

        System.out.println("Nombres registrados:");

        for (int i = 0; i < nombres.size(); i++) {
            System.out.println(nombres.get(i));
        }
    }
}
```

## Explicación

```java
ArrayList<String> nombres = new ArrayList<>();
```

Crea una lista dinámica para guardar textos.

```java
nombres.add("Ana");
```

Agrega un elemento a la lista.

```java
nombres.get(i);
```

Obtiene el elemento ubicado en la posición `i`.

---

# Ejemplo 2. Registrar nombres desde teclado

```java
import java.util.ArrayList;
import java.util.Scanner;

public class RegistrarNombres {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        ArrayList<String> nombres = new ArrayList<>();

        int cantidad;
        String nombre;

        System.out.print("¿Cuántos nombres desea registrar?: ");
        cantidad = entrada.nextInt();

        entrada.nextLine();

        for (int i = 0; i < cantidad; i++) {
            System.out.print("Ingrese el nombre " + (i + 1) + ": ");
            nombre = entrada.nextLine();

            nombres.add(nombre);
        }

        System.out.println("Nombres registrados:");

        for (String n : nombres) {
            System.out.println(n);
        }

        entrada.close();
    }
}
```

---

# Ejemplo 3. ArrayList de notas

```java
import java.util.ArrayList;
import java.util.Scanner;

public class ListaNotas {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        ArrayList<Double> notas = new ArrayList<>();

        int cantidad;
        double nota;
        double suma = 0;
        double promedio;

        System.out.print("¿Cuántas notas desea ingresar?: ");
        cantidad = entrada.nextInt();

        for (int i = 0; i < cantidad; i++) {
            System.out.print("Ingrese la nota " + (i + 1) + ": ");
            nota = entrada.nextDouble();

            notas.add(nota);
        }

        for (double n : notas) {
            suma = suma + n;
        }

        promedio = suma / notas.size();

        System.out.println("Promedio: " + promedio);

        entrada.close();
    }
}
```

---

# Ejemplo 4. Validar notas en ArrayList

```java
import java.util.ArrayList;
import java.util.Scanner;

public class NotasValidadasArrayList {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        ArrayList<Double> notas = new ArrayList<>();

        int cantidad;
        double nota;

        System.out.print("¿Cuántas notas desea ingresar?: ");
        cantidad = entrada.nextInt();

        for (int i = 0; i < cantidad; i++) {
            do {
                System.out.print("Ingrese la nota " + (i + 1) + " entre 0.0 y 5.0: ");
                nota = entrada.nextDouble();
            } while (nota < 0.0 || nota > 5.0);

            notas.add(nota);
        }

        System.out.println("Notas registradas:");

        for (double n : notas) {
            System.out.println(n);
        }

        entrada.close();
    }
}
```

---

# Ejemplo 5. Buscar un nombre

```java
import java.util.ArrayList;
import java.util.Scanner;

public class BuscarNombre {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        ArrayList<String> nombres = new ArrayList<>();

        nombres.add("Ana");
        nombres.add("Carlos");
        nombres.add("María");

        String buscado;
        boolean encontrado = false;

        System.out.print("Ingrese el nombre a buscar: ");
        buscado = entrada.nextLine();

        for (String nombre : nombres) {
            if (nombre.equalsIgnoreCase(buscado)) {
                encontrado = true;
            }
        }

        if (encontrado) {
            System.out.println("El nombre está registrado");
        } else {
            System.out.println("El nombre no está registrado");
        }

        entrada.close();
    }
}
```

---

# Ejemplo 6. Modificar un elemento

```java
import java.util.ArrayList;

public class ModificarElemento {
    public static void main(String[] args) {
        ArrayList<String> nombres = new ArrayList<>();

        nombres.add("Ana");
        nombres.add("Carlos");
        nombres.add("María");

        System.out.println("Lista original: " + nombres);

        nombres.set(1, "Camila");

        System.out.println("Lista modificada: " + nombres);
    }
}
```

---

# Ejemplo 7. Eliminar un elemento

```java
import java.util.ArrayList;

public class EliminarElemento {
    public static void main(String[] args) {
        ArrayList<String> nombres = new ArrayList<>();

        nombres.add("Ana");
        nombres.add("Carlos");
        nombres.add("María");

        System.out.println("Lista original: " + nombres);

        nombres.remove("Carlos");

        System.out.println("Lista después de eliminar: " + nombres);
    }
}
```

---

# Ejemplo 8. Menú básico con ArrayList

```java
import java.util.ArrayList;
import java.util.Scanner;

public class MenuArrayList {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        ArrayList<String> tareas = new ArrayList<>();

        int opcion;
        String tarea;

        do {
            System.out.println("===== MENÚ DE TAREAS =====");
            System.out.println("1. Agregar tarea");
            System.out.println("2. Mostrar tareas");
            System.out.println("3. Eliminar tarea por posición");
            System.out.println("4. Salir");
            System.out.print("Ingrese una opción: ");
            opcion = entrada.nextInt();

            entrada.nextLine();

            switch (opcion) {
                case 1:
                    System.out.print("Ingrese la tarea: ");
                    tarea = entrada.nextLine();
                    tareas.add(tarea);
                    System.out.println("Tarea agregada");
                    break;

                case 2:
                    if (tareas.isEmpty()) {
                        System.out.println("No hay tareas registradas");
                    } else {
                        for (int i = 0; i < tareas.size(); i++) {
                            System.out.println(i + ". " + tareas.get(i));
                        }
                    }
                    break;

                case 3:
                    if (tareas.isEmpty()) {
                        System.out.println("No hay tareas para eliminar");
                    } else {
                        int posicion;

                        System.out.print("Ingrese la posición a eliminar: ");
                        posicion = entrada.nextInt();

                        if (posicion >= 0 && posicion < tareas.size()) {
                            tareas.remove(posicion);
                            System.out.println("Tarea eliminada");
                        } else {
                            System.out.println("Posición no válida");
                        }
                    }
                    break;

                case 4:
                    System.out.println("Saliendo del programa");
                    break;

                default:
                    System.out.println("Opción no válida");
                    break;
            }

        } while (opcion != 4);

        entrada.close();
    }
}
```

---

## Recomendación

Un `ArrayList` es especialmente útil cuando el usuario decide cuántos datos ingresar o cuando la lista puede cambiar durante el programa.
