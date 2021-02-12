import os				
import sys				
import requests      
import json			
import time			

web = ('web site')
os.system('clear') 
headers = {'API-Key':'TU KEY ','Content-Type':'application/json'}
data = {"url": web , "visibility": "public"}
response = requests.post('https://urlscan.io/api/v1/scan/',headers=headers, data=json.dumps(data))
print("Respuesta del servidor: ",response) 
print("Raw de urlscan.io: ",response.json()) 
response_json = response.json() 
url = response_json['api'] 
time.sleep(30) 	
response =requests.get(url)
if response.status_code == 200: 
	content = response.content 
	file = open('resultado.json','wb') 
	file.write(content)					
	file.close									
os.system('clear') 
print("Finalizo y archivo creado")
sys.exit()
