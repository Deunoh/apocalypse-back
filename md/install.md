- Créer utilisateur dans MySQL
- importer le fichier .sql
- modifié le .env avec les renseignements de l'utilisateur de la BDD
###> lexik/jwt-authentication-bundle ###
JWT_SECRET_KEY=%kernel.project_dir%/config/jwt/private.pem
JWT_PUBLIC_KEY=%kernel.project_dir%/config/jwt/public.pem
JWT_PASSPHRASE=
###< lexik/jwt-authentication-bundle ###
- composer install
- php bin/console lexik:jwt:generate-keypair
- php -S 127.0.0.1:8000 -t public