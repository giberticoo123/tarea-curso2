# tarea-curso2
#tarea1
cuenta = float(input("Ingresa el total de tu cuenta: "))
porcentaje = float(input("Ingresa el % de propina (ejemplo 10 o 15): "))

propina = cuenta * (porcentaje / 100)
total_a_pagar = cuenta + propina

print("La propina es:", propina)
print("El total a pagar es:", total_a_pagar)

#tarea2
horas = int(input("ingrese una hora"))
minutos = int(input("ingrese los minutos"))

total_a_segundo = (horas * 3600) + (minutos * 60)
print("total en segundos", total_a_segundo)

#tarea3
num1 = int(input("Ingrese un número "))

if num1 <= 100 and num1 >= 1:
    print("este número esta dentro de lo permitido")
else:
    print("este número no está adentro de lo permitido")

#tarea4
precio = 10

if precio >= 60:
    precio_final = precio * 0.20
else:
    precio_final = precio

#tarea5
letra = input("ingrese una letra ").lower()

if letra == 'a' or letra == 'e' or letra == 'i' or letra == 'o' or letra == 'u':
    print("es una vocal")
else:
    print("es una consonante")

    #tarea6
la1 = float(input("ingrese una medida: "))
la2 = float(input("ingrese otra medida: "))
la3 = float(input("ingrese otra medida: "))

if la1 == la2 and la2 == la3:
    print("Es un triangulo")  # Nota: El texto dice "triangulo", aunque conceptualmente se refiere a un equilátero.

elif la1 != la2 and la2 != la3 and la3 != la1:
    print("Es un escaleno")

else:
    print("Es un isósceles")

#tarea7
saldo = 1000
retiro = int(input("cuanto dinero necesitas: "))

if retiro > 0:
    if retiro <= saldo and retiro % 10 == 0:
        saldo = saldo - retiro
        print("Retiro con exito su saldo actual es:", saldo)
    else:
        print("error el retiro tiene que ser menor o igual a su saldo y multiplo de 10")
else:
    print("error el retiro tiene que ser mayor a cero")

#tarea8
limite = float(input("Por el limite de velocidad "))
velocidad = float(input("pon la velocidad actual "))

exceso = velocidad - limite

if exceso > 0:
    multa = 50 + (exceso * 5)
    print(f"excede el limite por {exceso} Km/h multa: ${multa}")
else:
    print("tu velocidad esta adentro del limite")

#tarea9
año = int(input("Ingrese un año "))

if (año % 4 == 0 and año % 100 != 0) or (año % 400 == 0):
    print(f"El año {año} es bisiesto")
else:
    print(f"El año {año} no es bisiesto")

#tarea10
promedio = float(input("ingrese su promedio "))
ingresos = float(input("ingresa tus ingresos "))
distancia = float(input("ingrese la distancia "))

if promedio > 90 and ingresos < 500:
    print("tienes una beca completa")
elif promedio > 80 and distancia > 50:
    print("tienes la beca de transporte")
else:
    print("no aplicas para la beca")

#tarea11
salario = float(input("¿Cuál es su salario? "))

if salario > 30000:
    descuento = salario * 0.20
    precio_final = salario - descuento
    print(f"Tu total a pagar es: {precio_final} | Descuento: {descuento}")

elif salario > 1000 and salario <= 30000:
    descuento = salario * 0.10
    precio_final = salario - descuento
    print(f"Tu total a pagar es: {precio_final} | Descuento: {descuento}")

else:
    print("No tienes descuento. Total a pagar:", salario)


#tarea12
día = int(input("ingrese un día "))
mes = int(input("ingrese un mes "))
año = int(input("ingrese un año "))

if mes >= 1 and mes <= 12:
    if mes == 2:
        if (año % 4 == 0 and año % 100 != 0) or (año % 400 == 0):
            if día >= 1 and día <= 29:
                print("fecha válida es un año bisiesto")
            else:
                print("fecha inválida febrero en año bisiesto solo tiene hasta 29 días")
        else:
            if día >= 1 and día <= 28:
                print("la fecha es válida")
            else:
                print("fecha inválida febrero en año no bisiesto solo tiene hasta 28 días")
    elif mes == 4 or mes == 6 or mes == 9 or mes == 11:
        if día >= 1 and día <= 30:
            print("fecha válida")
        else:
            print("fecha inválida este mes solo tiene 30 días")
    else:
        if día >= 1 and día <= 31:
            print("la fecha es válida")
        else:
            print("fecha inválida este mes solo tiene 31 días")
else:
    print("fecha inválida el mes debe estar entre 1 y 12")

    #tarea13
jugador1 = input(" jugador1 (piedra, papel o tijera): ")
jugador2 = input(" jugador2 (piedra, papel o tijera): ")

if jugador1 == jugador2:
    print("empate") 

elif jugador1 == "piedra" and jugador2 == "tijera":
    print("jugador1 gana")
elif jugador1 == "papel" and jugador2 == "piedra":
    print("jugador1 gana")
elif jugador1 == "tijera" and jugador2 == "papel":
    print("jugador1 gana")
else:
    print("jugador2 gana")

    #tarea14
    consumo = float(input("ingrese el consumo en kwh: "))
total = 0.0
restante = consumo
if restante > 100:
    total += 100 * 0.50
    restante -= 100

else:
    total += restante * 0.50
    resultado = 0

if restante >0:
    if restante >200:
        total += 200 * 1.00
        restante -=200

    else:
        total += restante * 1.00
        restante = 0

if restante >0: 
    total += restante * 1.50

    print(F"EL TOTAL A PAGAR ES: {total: .2f}")

    #tarea15
    a = float(input("ingrese un número"))
b = float(input("ingrese otro número"))
c = float(input("ingrese otro número"))

if a > b and a > c and b > c:
    print("a b c")

elif a > b and a > c and c > b:
    print("a c b")

elif b > a and b > c and c > a:
    print("b c a")

elif b > a and b > c and a > c:
    print("b a c")

elif c > a and c > b and b > a:
    print("c b a")

else:
    print("c a b")
