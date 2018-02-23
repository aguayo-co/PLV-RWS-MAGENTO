# Servicios Prilov

**Crear Usuario**
url: /rest/V1/customers
método: post
body:

    {“customer”: {“email”: "blasruiz@gmail.com",“firstname”: “Blas Emiro Ruiz”},“password”: “Abc@123456”}

response:

    {
    “id”: 2,
    “group_id”: 1,
    “created_at”: “2018-02-13 17:25:47”,
    “updated_at”: “2018-02-13 17:25:47”,
    “created_in”: “Default Store View”,
    “email”: "blasruiz@gmail.com",
    “firstname”: "Blas ",
    “lastname”: " Ruiz ",
    “store_id”: 1,
    “website_id”: 1,
    “addresses”: [],
    “disable_auto_group_change”: 0
    }

fail response:

    {“message”: “A customer with the same email already exists in an associated website.”}

**Loguear Usuario**
url: /rest/V1/integration/customer/token
metodo: post

Body:

    {“username”:“blasruiz@gmail.com”, “password”:“Abc@123456”}

response:

    “fpxye7hegqmanqcl0qev2axury3d45on” 

Token

Fail Response:

    {“message”: “You did not sign in correctly or your account is temporarily disabled.”}

**Pedir contraseña**
url:	/rest/V1/customers/password
metodo:put
Body: 

    {
       "email": "blasruiz@gmail.com",
       "template": "email_reset",
       "websiteId": 1
    }

Response: 

    true

Fail Response:

    {
        "message": "Too many password reset requests. Please wait and try again or contact %1.",
        "parameters": [
            "hello@example.com"
        ]
    }

**Validar Token Contraseña**
url: /rest/V1/customers/{customerId}/password/resetLinkToken/{resetPasswordLinkToken}
metodo: get
Response: 

    true

**Cambiar Contraseña**