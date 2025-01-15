# Kafka Producer-Consumer Project

This project demonstrates a Kafka-based data pipeline using Python. The pipeline consists of a producer that sends data to a Kafka topic and a consumer that retrieves data from the topic. It can be used for streaming real-time data, such as stock market updates, to downstream applications.

## Project Structure

- **`kafkaproducer.ipynb`**: 
  - Implements a Kafka producer that streams stock data from a CSV file (`indexProcessed.csv`) to a Kafka topic (`demo_test`).
  - The producer sends one random sample from the dataset to the topic every second.
  
- **`kafkaconsumer.ipynb`**:
  - Implements a Kafka consumer that reads data from the same Kafka topic and processes it in real-time.

## Key Features

- Uses `kafka-python` for Kafka interactions.
- Reads stock market data from a CSV file.
- Serializes data to JSON format for Kafka message exchange.
- Demonstrates a simple producer-consumer pattern.

## Prerequisites

- **Kafka Broker**: Ensure that a Kafka broker is running and accessible. Update the broker address in the `bootstrap_servers` parameter.
- **Python Environment**: Python 3.x with the following packages:
  - `kafka-python`
  - `pandas`

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>

2. Install dependencies:
   ```bash
   pip install kafka-python pandas

3. Start yout Kafka broker and create the topic (demo_test):
   ```bash
   kafka-topics --create --topic demo_test --bootstrap-server <broker-address>

