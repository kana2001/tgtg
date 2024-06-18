# docker-compose.yml uses variables defined in .env file

## Run the tgtg scanner
    sudo docker compose up -d

## Kill the tgtg scanner log
    sudo docker kill tgtg-scanner-1

## view tgtg scanner log
    sudo docker logs tgtg-scanner-1

## Enter tgtg scanner container shell
    sudo docker exec -it tgtg-scanner-1 /bin/sh

# While in tgtg scanner container

## To create a formatted JSON file containing all your favorite items and their available information.
    python -m tgtg_scanner -f -J >> items.json

# from host machine
## To copy the JSON file to host machine
    docker cp tgtg-scanner-1:items.json ./items.json

