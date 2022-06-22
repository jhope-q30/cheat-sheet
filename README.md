# cheat-sheet
dev cheat sheet

## Breakpoints

$tiny-screen: 300px;

$small-screen-min: 463px;

$small-screen: 464px;

$small-screen-max: 607px;

$narrow-screen: 608px;

$narrow-screen-max: 767px;

$weird-screen: 768px;

$weird-screen-max: 895px;

$medium-screen: 896px;

$medium-screen-max: 991px;

$standard-screen: 992px;

$standard-screen-max: 1307px;

$wide-screen: 1308px;

$wide-screen-max: 1407px;

$super-wide-screen: 1408px;



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

## sed

**quick string replace**

sed 's/OLD ADDRESS/NEW ADDRESS/g' DATABASE.sql > UPDATED.sql

sed 's/<img[^>]\+>//g' temp.html > temp1.html

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

**direct access to update wordpress from system**

define('FS_METHOD', 'direct');

**wp cli**

cd public_html
sudo -u www-data wp core download

sudo -u www-data wp core config --dbname='wordpress' --dbuser='wpuser' --dbpass='password' --dbhost='localhost' --dbprefix='wp_'

sudo -u www-data wp core install --url='https://wordpress.localhost.com' --title='Default Wordpress Theme' --admin_user='default' --admin_password='defaultq30' --admin_email='email@domain.com'

## MongoDB

mongo --eval 'db.runCommand({ connectionStatus: 1 })'

## Apache2

List running instances

apache2ctl -S

