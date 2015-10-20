import os # 
import re # 
import fnmatch

# This is a comment
env = Environment()   # Create an environmnet

#Compiler flags
modo=Import('MODE')
if MODE =='debug':
	#para debug
	env.Append(CCFLAGS=['-O0' ,'-g3', '-Wall' , '-c' , '-fmessage-length=0' ])
else:
	#para release
	env.Append(CCFLAGS=['-O3', '-Wall', '-c', '-fmessage-length=0'])


#Add header search path, needed in case *.h files do not reside
#in default platform location (e.g. /usr/include, /usr/local/include, etc.)
#env.Append(CPPPATH = ['/usr/include/'])

#Add library search path
env.Append(LIBPATH = ['/lib/i386-linux-gnu'])

#Add libraries to link against , in this case. libpthread
env.Append(LIBS = ['pthread'])

#sources
sources= []
def find_files(directory, pattern):
    for root, dirs, files in os.walk(directory):
        for basename in files:
            if fnmatch.fnmatch(basename, pattern):
                filename = os.path.join(root, basename)
                yield filename


for filename in find_files('src', '*.c'):
	print 'Found C source:', filename	
	sources.append(filename)

#sources= []	
#sources += [each for each in os.listdir("./src") if each.endswith('.c')]

print sources

print 'muestro sources_list'
sources_list = env.Object(source = sources)
print sources_list

#Build the program
env.Program(target = "Trunks_Qin_Qout.exe", source = sources)
