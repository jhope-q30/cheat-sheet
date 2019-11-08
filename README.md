# cheat-sheet
dev cheat sheet

## Linux

**Extract archive**

tar -zcvf SOURCE.tar.gz /DEST

**Watchers**

echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p

**Replace spaces**

for file in *; do mv "$file" `echo $file | tr ' ' '_'` ; done

## Mysql

**export**

mysqldump --add-drop-table -u root -p DATABASE > DATABASE.sql

**import**

mysql -u root -p DATABASE < DATABASE.sql

**quick string replace**

sed 's/OLD ADDRESS/NEW ADDRESS/g' DATABASE.sql > UPDATED.sql

## Permissions ( AWS )

sudo usermod -a -G ubuntu www-data

sudo usermod -a -G www-data ubuntu

## git

git remote add origin https://github.com/jhope-q30/0000-test.git

git push -u origin master

git pull --allow-unrelated-histories


## Drupal

admin login - drush uli
update config - drush -y cim

## Wordpress

**remove revisions**

DELETE from wp_posts WHERE post_type = "revision";

## MongoDB

mongo --eval 'db.runCommand({ connectionStatus: 1 })'

