# Example module of RabbitMQ message queues in Magento 2

## Prerequisites
This tutorial assumes RabbitMQ is installed and running on ```localhost``` on the standard port ```(5672)```. In case you use a different host, port or credentials, connections settings would require adjusting.

## Publish message

```
php bin/magento example:rabbit:publish
```
Output will be

```
Message published successfully
```

## Executing consumers queue

Check if the queue is registered by running

```
php bin/magento queue:consumers:list
```
##### Output

```
example.consumer
```
Run consumer ```example.consumer```

```
php bin/magento queue:consumers:start example.consumer
```

### Note:
For a production environment, will configure a cron job for the consumer is always running.