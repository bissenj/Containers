# This project creates two containers....1 running mosquitto for mqtt, 1 for node-red as middleware between sensors and database (api).


# Testing MQTT

## On terminal A execute the following commands to start a subscriber client:
docker exec -it mosquitto sh
mosquitto_sub -u mqtt-user -P pw4mqtt-user -d -t home/kitchen/temperature


## On terminal B execute the following commands to start a publisher client:
docker exec -it mosquitto sh
mosquitto_pub -u mqtt-user -P pw4mqtt-user -d -t home/kitchen/temperature -m "21.3"