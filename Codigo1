from lifestore_file import lifestore_products, lifestore_sales, lifestore_searches
#lifestore_searches = [id_search, id product]
#lifestore_sales = [id_sale, id_product, score (from 1 to 5), date, refund (1 for true or 0 to false)]
#lifestore_products = [id_product, name, price, category, stock]
#definimos los usuarios que tendrán acceso
#[id de usuario, contraseña]
admins = [["A1","abc"],["A2","def"],["B1","ghi"],["B2","jkl"], ["C1","mno"],["C2","pqr"]]

#enviamos un mensaje de bienvenida
print ("Bienvenido al sistema de análisis de LifeStore." )

#solicitamos el usuario y la contraseña al usuario
usuario = input ("\nPor favor, ingrese su ID de usuario: ")
contraseña = input ("Por favor, ingrese su contraseña: ")

#definimos las variables de validación del usuario 
valido = 0
intentos = 0
#Definimos las listas que nos servirán para las iteraciones
lista = []
lista2 = []
lista3 = []
lista4 = []
lista5 = []
lista6 = []
lista7=[]
procesadores = []
tarjetas_video = []
tarjetas_madre = []
discos = []
memorias = []
pantallas = []
bocinas = []
audifonos = []
sums = []
prev = 0
curr_sum = 0
ene = []
feb = []
mar = []
abr = []
may = []
jun = []
jul = []
ago = []
sep = []
oct = []
nov = []
dic = []
#definimos variables que serán de apoyo para las iteraciones
a = 0
b = 0
i =0
suma = 0
#definimos una lista con las categorías posibles para los productos
#Realizamos los bucles que nos permitan validar al usuario
while valido != 1:
  for admin in admins: 
    if admin[0] == usuario and admin[1] == contraseña: 
      valido = 1
  #Solicitamos al usuario nuevamente el ingreso de sus credenciales    
  if valido == 0:
    print ("Datos incorrectos, por favor ")
    usuario = input ("Por favor, ingrese su ID de usuario: ")
    contraseña = input ("Por favor, ingrese su contraseña: ")
    

#Una vez validado el usuario, imprimimos un mensaje y desplegamos un menú con las opciones principales. 
if valido == True: 
  print ("\nUsuario validado")
  print ("\nElige una de las siguientes opciones: ")
  print ("\na) Análisis de ventas y búsquedas de productos.")
  print ("b) Análisis de reseñas de productos.")
  print ("c) Análisis de ventas totales.")
  opc = input("\nOpción elegida: ")
#Definimos el proceso a seguir si la opción elegida es la a, la cual es desplegar un nuevo submenú. 
  if opc == "a":
    print("\nBienvenido al análisis de ventas y búsquedas de productos.")
    print("Elige una de las siguientes opciones: ")
    print ("\na) Productos con mayores ventas.")
    print ("b) Productos con mayores búsquedas.")
    print ("c) Por categoría, productos con menores ventas.")
    print ("d) Por categoría, productos con menores búsquedas.")
    opc = input("\nOpción elegida: ")
    #Si la opción es a, realizamos las iteraciones para obtener los productos más vendidos.
    if opc == "a":
      contador = 0
      print ("\nEl top 10 de productos más vendidos es: \n")
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1]:
            contador +=1
        if contador !=0:
          lista.append([producto[0],producto[1],contador])
          contador = 0
#Ordenamos la lista de mayor a menor
      lista.sort(key = lambda x: x[2], reverse = True) 
#Imprimimos los primeros 10 elementos de la lista ordenada.      
      for i in range(0,10):
        print (str(i+1) +  ". " + lista[i][1] + "  del cual se han vendido " + str(lista[i][2]) + " unidades\n")

#Si la opción es b, nuevamente realizamos las iteraciones, pero esta vez sobre los productos y las búsquedas, contabilizando el número de estas por producto. 
    if opc == "b":
      contador =0
      print ("\nEl top 10 de productos más buscados es: \n")
      for producto in lifestore_products:
        for search in lifestore_searches:
          if producto[0] == search[1]:
            contador += 1
        if contador !=0:
          lista.append([producto[0],producto[1],contador])
          contador = 0
#Ordenamos la lista de mayor a menor.
        lista.sort(key = lambda x: x[2], reverse = True)
#Imprimimos los primeros 10 elementos.
      for i in range(0,10):
        print (str(i+1) +  ". " + lista[i][1] + "  el cual ha sido buscado " + str(lista[i][2]) + " veces\n")
#Establecemos que la variable de opción elegida sea igual a cero, para evitar que continúe realizando las iteraciones para los menús subsecuentes.
      opc = 0
    
#Si la opción es c, nuevamente realizamos las ioteraciones, pero esta vez empleando las listas creadas para cada una de las categorias de los productos.
    if opc == "c":
      print ("\nPor categorías, productos con menores ventas: \n")
      contador = 0
#Realizamos la iteraci+on para obtner la lista de categoría      
      for producto in lifestore_products:
        if producto[3] == "procesadores":
          procesadores.append([producto[0],producto[1]])
#Realizamos la iteración para conocer los productos que si hayan sido buscados para esta categoría.      
      for procesador in procesadores:
        for venta in lifestore_sales:
          if procesador[0] == venta[1]:
            contador +=1
        if contador !=0:
          lista.append([procesador[0],procesador[1],contador])
          contador = 0
#Ordenamos la lista de menor a mayor      
      lista.sort(key = lambda x: x[2], reverse = False)
#Imprimimos los resultados.
      print("Procesadores \n")
      print("1." + procesadores[8][1] + " el cual ha sido vendido 0 veces \n" )
      for i in range(0,4):
        print (str(i+2) +  ". " + lista[i][1] + "  el cual ha sido vendido " + str(lista[i][2]) + " veces\n")
      
      lista = []
#Realizamos la iteraci+on para obtner la lista de categoría
      for producto in lifestore_products:
        if producto[3] == "tarjetas de video":
          tarjetas_video.append([producto[0],producto[1]])
#Realizamos la iteración para conocer los productos que si hayan sido buscados para esta categoría. 
      for tarjeta in tarjetas_video:
        for venta in lifestore_sales:
          if tarjeta[0] == venta[1]:
            contador +=1
        if contador !=0:
          lista.append([tarjeta[0],tarjeta[1],contador])
          contador = 0
      lista.sort(key = lambda x: x[2], reverse = False)
      print("\nTarjetas de video \n")
#Imprimimos los resultados      
      print("1." + tarjetas_video[4][1] + " el cual ha sido vendido 0 veces \n" )
      print("2." + tarjetas_video[5][1] + " el cual ha sido vendido 0 veces \n" )
      print("3." + tarjetas_video[6][1] + " el cual ha sido vendido 0 veces \n" )
      print("4." + tarjetas_video[9][1] + " el cual ha sido vendido 0 veces \n" )
      print("5." + tarjetas_video[10][1] + " el cual ha sido vendido 0 veces \n" )
     
      lista = []
#Realizamos la iteraci+on para obtner la lista de categoría
      for producto in lifestore_products:
        if producto[3] == "tarjetas madre":
          tarjetas_madre.append([producto[0],producto[1]])
#Realizamos la iteración para conocer los productos que si hayan sido buscados para esta categoría. 
      for tarjeta in tarjetas_madre:
        for venta in lifestore_sales:
          if tarjeta[0] == venta[1]:
            contador +=1
        if contador !=0:
          lista.append([tarjeta[0],tarjeta[1],contador])
          contador = 0
      lista.sort(key = lambda x: x[2], reverse = False)
      print("\nTarjetas madre \n")
#Imprimimos los resultados      
      print("1." + tarjetas_madre[1][1] + " el cual ha sido vendido 0 veces \n" )
      print("2." + tarjetas_madre[3][1] + " el cual ha sido vendido 0 veces \n" )
      print("3." + tarjetas_madre[5][1] + " el cual ha sido vendido 0 veces \n" )
      print("4." + tarjetas_madre[6][1] + " el cual ha sido vendido 0 veces \n" )
      print("5." + tarjetas_madre[7][1] + " el cual ha sido vendido 0 veces \n" )
     
      lista = []
#Realizamos la iteraci+on para obtner la lista de categoría
      for producto in lifestore_products:
        if producto[3] == "discos duros":
          discos.append([producto[0],producto[1]])
#Realizamos la iteración para conocer los productos que si hayan sido buscados para esta categoría. 
      for disco in discos:
        for venta in lifestore_sales:
          if disco[0] == venta[1]:
            contador +=1
        if contador !=0:
          lista.append([disco[0],disco[1],contador])
          contador = 0
      lista.sort(key = lambda x: x[2], reverse = False)
      print("\nDiscos duros\n")
#Imprimimos los resultados      
      print("1." + discos[6][1] + " el cual ha sido vendido 0 veces \n" )
      print("2." + discos[8][1] + " el cual ha sido vendido 0 veces \n" )
      print("3." + discos[9][1] + " el cual ha sido vendido 0 veces \n" )
      for i in range(0,2):
        print (str(i+4) +  ". " + lista[i][1] + "  el cual ha sido vendido " + str(lista[i][2]) + " veces\n")
      lista = []
#Realizamos la iteraci+on para obtner la lista de categoría
      for producto in lifestore_products:
        if producto[3] == "memorias usb":
          memorias.append([producto[0],producto[1]])
#Realizamos la iteración para conocer los productos que si hayan sido buscados para esta categoría. 
      for memoria in memorias:
        for venta in lifestore_sales:
          if memoria[0] == venta[1]:
            contador +=1
        if contador !=0:
          lista.append([memoria[0],memoria[1],contador])
          contador = 0
      print("\nMemorias usb\n")
#Imprimimos los resultados      
      print("1. " + memorias[1][1] + " el cual ha sido vendido 0 veces \n" )
      for i in range(0,1):
        print (str(i+2) +  ". " + lista[i][1] + "  el cual ha sido vendido " + str(lista[i][2]) + " veces\n")
      lista = []
#Realizamos la iteraci+on para obtner la lista de categoría
      for producto in lifestore_products:
        if producto[3] == "pantallas":
          pantallas.append([producto[0],producto[1]])
#Realizamos la iteración para conocer los productos que si hayan sido buscados para esta categoría. 
      for pantalla in pantallas:
        for venta in lifestore_sales:
          if pantalla[0] == venta[1]:
            contador +=1
        if contador !=0:
          lista.append([pantalla[0],pantalla[1],contador])
          contador = 0
      #lista.sort(key = lambda x: x[2], reverse = False)
      print("\nPantallas\n")
#Imprimimos los resultados     
      print("1." + pantallas[1][1] + " el cual ha sido vendido 0 veces \n" )
      print("2." + pantallas[2][1] + " el cual ha sido vendido 0 veces \n" )
      print("3." + pantallas[3][1] + " el cual ha sido vendido 0 veces \n" )
      print("4." + pantallas[6][1] + " el cual ha sido vendido 0 veces \n" )
      print("5." + pantallas[7][1] + " el cual ha sido vendido 0 veces \n" )
      
      lista = []
#Realizamos la iteraci+on para obtner la lista de categoría
      for producto in lifestore_products:
        if producto[3] == "bocinas":
          bocinas.append([producto[0],producto[1]])
#Realizamos la iteración para conocer los productos que si hayan sido buscados para esta categoría. 
      for bocina in bocinas:
        for venta in lifestore_sales:
          if bocina[0] == venta[1]:
            contador +=1
        if contador !=0:
          lista.append([bocina[0],bocina[1],contador])
          contador = 0
      lista.sort(key = lambda x: x[2], reverse = False)
#Imprimimos los resultados
      print("\nBocinas\n")
      print("1." + lista[0][1] + " el cual ha sido vendido "+ str(lista[0][2]) + " veces\n")

      lista = []
#Realizamos la iteraci+on para obtner la lista de categoría
      for producto in lifestore_products:
        if producto[3] == "audifonos":
          audifonos.append([producto[0],producto[1]])
#Realizamos la iteración para conocer los productos que si hayan sido buscados para esta categoría.       
      for audifono in audifonos:
        for venta in lifestore_sales:
          if audifono[0] == venta[1]:
            contador +=1
        if contador !=0:
          lista.append([audifono[0],audifono[1],contador])
          contador = 0
      lista.sort(key = lambda x: x[2], reverse = False)
#Imprimimos los resultados      
      print("\nAudífonos\n")
      print("1." + audifonos[2][1] + " el cual ha sido vendido 0 veces \n" )
      print("2." + audifonos[3][1] + " el cual ha sido vendido 0 veces \n" )
      print("3." + audifonos[4][1] + " el cual ha sido vendido 0 veces \n" )
      print("4." + audifonos[6][1] + " el cual ha sido vendido 0 veces \n" )
      print("5." + audifonos[7][1] + " el cual ha sido vendido 0 veces \n" )
      lista = []
      
    if opc == "d":
      contador = 0
#Realizamos la iteraci+on para obtner la lista de categoría      
      for producto in lifestore_products:
        if producto[3] == "procesadores":
          procesadores.append([producto[0],producto[1]])
#Realizamos la iteración para conocer los productos que si hayan sido buscados para esta categoría.       
      for procesador in procesadores:
        for search in lifestore_searches:
          if procesador[0] == search[1]:
            contador +=1
        if contador !=0:
          lista.append([procesador[0],procesador[1],contador])
          contador = 0
      lista.sort(key = lambda x: x[2], reverse = False)
     
      print("Procesadores \n")
      for i in range(0,5):
        print (str(i+1) +  ". " + lista[i][1] + "  el cual ha sido buscado " + str(lista[i][2]) + " veces\n")
      
      lista = []
#Realizamos la iteraci+on para obtner la lista de categoría
      for producto in lifestore_products:
        if producto[3] == "tarjetas de video":
          tarjetas_video.append([producto[0],producto[1]])
#Realizamos la iteración para conocer los productos que si hayan sido buscados para esta categoría. 
      for tarjeta in tarjetas_video:
        for search in lifestore_searches:
          if tarjeta[0] == search[1]:
            contador +=1
        if contador !=0:
          lista.append([tarjeta[0],tarjeta[1],contador])
          contador = 0
      lista.sort(key = lambda x: x[2], reverse = False)
      
      print("\nTarjetas de video \n")
#Imprimimos los resultados      
      print("1." + tarjetas_video[4][1] + " el cual ha sido buscado 0 veces \n" )
      print("2." + tarjetas_video[6][1] + " el cual ha sido buscado 0 veces \n" )
      print("3." + tarjetas_video[9][1] + " el cual ha sido buscado 0 veces \n" )
      print("4." + tarjetas_video[10][1] + " el cual ha sido buscado 0 veces \n" )
      print("5." + tarjetas_video[13][1] + " el cual ha sido buscado 0 veces \n" )
     
      lista = []
#Realizamos la iteraci+on para obtner la lista de categoría
      for producto in lifestore_products:
        if producto[3] == "tarjetas madre":
          tarjetas_madre.append([producto[0],producto[1]])
#Realizamos la iteración para conocer los productos que si hayan sido buscados para esta categoría. 
      for tarjeta in tarjetas_madre:
        for search in lifestore_searches:
          if tarjeta[0] == search[1]:
            contador +=1
        if contador !=0:
          lista.append([tarjeta[0],tarjeta[1],contador])
          contador = 0
      lista.sort(key = lambda x: x[2], reverse = False)
      
      print("\nTarjetas madre \n")
#Imprimimos los resultados      
      print("1." + tarjetas_madre[1][1] + " el cual ha sido buscado 0 veces \n" )
      print("2." + tarjetas_madre[3][1] + " el cual ha sido buscado 0 veces \n" )
      print("3." + tarjetas_madre[4][1] + " el cual ha sido buscado 0 veces \n" )
      print("4." + tarjetas_madre[5][1] + " el cual ha sido buscado 0 veces \n" )
      print("5." + tarjetas_madre[7][1] + " el cual ha sido buscado 0 veces \n" )
     
      lista = []
#Realizamos la iteraci+on para obtner la lista de categoría
      for producto in lifestore_products:
        if producto[3] == "discos duros":
          discos.append([producto[0],producto[1]])
#Realizamos la iteración para conocer los productos que si hayan sido buscados para esta categoría. 
      for disco in discos:
        for search in lifestore_searches:
          if disco[0] == search[1]:
            contador +=1
        if contador !=0:
          lista.append([disco[0],disco[1],contador])
          contador = 0
      lista.sort(key = lambda x: x[2], reverse = False)
     
      print("\nDiscos duros\n")
#Imprimimos los resultados      
      print("1." + discos[6][1] + " el cual ha sido buscado 0 veces \n" )
      print("2." + discos[8][1] + " el cual ha sido buscado 0 veces \n" )
      print("3." + discos[11][1] + " el cual ha sido buscado 0 veces \n" )
      for i in range(0,2):
        print (str(i+4) +  ". " + lista[i][1] + "  el cual ha sido buscado " + str(lista[i][2]) + " veces\n")
      lista = []
#Realizamos la iteraci+on para obtner la lista de categoría
      for producto in lifestore_products:
        if producto[3] == "memorias usb":
          memorias.append([producto[0],producto[1]])
#Realizamos la iteración para conocer los productos que si hayan sido buscados para esta categoría. 
      for memoria in memorias:
        for search in lifestore_searches:
          if memoria[0] == search[1]:
            contador +=1
        if contador !=0:
          lista.append([memoria[0],memoria[1],contador])
          contador = 0
#Imprimimos los resultados      
      print("\nMemorias usb\n")
      print("1." + memorias[0][1] + " el cual ha sido buscado 0 veces \n" )
      print("2." + memorias[1][1] + " el cual ha sido buscado 0 veces \n" )
      lista = []
#Realizamos la iteraci+on para obtner la lista de categoría
      for producto in lifestore_products:
        if producto[3] == "pantallas":
          pantallas.append([producto[0],producto[1]])
#Realizamos la iteración para conocer los productos que si hayan sido buscados para esta categoría. 
      for pantalla in pantallas:
        for search in lifestore_searches:
          if pantalla[0] == search[1]:
            contador +=1
        if contador !=0:
          lista.append([pantalla[0],pantalla[1],contador])
          contador = 0
      lista.sort(key = lambda x: x[2], reverse = False)
      
      print("\nPantallas\n")
#Imprimimos los resultados     
      print("1." + pantallas[0][1] + " el cual ha sido buscado 0 veces \n" )
      print("2." + pantallas[2][1] + " el cual ha sido buscado 0 veces \n" )
      print("3." + pantallas[3][1] + " el cual ha sido buscado 0 veces \n" )
      print("4." + pantallas[6][1] + " el cual ha sido buscado 0 veces \n" )
      print("5." + pantallas[7][1] + " el cual ha sido buscado 0 veces \n" )
      
      lista = []
#Realizamos la iteraci+on para obtner la lista de categoría
      for producto in lifestore_products:
        if producto[3] == "bocinas":
          bocinas.append([producto[0],producto[1]])
#Realizamos la iteración para conocer los productos que si hayan sido buscados para esta categoría. 
      for bocina in bocinas:
        for search in lifestore_searches:
          if bocina[0] == search[1]:
            contador +=1
        if contador !=0:
          lista.append([bocina[0],bocina[1],contador])
          contador = 0
      lista.sort(key = lambda x: x[2], reverse = False)
#Imprimimos los resultados     
      print("\nBocinas\n")
      print("1." + bocinas[1][1] + " el cual ha sido buscado 0 veces \n" )
      print("2." + bocinas[3][1] + " el cual ha sido buscado 0 veces \n" )
      print("3." + bocinas[4][1] + " el cual ha sido buscado 0 veces \n" )
      print("4." + bocinas[5][1] + " el cual ha sido buscado 0 veces \n" )
      print("5." + bocinas[7][1] + " el cual ha sido buscado 0 veces \n" )

      lista = []
#Realizamos la iteraci+on para obtner la lista de categoría
      for producto in lifestore_products:
        if producto[3] == "audifonos":
          audifonos.append([producto[0],producto[1]])
#Realizamos la iteración para conocer los productos que si hayan sido buscados para esta categoría.       
      for audifono in audifonos:
        for search in lifestore_searches:
          if audifono[0] == search[1]:
            contador +=1
        if contador !=0:
          lista.append([audifono[0],audifono[1],contador])
          contador = 0
      lista.sort(key = lambda x: x[2], reverse = False)
#Imprimimos los resultados     
      print("\nAudífonos\n")
      print("1." + audifonos[0][1] + " el cual ha sido buscado 0 veces \n" )
      print("2." + audifonos[2][1] + " el cual ha sido buscado 0 veces \n" )
      print("3." + audifonos[3][1] + " el cual ha sido buscado 0 veces \n" )
      print("4." + audifonos[4][1] + " el cual ha sido buscado 0 veces \n" )
      print("5." + audifonos[5][1] + " el cual ha sido buscado 0 veces \n" )
      lista = []

      opc = 0 
     
#Si la opción seleccionada es la b, desplegamos un nuevo submenú
  if opc == "b":
    print("\nBienvenido al análisis de reseñas de productos.")
    print("Elige una de las siguientes opciones: ")
    print ("\na) Productos con mejores reseñas.")
    print ("b) Productos con peores reseñas no devueltos.")
    print ("c) Productos con peores reseñas y devueltos")
    opc = input("\nOpción elegida: ")
#Si la opción elegida es la a, realizamos primero una iteración para conoces los productos que tienen el mayor número de reseñas-     
    if opc == "a":
      print ("\nEl top de productos con las mejores reseñas es: \n")
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1]:
            lista.append([producto[0],venta[2]])
            lista2.append(producto[0])
            counts = [[ID, lista2.count(ID)] for ID in set(lista2)]
      
#Iteramos para conocer la calificación total de cada producto reseñado.      
      for elemento in lista:
        if elemento[0] == prev:
            curr_sum += elemento[1]
            prev = elemento [0]
        if elemento[0] != prev:
          sums.append([elemento[0],curr_sum])
          curr_sum = 0
          curr_sum += elemento[1]
          prev = elemento[0]

#Creamos una lista de las reseñas para cada producto, y una lista para las etiquetas de cada producto        
      for suma in sums:
        lista3.append(suma[0])
        lista4.append(suma[1])
#Añadimos la calificación acumulada del producto 1        
      del lista4 [0]
      lista4.append(4)
      
#Iteramos para obtener una lista que combine las dos listas definidas previamente
      for i in range(0,len(sums)):
        lista5.append([lista3[i],lista4[i]])
#Iteramos para conocer el promedio de cada producto, y añadirlo a una nueva lista      
      for i in range(0,len(lista5)):
        x = int(counts[i][1])
        
        y = float(lista5[i][1] / x)
        
        lista6.append([lista5[i][0],y])
#Iteramos para tener en una nueva lista el nombre del producto y el promedio de calificación      
      for producto in lifestore_products:
        for elemento in lista6: 
          if producto[0] == elemento[0]:
            lista7.append([producto[1],elemento[1]])
#Ordenamos la lista de mayor a menor
      lista7.sort(key = lambda x: x[1], reverse = True)  
#Imprimimos los resultados      
      for i in range(0,20):
        print (str(i+1) +  ". " + lista7[i][0] + "  el cual tiene una calificación promedio de " + str(lista7[i][1]) + " estrellas\n")
#Si la opción elegida es la b, iteramos para conocer la cantidad de productos vendidos para productos no devueltos
    if opc == "b":
      print ("\nEl top de productos no devueltos con peores reseñas es: \n")
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1] and venta[4] == 0:
            lista.append([producto[0],venta[2]])
            lista2.append(producto[0])
            counts = [[ID, lista2.count(ID)] for ID in set(lista2)]
      
#Iteramos para obtener las calificaciones acumuladas por producto      
      for elemento in lista:
        if elemento[0] == prev:
            curr_sum += elemento[1]
            prev = elemento [0]
        if elemento[0] != prev:
          sums.append([elemento[0],curr_sum])
          curr_sum = 0
          curr_sum += elemento[1]
          prev = elemento[0]

#iteramos para tener una lista con las calificaciones acumuladas y los ID de productos  
      for suma in sums:
        lista3.append(suma[0])
        lista4.append(suma[1])
#Eliminamos elementos que estorban en la lista        
      del lista4 [0]
      lista4.append(4)
#Combinamos las listas anteriores en una sola      
      for i in range(0,len(sums)):
        lista5.append([lista3[i],lista4[i]])
#Obtenemos los promedios      
      for i in range(0,len(lista5)):
        x = int(counts[i][1])
        
        y = float(lista5[i][1] / x)
        
        lista6.append([lista5[i][0],y])
#Creamos una lista con los nombres y los promedios      
      for producto in lifestore_products:
        for elemento in lista6: 
          if producto[0] == elemento[0]:
            lista7.append([producto[1],elemento[1]])
#Ordenamos la lista de menor a mayor
      lista7.sort(key = lambda x: x[1], reverse = False)
#Imprimimos los resultados
      for i in range(0,20):
        print (str(i+1) +  ". " + lista7[i][0] + "  el cual tiene una calificación promedio de " + str(lista7[i][1]) + " estrellas\n")
    
#Si la opción del submenu es c
    if opc == "c":
      print("\nÚnicamente se han registrado 7 devoluciones de productos, a continuación se presentan las reseñas que estos productos tuvieron en la devolución.\n")
      print ("El top de productos devueltos con peores reseñas es: \n")
#Creamos una lista con los productos vendidos y devueltos      
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1] and venta[4] == 1:
            lista.append([producto[0],venta[2]])
            lista2.append(producto[0])
            counts = [[ID, lista2.count(ID)] for ID in set(lista2)]
#Creamos una lista para conocer las calificaciones acumuladas de estos productos       
      for elemento in lista:
        if elemento[0] == prev:
            curr_sum += elemento[1]
            prev = elemento [0]
        if elemento[0] != prev:
          sums.append([elemento[0],curr_sum])
          curr_sum = 0
          curr_sum += elemento[1]
          prev = elemento[0]
#Creamos las listas de Id y acumulados
      for suma in sums:
        lista3.append(suma[0])
        lista4.append(suma[1])
#Eliminamos elementos extras        
      del lista4 [0]
      lista4.append(4)
#Combinamos las listas en una sola
      for i in range(0,len(sums)):
        lista5.append([lista3[i],lista4[i]])
#Obtenemos el promedio      
      for i in range(0,len(lista5)):
        x = int(counts[i][1])
        
        y = float(lista5[i][1] / x)
        
        lista6.append([lista5[i][0],y])
#ponemos en una lista el nombre y el promedio      
      for producto in lifestore_products:
        for elemento in lista6: 
          if producto[0] == elemento[0]:
            lista7.append([producto[1],elemento[1]])
#Ordenamos de menor a mayor
      lista7.sort(key = lambda x: x[1], reverse = False)
#Imprimimos los resultados      
      for i in range(0,len(lista7)):
        print (str(i+1) +  ". " + lista7[i][0] + "  el cual tiene una calificación promedio de " + str(lista7[i][1]) + " estrellas\n")
#Establecemos la opción como 0 para evitar que el programa siga corriendo    
      opc == 0

#Si la opción elegida es c, desplegamos un nuevo submenú
  if opc == "c":
    print("\nBienvenido al análisis de ventas.")
    print("Elige una de las siguientes opciones: ")
    print ("\na) Total de ingresos.")
    print ("b) Ventas promedio mensuales.")
    print ("c) Total anual.")
    print ("d) Meses con más ventas al año.")
    opc = input("\nOpción elegida: ")
#Iteramos para conocer el número de ventas, y colocamos en la lista el precio del producto, así como el número de unidades vendidas de cada uno    
    if opc == "a":    
      contador = 0
      print ("\nEl total de ingresos es: \n")
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1]:
            contador +=1
        if contador !=0:
          lista.append([producto[0],producto[1],contador,producto[2]])
          contador = 0
#Iteramos para conocer cuanto dinero representó la venta de los productos y lo añadimos a una lista 
      for elemento in lista: 
        x = int(elemento[2]) 
        y = int(elemento[3])
        dinero = x*y
        lista2.append([elemento[0],elemento[1],dinero])
#Sumamos todos los ingresos      
      for elemento in lista2:
        suma += elemento[2]
#Convertimos la sumatoria en un string        
      suma = str(suma)
#Imprimimos los resultados       
      print("El total de ingresos para las ventas registradas hasta el momento es de: $" + suma[0:3] + "," + suma[3:6])
#Si la opción es b
    if opc == "b":    
      contador = 0
#Iteramos para conocer los productos que se han vendido, así como el número de estos vendidos y el precio de cada uno      
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1] and venta[3][-4:-1] == "202":
            contador +=1
        if contador !=0:
          lista.append([producto[0],contador,producto[2]])
          contador = 0
#Iteramos para conocer el dinero que representó cada producto        
      for elemento in lista: 
         x = int(elemento[1]) 
         y = int(elemento[2])
         dinero = x*y
         lista2.append([elemento[0],dinero])
#Obtenemos los ingresos totales      
      for elemento in lista2:
        suma += elemento[1]
#Obtenemos el promedio de cada mes        
      promedio = suma/12
#Imprimimos el resultado      
      print("Las ventas promedio para cada mes del 2020 son: $" + str(promedio))

#Si la opción es c    
    if opc == "c":    
      contador = 0
      print ("\nLas ventas anuales: \n")
#Iteramos para conocer las ventas del año 2020 únicamente      
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1] and venta[3][-4:-1] == "202":
            contador +=1
        if contador !=0:
          lista.append([producto[0],producto[1],contador,producto[2]])
          contador = 0
#Iteramos para conocer los ingresos totales de cada producto 
      for elemento in lista: 
        x = int(elemento[2]) 
        y = int(elemento[3])
        dinero = x*y
        lista2.append([elemento[0],elemento[1],dinero])
#Sumamos los resultados anteriores      
      for elemento in lista2:
        suma += elemento[2]

      suma = str(suma)
#Imprimimos el resultado      
      print("El total de ingresos para las ventas del 2020 es: $" + suma[0:3] + "," + suma[3:6])
#Si la opción es d    
    if opc == "d":  
#Definimos variables de apoyo para el programa, tales como las listas de cada mes, listas auxiliares y la sumatoria de cada mes        
      contador = 0
      print ("\nLos meses con más ventas son: \n")
      enero=[]
      enero2=[]
      suma_ene=0
      feb=[]
      feb2=[]
      suma_feb=0
      mar=[]
      mar2=[]
      suma_mar=0
      abr=[]
      abr2=[]
      suma_abr=0
      may=[]
      may2=[]
      suma_may=0
      jun=[]
      jun2=[]
      suma_jun=0
      jul=[]
      jul2=[]
      suma_jul=0
      ago=[]
      ago2=[]
      suma_ago=0
      sep=[]
      sep2=[]
      suma_sep=0
      oct_=[]
      oct_2=[]
      suma_oct=0
      nov=[]
      nov2=[]
      suma_nov=0
      dic=[]
      dic2=[]
      suma_dic=0
      meses_ventas = []
#Iteramos para el mes de enero, conociendo las ventas de cada producto
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1] and venta[3][3:5] == "01":
            contador +=1
        if contador !=0:
          enero.append([producto[0],producto[1],contador,producto[2]])
          contador = 0
#Conocemos el dinero de cada producto en el mes    
      for elemento in enero: 
        x = int(elemento[2]) 
        y = int(elemento[3])
        dinero = x*y
        enero2.append([elemento[0],elemento[1],dinero])
      for elemento in enero2:
        suma_ene += elemento[2]
#Creamos la lista que contiene las ventas totales del mes
      meses_ventas.append(["enero",suma_ene])
      suma_ene = str(suma_ene)
#Iteramos para conocer los productos vendidos
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1] and venta[3][3:5] == "02":
            contador +=1
        if contador !=0:
          feb.append([producto[0],producto[1],contador,producto[2]])
          contador = 0
#Conocemos el dinero de cada producto en el mes      
      for elemento in feb: 
        x = int(elemento[2]) 
        y = int(elemento[3])
        dinero = x*y
        feb2.append([elemento[0],elemento[1],dinero])
      for elemento in feb2:
        suma_feb += elemento[2]
      #Creamos la lista que contiene las ventas totales del mes
      meses_ventas.append(["febrero",suma_feb])
      suma_feb = str(suma_feb)
 #Iteramos para conocer los productos vendidos     
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1] and venta[3][3:5] == "03":
            contador +=1
        if contador !=0:
          mar.append([producto[0],producto[1],contador,producto[2]])
          contador = 0
#Conocemos el dinero de cada producto en el mes      
      for elemento in mar: 
        x = int(elemento[2]) 
        y = int(elemento[3])
        dinero = x*y
        mar2.append([elemento[0],elemento[1],dinero])
      for elemento in mar2:
        suma_mar += elemento[2]
     #Creamos la lista que contiene las ventas totales del mes
      meses_ventas.append(["marzo",suma_mar])
      suma_mar = str(suma_mar)
 #Iteramos para conocer los productos vendidos     
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1] and venta[3][3:5] == "04":
            contador +=1
        if contador !=0:
          abr.append([producto[0],producto[1],contador,producto[2]])
          contador = 0
  #Conocemos el dinero de cada producto en el mes    
      for elemento in abr: 
        x = int(elemento[2]) 
        y = int(elemento[3])
        dinero = x*y
        abr2.append([elemento[0],elemento[1],dinero])
      for elemento in abr2:
        suma_abr += elemento[2]
     #Creamos la lista que contiene las ventas totales del mes
      meses_ventas.append(["abril",suma_abr])
      suma_abr = str(suma_abr)
  #Iteramos para conocer los productos vendidos    
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1] and venta[3][3:5] == "05":
            contador +=1
        if contador !=0:
          may.append([producto[0],producto[1],contador,producto[2]])
          contador = 0
   #Conocemos el dinero de cada producto en el mes   
      for elemento in may: 
        x = int(elemento[2]) 
        y = int(elemento[3])
        dinero = x*y
        may2.append([elemento[0],elemento[1],dinero])
      for elemento in may2:
        suma_may += elemento[2]
    #Creamos la lista que contiene las ventas totales del mes
      meses_ventas.append(["mayo",suma_may])
      suma_may = str(suma_may)
 #Iteramos para conocer los productos vendidos     
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1] and venta[3][3:5] == "06":
            contador +=1
        if contador !=0:
          jun.append([producto[0],producto[1],contador,producto[2]])
          contador = 0
    #Conocemos el dinero de cada producto en el mes  
      for elemento in jun: 
        x = int(elemento[2]) 
        y = int(elemento[3])
        dinero = x*y
        jun2.append([elemento[0],elemento[1],dinero])
      for elemento in jun2:
        suma_jun += elemento[2]
     #Creamos la lista que contiene las ventas totales del mes
      meses_ventas.append(["junio",suma_jun])
      suma_jun = str(suma_jun)
#Iteramos para conocer los productos vendidos      
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1] and venta[3][3:5] == "07":
            contador +=1
        if contador !=0:
          jul.append([producto[0],producto[1],contador,producto[2]])
          contador = 0
    #Conocemos el dinero de cada producto en el mes  
      for elemento in jul: 
        x = int(elemento[2]) 
        y = int(elemento[3])
        dinero = x*y
        jul2.append([elemento[0],elemento[1],dinero])
      for elemento in jul2:
        suma_jul += elemento[2]
  #Creamos la lista que contiene las ventas totales del mes
      meses_ventas.append(["julio",suma_jul])
      suma_jul = str(suma_jul)
      
#Iteramos para conocer los productos vendidos      
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1] and venta[3][3:5] == "08":
            contador +=1
        if contador !=0:
          ago.append([producto[0],producto[1],contador,producto[2]])
          contador = 0
    #Conocemos el dinero de cada producto en el mes  
      for elemento in ago: 
        x = int(elemento[2]) 
        y = int(elemento[3])
        dinero = x*y
        ago2.append([elemento[0],elemento[1],dinero])
      for elemento in ago2:
        suma_ago += elemento[2]
   #Creamos la lista que contiene las ventas totales del mes
      meses_ventas.append(["agosto",suma_ago])
      suma_ago = str(suma_ago)
      
#Iteramos para conocer los productos vendidos
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1] and venta[3][3:5] == "09":
            contador +=1
        if contador !=0:
          sep.append([producto[0],producto[1],contador,producto[2]])
          contador = 0
   #Conocemos el dinero de cada producto en el mes   
      for elemento in sep: 
        x = int(elemento[2]) 
        y = int(elemento[3])
        dinero = x*y
        sep2.append([elemento[0],elemento[1],dinero])
      for elemento in sep2:
        suma_sep += elemento[2]
  #Creamos la lista que contiene las ventas totales del mes
      meses_ventas.append(["septiembre",suma_sep])
      suma_sep = str(suma_sep)
#Iteramos para conocer los productos vendidos      
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1] and venta[3][3:5] == "10":
            contador +=1
        if contador !=0:
          oct_.append([producto[0],producto[1],contador,producto[2]])
          contador = 0
    #Conocemos el dinero de cada producto en el mes  
      for elemento in oct_: 
        x = int(elemento[2]) 
        y = int(elemento[3])
        dinero = x*y
        oct_2.append([elemento[0],elemento[1],dinero])
      for elemento in oct_2:
        suma_oct += elemento[2]
    #Creamos la lista que contiene las ventas totales del mes
      meses_ventas.append(["octubre",suma_oct])
      suma_oct = str(suma_oct)

#Iteramos para conocer los productos vendidos
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1] and venta[3][3:5] == "11":
            contador +=1
        if contador !=0:
          nov.append([producto[0],producto[1],contador,producto[2]])
          contador = 0
   #Conocemos el dinero de cada producto en el mes   
      for elemento in nov: 
        x = int(elemento[2]) 
        y = int(elemento[3])
        dinero = x*y
        nov2.append([elemento[0],elemento[1],dinero])
      for elemento in nov2:
        suma_nov += elemento[2]
    #Creamos la lista que contiene las ventas totales del mes
      meses_ventas.append(["noviembre",suma_nov])
      suma_nov = str(suma_nov)
    
#Iteramos para conocer los productos vendidos
      for producto in lifestore_products:
        for venta in lifestore_sales:
          if producto[0] == venta[1] and venta[3][3:5] == "12":
            contador +=1
        if contador !=0:
          dic.append([producto[0],producto[1],contador,producto[2]])
          contador = 0
    #Conocemos el dinero de cada producto en el mes  
      for elemento in dic: 
        x = int(elemento[2]) 
        y = int(elemento[3])
        dinero = x*y
        dic2.append([elemento[0],elemento[1],dinero])
      for elemento in dic2:
        suma_dic += elemento[2]
    #Creamos la lista que contiene las ventas totales del mes
      meses_ventas.append(["diciembre",suma_dic])
      suma_dic = str(suma_dic)
    #Ordenamos la lista de mayor a menor  
      meses_ventas.sort(key = lambda x: x[1], reverse = True)
    #Imprimimos los resultados  
      for i in range(0,5):
        print (str(i+1) +  ". " + meses_ventas[i][0] + "  en el cual históricamente se han vendido $" + str(meses_ventas[i][1]))
         
      
