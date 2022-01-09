# InfluxDB2-Grafana-Docker
InfluxDB2 + Grafana with docker-compose

## INFO
This setup does not contain SSL configs. If you want to secure communications, please create an nginx proxy or make changes in the configuration. 

## Usage
- Clone repository
- cd /DIR/
- docker-compose up -d
- navigate to Grafana website:
  - http://IP_ADDRESS:3000
  - Use admin:admin to login, than change password
- navigate to InfluxDB website:
  - http://IP_ADDRESS:8086
  - Create admin account and organisation + bucket

## Volumes for permanent storage
| Image     | Host Path                     |  Docker Path              |
| -------   | ---------                     | ------------              |
| Grafana   | ./grafana-config              | /etc/grafana/             |
| Grafana   | ./grafana-data                | /var/lib/grafana          |
| InfluxDB  | ./flux-data                   | /var/lib/influxdb2        |
| InfluxDB  | ./flux-config/flux-config.yml | /etc/influxdb2/config.yml |
