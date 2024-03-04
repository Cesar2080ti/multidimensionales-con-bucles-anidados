# Definir las ciudades, días de la semana y semanas
ciudades = ['Ciudad A', 'Ciudad B', 'Ciudad C']
dias_semana = ['Lunes', 'Martes', 'Miércoles', 'Jueves', 'Viernes', 'Sábado', 'Domingo']
semanas = ['Semana 1', 'Semana 2', 'Semana 3']

# Crear una matriz 3D para almacenar las temperaturas
temperaturas = [[[0 for _ in range(len(dias_semana))] for _ in range(len(semanas))] for _ in range(len(ciudades))]

# Llenar la matriz con datos de temperaturas (este es solo un ejemplo, puedes ingresar tus propios datos)
temperaturas[0][0] = [25, 26, 24, 23, 27, 28, 25]  # Temperaturas para Ciudad A en la Semana 1
temperaturas[0][1] = [26, 27, 25, 24, 28, 29, 26]  # Temperaturas para Ciudad A en la Semana 2
temperaturas[0][2] = [24, 25, 23, 22, 26, 27, 24]  # Temperaturas para Ciudad A en la Semana 3

temperaturas[1][0] = [28, 29, 27, 26, 30, 31, 28]  # Temperaturas para Ciudad B en la Semana 1
temperaturas[1][1] = [29, 30, 28, 27, 31, 32, 29]  # Temperaturas para Ciudad B en la Semana 2
temperaturas[1][2] = [27, 28, 26, 25, 29, 30, 27]  # Temperaturas para Ciudad B en la Semana 3

temperaturas[2][0] = [22, 23, 21, 20, 24, 25, 22]  # Temperaturas para Ciudad C en la Semana 1
temperaturas[2][1] = [23, 24, 22, 21, 25, 26, 23]  # Temperaturas para Ciudad C en la Semana 2
temperaturas[2][2] = [21, 22, 20, 19, 23, 24, 21]  # Temperaturas para Ciudad C en la Semana 3

# Calcular el promedio de temperaturas para cada ciudad por semana
for i, ciudad in enumerate(ciudades):
    print(f"Promedio de temperaturas para {ciudad}:")
    for j, semana in enumerate(semanas):
        promedio_semana = sum(temperaturas[i][j]) / len(dias_semana)
        print(f"{semana}: {promedio_semana:.2f} °C")
    print()
