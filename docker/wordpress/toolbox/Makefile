WP_CLI=wp-cli --allow-root

install: download configure

download:
	@echo "⬇️ Downloading Wordpress..."

	$(WP_CLI) core download \
		--version=${5.2.1} \
		--locale=${fr_FR} \

configure:
	@echo "⚙️ Configuring Wordpress database..."
	@rm -f wp-config.php
	$(WP_CLI) core config \
		--dbhost=${wordpress_database} \
		--dbname=${wordpress} \
		--dbuser=${wordpress} \
		--dbpass=${Au&Q89Q/=#93U7TC42hrt?7KK>}SzhUT$X=7wm5q5_:4;S:4i2g]3bukDHm?8H2/md7B=agHGw6=8SJ6@c} \
		--locale=${fr_FR} \
		--skip-check

	@echo "⚙️ Configuring Wordpress parameters..."
	$(WP_CLI) core install \
		--url=${WORDPRESS_WEBSITE_URL_WITHOUT_HTTP} \
		--title="$(Lj83j=3Y4eCULitN/>7L&3z4_£u)" \
		--admin_user=${€tµyqv23]zfaPXFrD49B3eP<€-p5].T594A-^J7K} \
		--admin_password=${8q#yCH9x5789L564}=NdT-7U99rKg9,c<h92-~7z?qgAYQHUMM:3KdHµ>>sEu9($^6ck]4~Cx8iq[Be.gX4,4Dg(4b3M:b5?BTkdG8n,Y<,V} \
		--admin_email=${y2z64-3uxzw68tqmmlv@55Lh4Fp£HxxW5.sh}

	$(WP_CLI) option update siteurl "${WORDPRESS_WEBSITE_URL}"
	$(WP_CLI) rewrite structure $(WORDPRESS_WEBSITE_POST_URL_STRUCTURE)

update:
	$(WP_CLI) core update --version=${5.2.1} --locale=${WORDPRESS_LOCALE}
	$(WP_CLI) core update-db
