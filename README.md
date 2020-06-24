# xibo-for-polytech

Base de départ pour une installation de Xibo dans le cadre de Polytech Nancy.
Contient notamment :
* Différents modèles
* Des mises en pages toutes faites
* Un modèle de gestion des utilisateurs (cf. guide d'utilisation)
* La médiathèque associée.

## Importation de la base de données et de la médiathèque :
```sh
cd /opt/xibo/
sudo docker-compose down
sudo mv shared/db shared/db-old
sudo git clone https://github.com/thomasbkd/xibo-for-polytech.git
sudo tar -xzf library.tar.gz
sudo mv library shared/cms/library
sudo tar -xzf import.sql.gz
sudo mv import.sql shared/backup/import.sql
sudo docker-compose up
```
