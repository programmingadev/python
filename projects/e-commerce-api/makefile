.PHONY: reset-db format

reset-db:
	rm -f instance/ecommerce.db
	python3 -c "from app import app, db; app.app_context().push(); db.create_all()"

format:
	black .
