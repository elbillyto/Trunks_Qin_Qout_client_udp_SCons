diccionario={'RELEASE':'release', 'DEBUG':'debug'}
for clave in diccionario:
    MODE = diccionario[clave]
    SConscript('SConscript', variant_dir='./'+diccionario[clave], duplicate=0, exports='MODE')
#
#diccionario={'RELEASE':'release', 'DEBUG':'debug'}
#MODE = diccionario['RELEASE']
#SConscript('SConscript', variant_dir='./release', duplicate=0, exports='MODE')
#MODE = diccionario['DEBUG']
#SConscript('SConscript', variant_dir='./debug', duplicate=0, exports='MODE')
