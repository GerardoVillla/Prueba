# Prueba
prueba
Definir minutos Como Real
	definir turno Como Caracter
	definir dia Como Caracter
	escribir "Selecciona el dia de la llamada"
	Escribir "a = Domingo"
	Escribir "b = Lunes a sabado"
	leer dia
	escribir "Selecciona turno"
	escribir "M = matutino"
	escribir "V = vespertino"
	leer turno
	escribir "ingresa minutos utilizados en llamada"
	leer minutos
	si dia == Domingo Entonces
		si minutos >10 Entonces
			llamada = 8.8+ (.5*(minutos-10))
			impuestos = .03 * llamada
		SiNo
			si minutos >8 Entonces
				llamada = 7.4+(.7*(minutos-8))
				impuestos = .03*(llamada)
			SiNo
				si minutos >5 Entonces
					llamada = 5+(.8*(minutos-5))
					impuestos = .03*(llamada)
				SiNo
					llamada = 1*(minutos)
					impuestos = .03 * llamada
					
				FinSi
			FinSi
			
			
		FinSi
	sino
		si turno == matutino Entonces
			si minutos >10 Entonces
				llamada = 8.8+ (.5*(minutos-10))
				impuestos = .15* llamada
			SiNo
				si llamada >8 Entonces
					llamada = 7.4+(.7*(minutos-8))
					impuestos = .15*llamada
				SiNo
					si minutos >5 Entonces
						llamada = 5+(.8*(minutos-5))
						impuestos = .15*llamada
					SiNo
						llamada = 1*(minutos)
						impuestos = .15*llamada
					FinSi
					
					
				FinSi
				
			FinSi
		SiNo
			si  minutos >10 Entonces
				llamada = 8.8+ (.5*(minutos-10))
				impuestos = .1*llamada
			SiNo
				si minutos >8 Entonces
					llamada = 7.4+ (.7*(minutos-8))
					impuestos = .1*llamada
				SiNo
					si minutos >5 Entonces
						llamada = 5+(.8*(minutos-5))
						impuestos = .1*llamada
					SiNo
						llamada = 1*minutos
						impuestos = .1*llamada
						
					FinSi
				FinSi
				
			FinSi
		FinSi
		
	FinSi
	total = llamada + impuestos
	Escribir "Monto a pagar es"," " total
	Escribir "IVA"," " impuestos
	Escribir "Subtotal"," " llamada
