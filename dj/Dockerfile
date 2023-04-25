FROM python:3.10

WORKDIR /stocks_products

COPY stocks_products /stocks_products

RUN pip install -r /stocks_products/requirements.txt

ENV SECRET_KEY django-insecure-nw^y+m^wmxza1asgk+)!ua2qx9)g+#v=6%76-9i8i(6eqiw94j
ENV DEBUG True
ENV ENGINE_DB=django.db.backends.sqlite3
ENV NAME_DB=netology_stocks_products

RUN python manage.py migrate

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "stocks_products.wsgi"]