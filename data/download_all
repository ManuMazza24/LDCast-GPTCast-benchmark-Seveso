import requests

record_id = "XXXXX"
api_url = f"https://zenodo.org/api/records/{record_id}"
data = requests.get(api_url).json()

for file in data["files"]:
    url = file["links"]["self"]
    name = file["key"]
    print("Scarico", name)

    r = requests.get(url, stream=True)
    with open(name, "wb") as f:
        for chunk in r.iter_content(8192):
            f.write(chunk)

print("Tutti i file scaricati.")
