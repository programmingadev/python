.PHONY: reset-db format create-admin

reset-db:
	rm -f instance/ecommerce.db
	python3 -c "from app import app, db; app.app_context().push(); db.create_all()"

create-admin:
	python3 -c "from app import app, db, User; app.app_context().push(); db.create_all(); user = User(username='admin', password='123'); db.session.add(user); db.session.commit(); print('Admin user created')"

format:
	black .
