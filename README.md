Python-Webhook
 ------------
 
Um código simples para trazer alguma informação para o discord. 

 ------------
Exemplo:
<div>
<img src="https://i.imgur.com/TDUhtgA.png)" />

 ----------------
 
Codigo:
```python
import requests #dependencia

url = "<your url>" #URL da Webhook.


data = {
    "username" : "Username que queres" #Nome da webhook (Nome do bot)
}


data["embeds"] = [
    {
        "description" : "Texto da embed",
        "title" : "Titulo da embed"
    }
]

result = requests.post(url, json = data)

try:
    result.raise_for_status()
except requests.exceptions.HTTPError as err:
    print(err)
else:
    print("A webhook foi enviada, code {}.".format(result.status_code))

```
