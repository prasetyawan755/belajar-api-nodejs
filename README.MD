**Belajar API NodeJS**

Belajar API NodeJS menggunakan ExpressJS

*********
Dokumentasi
*********

{root.api}/{version}/{grouping}/{endpoint}
SAMPLE:
belajar-api.prasetyawan.com/v1/auth/login

=================================================================

Standar Status Response

200 - OK                    --> Call API Success
201 - CREATED               --> Post Success
400 - BAD REQUEST           --> Error on Client Side (Bisa input yang salah dll).
401 - UNAUTHORIZED          --> User not authorized to the request.
403 - FORBIDDEN             --> User not allowed to access.
404 - NOT FOUND             --> Request Endpoint Not Found.
500 - INTERNAL SERVER ERROR --> Error on Server Side
502 - BAD GATEWAY           --> Invalid Response From Antoher Request

=================================================================

GROUP: Authentication

[1] - Register
{root.api}/{version}/auth/register

req:
{
    "name": "Testing",
    "email": "test@mail.com",
    "password": "123456"
}

res:
{
    "message": "Register Success",
    "data": {
        "uid": 1,
        "name": "Testing",
        "email": "test@mail.com"
    }
}

err-response:
201 -> Register Berhasil
400 -> Input yang anda masukkan tidak valid

[2] - Login
{root.api}/{version}/auth/login

req:
{
    "name": "Testing",
    "email": "test@mail.com"
    "password": "123456"
}

GROUP: BLOG

[1] - Create Blog Post
{root.api}/{version}/auth/register

req:
{
    "title": "Title Blog",
    "image": "imagefile.png",
    "body": "Lorem ipsum dolor sit, amet consectetur adipisicing elit."
}

res:
{
    "message": "Create Blog Post Success",
    "data": {
        "post_id": 1,
        "title": "Title BLog",
        "image": "imagefile.png",
        "body": "Lorem ipsum dolor sit, amet consectetur adipisicing elit.",
        "created_at": "21/10/2021",
        "author": {
            "uid": 1,
            "name": "Testing"
        }
    }
}

err-response:
201 -> Blog Post Berhasil Dibuat
400 -> Input yang anda masukkan tidak valid

[2] - Get Blog Post
[3] - Update Blog Post
[4] - Delete Blog Post

*********
Referensi
*********

- [Prawito Hudoro] https://www.youtube.com/channel/UC4k3OBYU4q6MuspHVzZlkew