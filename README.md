# RECONOCIMIENTO_DE_MAKEUP
#Start code here
import time
#declaramos variables para ingresar # your own code
#3ADM # your own code
#Ciencia de Datos e informacion # your own code
#Equipo taylor swift # your own code
#Integrantes: CASTREJON, CORELLA, MARTINEZ # your own code
sep = "-"*25
opcion1 = "s"
Cdigitos = 0
opcion3 = "s"
#mientras la opcion1 sea S se ejecutara el progroma # your own code
print("\tBienvenido al Banco")
while opcion1 == "s":
  #se muestra el menu # your own code
  print("-----¿QUE TIPO DE MOVIMIENTO DESEA HACER ?------")
  print("1) Movimientos en efectivo.")
  print("2) Movimientos con tarjeta.")
  #se pide el movimiento que desea el usuario # your own code
  movi = input("Elija:")
  #se valida el movimiento # your own code
  if movi == "1":
    print(sep)
    print("a)Pago de servicios.")
    print("b)Pago de tarjetas de creditos.")
    print(sep)
    #se pide que elija la opcion de desea # your own code
    opcion2 = str(input("Elija: "))
    #se valida la opcion # your own code
    if opcion2=="a":
      #si elije la a se muestra lo siguiente # your own code
      print("-----¿QUE SERVICIO DESEA PAGAR ?------")
      print("1) Agua.")
      print("2) Luz.")
      print("3) Teléfono.")
      print("4) Otro.")
      print(sep)
      #se pide el servicio # your own code
      ser = str(input("Ingrese el servicio que desea pagar :"))
      #se valida el servicio que se ingreso es verifico # your own code
      if ser == "1" or ser == "2" or ser == "3" or ser == "4" :
        #despues con if y elif se verifica a que numero le toca cada servicio # your own code
        if ser == "1":
          ser = "Agua" # your own code
        elif ser == "2":
          ser = "Luz" # your own code
        elif ser == "3":
          ser = "Teléfono" # your own code
        elif ser =="4":
          ser = "Otro" # your own code
        else:
          print("ERROR , Servicio no existente ")
        print(sep)
        #se piden datos despues de la validacion # your own code
        nconvenio = int(input("Ingrese el número de convenio :"))
        print(sep)
        monto = int(input("Ingrese el monto a pagar: "))
        #se valida el monto  # your own code
        if monto>0:
          #si el monto el valido se pide el efectivo  # your own code
          print(sep)
          efectivo = int(input("Ingrese el efectivo con el que va ha pagar:"))
          #se valida el efectivo # your own code
          if efectivo >= 0:
            #si es valida se ejecuta lo siguiente # your own code
            print("cargando...")
            #se usa for para imprimir los puntos y el tiempo en el que se van a mostrar # your own code
            for i in range(3):
              print("...")
              time.sleep(1)
            #se ejecuta la operacion del cambio # your own code
            cambio = efectivo - monto
            #se pregunta si desea el comprobante # your own code
            print("¿Desea imprimir comprobante?")
            print(sep)
            print("S) si.")
            print("N) no.")
            compro = str(input("Elija:"))
            #se valida si desea el comprobante # your own code
            if compro == "s":
              #si es afirmativa # your own code
              print("cargando...")
              #el ciclo FOR ayuda a la libreria time para ejecutar tiempos  # your own code
              for i in range(3):
                print("...")
                time.sleep(1)
              #Datos de salida que es el ticket o comprobante # your own code
              print("\n          COMPROBANTE")
              print("\t",sep)
              print("\t Servicio---------------------",ser)
              print("\t El numero de convenio es-----",nconvenio)
              print("\t El total pagado es-----------",monto)
              print("\t El efectivo ingresado es-----",efectivo)
              print("\t El cambio es de--------------",cambio)
              print("\t",sep)
            elif compro == "n":
              #si no quiere comprobante # your own code
              print("")
              print("Desea realizar otra movimiento")
              print("\tS) si.")
              print("\tN) no.")
              opcion3 = input("Elija: ")
            #si el efectivo es uno erroneo # your own code
            else:
              #si es invalido el dato se muestra el siguiente mensaje # your own code
              print("Efectivo ingresado menor al monto que se desea pagar o invalido")
              print("Desea realizar algún movimiento")
              print("\tS) si.")
              print("\tN) no.")
              opcion3 = input("Elija: ")
        #datos de salida si el monto es uno incorrecto # your own code
        else:
          print("Monto ingresado invalido.")
      #datos de salida si el servicio es uno incorrecto # your own code
      else:
        print("Servicio invalido")
      print(sep)
      #se pregunta al usuario si desea realizar otro movimiento # your own code
      print("Desea realizar otra movimiento")
      print("\tS) si.")
      print("\tN) no.")
      opcion3 = input("Elija: ")
      #si es afirmativa se regresa al menu principal y se es negativa se muetra un mensaje de despedida # your own code
    #si la opcion es la b # your own code
    elif opcion2 == 'b':
      #si la opcion es la b se ejecuta la siguiente accion que es el PAGO DE TARJETA DE CRÈDITO # your own code
      print(sep)
      print("Pago de tarjeta de crédito")
      #se piden datos de entrada # your own code
      ntarjeta = input("Ingresa el número de la tarjeta[8 números enteros]: ")
      #se ejecuta un ciclo for para contar las cifras de el numero de tarjeta # your own code
      #el ciclo FOR contara los caracteres hasta llegar al numeros de caracteres que tienen la variable ntarjeta # your own code
      for i in ntarjeta:
        Cdigitos += 1
      # y se acumulara el conteo en la variable Cdigito # your own code
      #se validad que el numero de caracteres o la variable de conteo tenga 8 # your own code
      # si es verdadero se pedira el monto # your own code
      if Cdigitos == 8:
        monto = int(input("Ingrese el total a pagar: "))
        #se valida el monto si es mayor a 0 # your own code
        #si el monto si es mayor a 0 # your own code
        if monto > 0:
          print("cargando...")
          for i in range(3):
            print("...")
            time.sleep(1)
           #se pedira el efectivo # your own code
          efectivo = float(input("Ingrese el efectivo:"))
          #se valida si el efecto es mayor al monto ingresado # your own code
          if efectivo >= monto:
            #si el efectivo es > al monto se ejecuta la operaciòn y se pregunta si desea imprimir el comprobante # your own code
            cambio = efectivo - monto
            print("S) si.")
            print("N) no.")
            compro = str(input("Desea imprimir comprobante:"))
            #si es afimativo que desea el comprobante se el programa lo mostrara # your own code
            if compro == "s":
              #datos de salida del comprobante # your own code
              print("\t       COMPROBANTE")
              print("\t",sep)
              print("\t número de la tarjeta ",ntarjeta)
              print("\t Monto ",monto)
              print("\t El efectivo ingresado es ",efectivo)
              print("\t El cambio es de  ",cambio)
              print("\t",sep)
            elif compro == "n":
              print("")
              print("Desea realizar otro movimiento")
              print("\tS) si.")
              print("\tN) no.")
              opcion3 = input("Elija: ")
            else:
              print("")
              print("ERROR INVALIDO")
              print("Desea realizar otro movimiento")
              print("\tS) si.")
              print("\tN) no.")
              opcion3 = input("Elija: ")
          else:
            print("Efectivo ingresado menor al monto que se desea pagar o invalido")
        else:
          print("Monto ingresado invalido")
        print("Desea realizar otro movimiento")
        print("\tS) si.")
        print("\tN) no.")
        opcion3 = input("Elija: ")
      else:
        print("La tarjeta es invalida")
      print("Desea realizar otro movimiento")
      print("\tS) si.")
      print("\tN) no.")
      opcion3 = input("Elija: ")
    else:
      print("La opcion es invalida")
      print(sep)
      print("Desea realizar algún movimiento")
      print("\tS) si.")
      print("\tN) no.")
      opcion3 = input("Elija: ")
    opcion1 = opcion3
    opcion3 = "n"
  #movimiento 2  # your own code
  elif movi == "2":
    opcion3 = "s" # your own code
    for i in range(opcion3 == "s"):
      print("\tMovimiento con tarjeta")
      ntarjeta = int(input("Ingresa el número de la tarjeta: "))
      if ntarjeta == 12345678 or ntarjeta == 98765432 or ntarjeta == 10103333  or ntarjeta == 90807060:
        if ntarjeta == 12345678:
          nom = "Areli"
          saldoD = 56000
          nip = 9900
        elif ntarjeta == 98765432:
          nom = "Fernando"
          saldoD = 7000
          nip = 7700
        elif ntarjeta == 10103333:
          nom = "Victor"
          saldoD = 14000
          nip = 9080
        else:
          nom = "Martha"
          saldoD = 1000
          nip = 1010
        nnip = int(input("Ingresa el NIP de la tarjeta: "))
        if nnip == nip:
          print("\tHOLA ",nom)
          print(" ")
          print("\t¿Que tipo de acción desea realizar?")
          print("a) Consultar saldo.")
          print("b) Retiro de efectivo.")
          print("c) Pagos de servicios.")
          opcion4 = input("Elija: ")
          if opcion4 == "a":
            print("")
            print("\tConsultar saldo.")
            print("Hola")
            print(nom, "tu saldo es de ", saldoD)
            print(sep)
            print("Desea imprimir comprobante:")
            print("\tS) si.")
            print("\tN) no.")
            compro = str(input("ingresa tu opcion:"))
            print("")
            if compro == "s":
              print("\t       COMPROBANTE")
              print("\t nombre de la persona ",nom)
              print("\t Saldo Disponible $",saldoD)
            elif compro == "n":
              print("")
              print("Desea realizar otro movimiento")
              print("\tS) si.")
              print("\tN) no.")
              opcion3 = input("Elija: ")
            else:
              print("\tERROR")
              print("Desea realizar otro movimiento")
              print("\tS) si.")
              print("\tN) no.")
              opcion3 = input("Elija: ")
          elif opcion4 == "b":
            print("")
            print("\tRetiro de efectivo.")
            print("")
            print(nom, "su saldo es de ", saldoD)
            retiro = int(input("¿Cuánto desea retirar?"))
            if retiro > saldoD:
              print("Fondos insuficientes.")
              print("")
              print("Desea realizar otro movimiento")
              print("\tS) si.")
              print("\tN) no.")
              opcion3 = input("Elija: ")
            else:
              print("Se esta preparando su efectivo...")
              for i in range(1,4):
                print("...")
                time.sleep(1)
              print("Ya puedes tomar su dinero...")
              for i in range(1,4):
                print("...")
                time.sleep(1)
              print(sep)
              print("S) si.")
              print("N) no.")
              compro = str(input("Desea imprimir comprobante:"))
              if compro == "s":
                saldoN = saldoD - retiro
                print("** COMPROBANTE **")
                print( "Usted a retirado $ ",retiro )
                print("Su saldo nuevo es $ ",saldoN)
              elif compro == "n":
                print("")
                print("Desea realizar otro movimiento")
                print("S) si.")
                print("N) no.")
                print("")
                opcion3 = input("Elija: ")
              else:
                print("\n ERROR")
                print("Desea realizar otro movimiento")
                print("S) si.")
                print("N) no.")
                opcion3 = input("Elija: ")
          elif opcion4 == "c":
            print("\tPago de servicio")
            print("")
            print(nom, "su saldo es de ", saldoD)
            print("\n¿Qué servicio desea pagar?")
            print("1) Agua.")
            print("2) Luz.")
            print("3) Teléfono.")
            print("4) Otro.")
            ser = str(input("Ingrese el servicio que desea pagar :"))
            if ser == "1" or ser == "2" or ser == "3" or ser == "4":
              if ser == "1":
                ser = "Agua" # your own code
              elif ser == "2":
                ser = "Luz" # your own code
              elif ser == "3":
                ser = "Teléfono" # your own code
              else:
                ser = "Otro" # your own code
              print(sep)
              nconvenio = int(input("Ingrese el numero de convenio :"))
              print(sep)
              monto = int(input("Ingrese el monto a pagar: "))
              print(sep)
              print(" s) si.")
              print(" n) no.")
              seguir = input("¿Desea realizar el pago? ")
              if seguir == "S" or seguir == "s":
                if monto <= saldoD:
                  cambio = saldoD - monto
                  print("SERVICIO PAGADO")
                  print("S) si.")
                  print("N) no.")
                  compro = str(input("Desea imprimir comprobante:"))
                  if compro == "S" or compro =="s":
                    print("\t",sep)
                    print("\tCOMPROBANTE")
                    print("\tServicio",ser)
                    print("\tNùmero de convenio",nconvenio)
                    print("\tMonto",monto)
                    print("\tCambio",cambio)
                    print("\t",sep)
                  elif compro == "N" or compro =="n":
                    print("")
                    print("Desea realizar otro movimiento")
                    print("S o s) si.")
                    print("N o n) no.")
                    opcion3 = input("Elija: ")
                  else:
                    print("ERROR")
                    print("Desea realizar otro movimiento")
                    print("S o s) si.")
                    print("N o n) no.")
                    opcion3 = input("Elija: ")
                else:
                  print("FONDOS INSUFICIENTES")
                  print("")
                  print("Desea realizar otro movimiento")
                  print("S o s) si.")
                  print("N o n) no.")
                  opcion3 = input("Elija: ")
              elif seguir =="N" or seguir == "n":
                print("S o s) si.")
                print("N o n) no.")
                print("Desea realizar otro movimiento")
                opcion3 = input("Elija: ")
              else:
                print("ERRRO INVALIDO movimiento")
                print("")
                print("Desea realizar otro movimiento")
                print("S o s) si.")
                print("N o n) no.")
                opcion3 = input("Elija: ")
          else:
            print("ERRRO INVALIDO movimiento")
            print("")
            print("S o s) si.")
            print("N o n) no.")
            print("Desea realizar otro movimiento")
            opcion3 = input("Elija: ")
          print("")
          print("Desea realizar otro movimiento")
          print("S o s) si.")
          print("N o n) no.")
          opcion3 = input("Elija: ")
        else:
          print("")
          print("\tNIP invalido")
          print("")
          print("S o s) si.")
          print("N o n) no.")
          print("Desea realizar otro movimiento")
          opcion3 = input("Elija: ")
      else:
        print("tarjeta invalida")
        print("Desea realizar otro movimiento")
        print("S o s) si.")
        print("N o n) no.")
        opcion3 = input("Elija: ")
      print("")
      opcion1 = opcion3
  else:
    print("La opcion es invalida")
    print("Desea realizar otro movimiento")
    print("S o s) si.")
    print("N o n) no.")
    opcion1 = input("Elija: ")
print("\nGracias por usar nuestro servicio :)")
print("Hasta luego")
print("Programadores: Areli, Fernando , Victor :)")

