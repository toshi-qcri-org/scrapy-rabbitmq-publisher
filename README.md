![Upload Python Package](https://github.com/toshi-qcri/scrapy-rabbitmq-publisher/workflows/Upload%20Python%20Package/badge.svg)
## A RabbitMQ Publisher for Scrapy Framework.

Scrapy-RabbitMQ-Publisher allows you to save publish items to RabbitMQ.

## Installation

Using pip, type in your command-line prompt

```
pip install scrapy-rabbitmq-publisher
```

Or clone the repo and inside the `scrapy-rabbitmq-publisher` directory, type

```
python setup.py install
```

## Usage

Add following code to your scrapy settings.

```python
RABBITMQ_HOST = "localhost"
RABBITMQ_PORT = 5672
RABBITMQ_USER = "guest"
RABBITMQ_PASSWORD = "guest"
RABBITMQ_VIRTUAL_HOST = "/"
RABBITMQ_EXCHANGE = "scrapy"
RABBITMQ_ROUTING_KEY = "item"
RABBITMQ_QUEUE = "item"

ITEM_PIPELINES = {
    "scrapy_rabbitmq_publisher.pipelines.RabbitMQItemPublisherPipeline": 1,
}
```
