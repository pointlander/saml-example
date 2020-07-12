# SAML Example

## Demo
```bash
go build
```

Then in another terminal:
```bash
./saml-example -server
```

Then in another terminal:
```bash
openssl req -x509 -newkey rsa:2048 -keyout myservice.key -out myservice.cert -days 365 -nodes -subj "/CN=myservice.example.com"
./saml-example -client
```

Then:
```bash
curl localhost:7000/saml/metadata > metadata.xml
curl -T metadata.xml localhost:8000/services/test
```

Now open: localhost:7000/hello  
Username: john  
Password: johnldap  
