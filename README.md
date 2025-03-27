numero = 387
cen_str = dez_str = uni_str = ''
cen_int = dez_int = uni_int = ''
partes_numericas = 0

cen_int, numero = divmod(numero,100)

if cen_int == 1:
  cen_str = '1 centena'
  partes_numericas += 1
elif cen_int > 1:
  cen_str = f'{cen_int} centenas'
  partes_numericas += 1

dez_int, numero = divmod(numero,10)

if dez_int == 1:
  dez_str = '1 dezena'
  partes_numericas += 1
elif dez_int > 1:
  dez_str = f'{dez_int} dezenas'
  partes_numericas += 1

if numero == 1:
  uni_str = '1 unidade'
  partes_numericas += 1
elif numero > 1:
  uni_str = f'{numero} unidades'
  partes_numericas += 1

if partes_numericas == 0:
  print ('Número 0 não possui centenas, dezenas e unidades')
elif partes_numericas == 1:
  print (cen_str + dez_str + uni_str)
elif partes_numericas == 3:
  print (f'{cen_str}, {dez_str} e {uni_str}')
elif partes_numericas == 2:
  if cen_str != ' ':
    segunda_parte = dez_str + uni_str
    print (f'{cen_str} e {segunda_parte}')
  else:
    print (f'{dez_str} e {uni_str}')
