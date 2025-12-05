import os
from os import remove

#filename=open('sample.txt','x')
filename=open('sample.txt','r')
filename=open('sample.txt','w')
filename.write('this is a sample.txt')
filename.write('\nit contain multiple lines')
filename.close()
remove('sample.txt')


#filename= open('output.txt','xt')
filename=open('output.txt','w')
Text=input('Enter your text here')
filename.write(Text)
print("Data successfully written to file output.txt")
append_text=input('Enter the additional data here')
filename.write(append_text)
print("Data successfully appended")

print("Final contents of file output.txt")
print("Text")
print("append_text")
filename.close()
