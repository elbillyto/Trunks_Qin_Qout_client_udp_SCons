diccionario={'RELEASE':'release', 'DEBUG':'debug'}
MODE = diccionario['RELEASE']
SConscript('SConscript', variant_dir='./release', duplicate=0, exports='MODE')
MODE = diccionario['DEBUG']
SConscript('SConscript', variant_dir='./debug', duplicate=0, exports='MODE')
