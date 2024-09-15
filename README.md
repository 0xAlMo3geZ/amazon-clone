# Amazon-Clone

![Screenshot 2023-01-08 at 22 13 46](https://user-images.githubusercontent.com/108229029/211273079-e792667b-a16f-4ea3-a726-4be3fbe133cc.png)
![Screenshot 2023-01-08 at 22 14 08](https://user-images.githubusercontent.com/108229029/211274170-a74fe46b-5fe3-4654-b675-22f9d7579e38.png)
![Screenshot 2023-01-08 at 22 14 24](https://user-images.githubusercontent.com/108229029/211274612-83fe1ccc-12c9-4934-a411-8ba6c5a66eeb.png)
![Screenshot 2023-01-08 at 22 14 51](https://user-images.githubusercontent.com/108229029/211274617-ae2d3138-f116-494f-b625-18f9e27d5bd8.png)
![Screenshot 2023-01-08 at 22 15 42](https://user-images.githubusercontent.com/108229029/211274628-0bd1e5f9-7fbb-41f9-86bf-4860e723a7e4.png)
![Screenshot 2023-01-08 at 22 16 01](https://user-images.githubusercontent.com/108229029/211274638-9d3461a8-617d-4797-868d-c1ed285c57d7.png)
![Screenshot 2023-01-08 at 22 16 41](https://user-images.githubusercontent.com/108229029/211274648-9d55d0a7-ef43-49fb-b332-8b43ed6f0334.png)
![Screenshot 2023-01-08 at 22 16 54](https://user-images.githubusercontent.com/108229029/211274652-1da2b0c5-8033-4f40-95d8-ecbbb7925305.png)
![Screenshot 2023-01-08 at 22 17 13](https://user-images.githubusercontent.com/108229029/211274658-c1a46bde-f438-4467-848b-50bfbd607ca0.png)
![Screenshot 2023-01-08 at 22 17 21](https://user-images.githubusercontent.com/108229029/211274662-665e1c76-a5fa-4e13-9bbc-6de831a712bd.png)
![Screenshot 2023-01-08 at 22 18 07](https://user-images.githubusercontent.com/108229029/211274663-4fe0ebd2-d553-47db-bdca-e8ca5974f7b0.png)
![Screenshot 2023-01-08 at 22 18 36](https://user-images.githubusercontent.com/108229029/211274673-736a05f2-c236-4e02-8840-8eccfaa80658.png)
![Screenshot 2023-01-08 at 22 19 45](https://user-images.githubusercontent.com/108229029/211274684-2f2c1af1-17ca-465f-892a-e5f1f24e2284.png)
![Screenshot 2023-01-08 at 22 20 53](https://user-images.githubusercontent.com/108229029/211274691-cd998330-ed21-4da8-a53f-6cf3dca8c38e.png)

## Installation

1. Download the code by clicking **Code**, **Download ZIP**. Or if you have Git install in your machine, you can run this in your terminal.

```
git clone https://github.com/0xAlMo3geZ/amazon-clone.git
```

2. Change directory to your local copy of `amazon-clone` in your terminal. Then install composer dependencies.

```
composer install
```

3. Install frontend dependencies.

```
npm install
```

4. Copy `.env` file from `.env.example`. In NIX machine you can use this command.

```
cp .env.example .env
```

5. Prepare a database. You can use this command.

```
mysql -uroot -e "CREATE DATABASE amazon-clone_db"
```

If you have password for your database, you need to specify `-p` on the command.

6. Configure your database and email sender settings in `.env`

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=amazon-clone_db
DB_USERNAME=root
DB_PASSWORD=

MAIL_MAILER=smtp
MAIL_HOST=mailpit
MAIL_PORT=1025
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS="amazon-clone@mail.com"
MAIL_FROM_NAME="${APP_NAME}"
```

7. Migrate database tables and seed them with fake data

```
php artisan migrate --seed
```

8. Generate a key for you application

```
php artisan key:generate
```

9. Now go to https://stripe.com/en-gb-us and Create a public and a private KEY.

```
Add your new PRIVATE API KEY to CheckoutController.php and Checkout.vue
```

10. Run php development server

```
php artisan serve
```

11. Run node.js development server (alongside php server)

```
npm run dev
```

Your local copy of amazon-clone is ready to access in your browser ;)
