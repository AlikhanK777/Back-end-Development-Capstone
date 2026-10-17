# Back-end-Development-Capstone

Django main application for the Back-End Development Capstone Project. It shows a band website with Songs, Photos and Concerts pages and uses two microservices: Songs (Flask + MongoDB) and Pictures (Flask).

## Run locally

    pip install -r requirements.txt
    python manage.py migrate
    python manage.py runserver

## Deploy

    docker build -t us.icr.io/$SN_ICR_NAMESPACE/djangoapp:1 .
    docker push us.icr.io/$SN_ICR_NAMESPACE/djangoapp:1
    kubectl apply -f deployment.yml
