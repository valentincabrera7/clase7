# Ejercicio n1

campeones_mundiales = {

    "Campeon del Mundo 1990" : "Alemania",
    "Campeon del mundo 1994" : "Brasil",
    "Campeon del mundo 1998" : "Francia",
    "Campeon del mundo 2002" : "Brasil",
    "Campeom del mundo 2006" :  "Italia", 
    "Campeon del mundo 2010" : "España",
    "Campeon del mundo 2014" : "Alemania",
    "Campeon del mundo 2018" : "Francia",
    "Campeon del mundo 2022" : "Argentina"
    


}

for index, (año, pais) in enumerate(campeones_mundiales.items(), start=1): # index recorre enumerate
    print(f"{año}, {pais}") # lo tengo en otra filmina tambien explicado(clase 5)

# Metodos de colecciones(listas, tuplas, conjuntos y diccionarios)

cadena = ("Hola, hola, esto es una cadena")
cadena = cadena.count("hola")
print(cadena)

cadena = input("Ingrese una cadena: ")
subcadena = input("Ingrese una letra o palabra a contar: ")
cantidad = cadena.lower().count(subcadena)

if cantidad == 1:
    print(f"La letra o palabra {subcadena} aparece {cantidad} vez")
else:
    print(f"La letra o palabra {subcadena} aparece {cantidad} de veces")


# con strip() damos a entender que son los espacios para que no tire error

# Ejercico n2

"1) Pedir al usuario que ingrese una cadena"
cadena = input("Ingrese una cadena: ")
"2) Pedir al usuario que ingrese una cadena a remplazar"
cadena_remplazo = input("Ingrese una cadena a remplazar: ")
"3) Pedir al usuario que ingrese una nueva palabra"
nueva_palabra = input("Ingrese una nueva palabra: ")
"4) Verificar si la palabra a remplazar esta en la cadena"
if cadena_remplazo in cadena:
    cadena_remplazada = cadena.replace(cadena_remplazo, nueva_palabra) # creo el remplazo en un variable antes del print, sino no me lo guarda
    print("Cadena con la palabra remplazada", cadena_remplazada)
else:
    print("La palabra no esta en la cadena ingresada.")


# insert
lista = [1, 2, 3, 4]
lista.insert(0, 0) # coloca el 0 delante del 1
print(lista)

# reverse, da vuelta todo, lista.reverse()

# sort, ordena de mayor a menor

# Conjuntos

set_1 = {1, 2, 3}
set_2 = {3, 4, 5}
set_1.difference(set_2) # muestra la diferecia entre los 2 
# set_1 - set_2 es lo mismo que difference
# aca devuelve 1 y 2 porque es lo que tiene diferente, set_2 no tiene 1 y 2 

set_1 = {1, 2, 3}
set_2 = {3, 4, 5}
set_1.intersection(set_2)
# set_1 & set_2 es lo mismo que intersection
# aca devuelve el item repetido en los dos set, o sea, el 3

# las colecciones utilizan el mismo ID (cuando hago una asignacion de variables y para eso usamos copy())
# los enteros utilizan diferentes ID entre ellos
talles = {"small", "medium", "large"}
otros_talles = talles.copy() # otros_talles adquiere otro ID, porque hago una copia de talles y no me imprime lo mismo
# con copy no agrega "extra large" a talles ya que yo a talles le asigne la variable otros_talles

otros_talles.add("extra large")
print(talles)
print(otros_talles)


# Ejercicio n3

# leer una cadena del usuario usando input
oracion = input("Ingrese una oracion: ")
# convertir la cadena de texto de palabras utilizando la funcion split()
oracion = oracion.split()
print(oracion)
# convertir la lista en un conjunto para eliminar las palabras duplicadas con set 
palabras_unicas = set(oracion)
print(palabras_unicas)
# convertir el conjunto de vuelta en una lista ordenada utilizando la funcion list() y sort()
lista_palabras_unicas = list(palabras_unicas)
lista_palabras_unicas.sort()
print(lista_palabras_unicas)


# Diccionarios 

persona = {"DNI": 40979601,
           "Nombre": "Valentin",
           "Edad": 25}
persona["Domicilio"] = "Ruiz moreno 796" # sirve para agregar otro dato
persona.update({"Pais de origen": "Argentina"}) # otra forma para agregar datos
#print(persona["Nombre"])
#print(persona["Edad"])
#print(persona["DNI"])
#print(persona["Domicilio"])


for clave, valor in persona.items(): # comn items bajo clave valor, o sea, todo junto
    print(f"Clave: {clave}, Valor: {valor}")
