{% include templates/install/queue-pub-sub-config.md %}

##### ThingsBoard Configuration

Edit ThingsBoard configuration file

```text
sudo nano /etc/thingsboard/conf/thingsboard.conf
```
{: .copy-code}

Add the following lines to the configuration file. Don't forget to replace “YOUR_PROJECT_ID”, "YOUR_SERVICE_ACCOUNT" with your **real Pub/Sub project id, and service account (it is whole data from json file):**

```bash
export TB_QUEUE_TYPE=pubsub
export TB_QUEUE_PUBSUB_PROJECT_ID=YOUR_PROJECT_ID
export TB_QUEUE_PUBSUB_SERVICE_ACCOUNT=YOUR_SERVICE_ACCOUNT

# These params affect the number of requests per second from each partitions per each queue!!!
export TB_QUEUE_TRANSPORT_REQUEST_POLL_INTERVAL_MS=1000
export TB_QUEUE_TRANSPORT_RESPONSE_POLL_INTERVAL_MS=1000
export TB_QUEUE_CORE_POLL_INTERVAL_MS=1000
export REMOTE_JS_RESPONSE_POLL_INTERVAL_MS=1000
export TB_QUEUE_RULE_ENGINE_POLL_INTERVAL_MS=1000
export TB_QUEUE_RE_MAIN_POLL_INTERVAL_MS=1000
export TB_QUEUE_RE_HP_POLL_INTERVAL_MS=1000
export TB_QUEUE_RE_SQ_POLL_INTERVAL_MS=1000
export TB_QUEUE_TRANSPORT_NOTIFICATIONS_POLL_INTERVAL_MS=1000

# These params affect the number of requests per second from each partitions per each queue.
# Number of requests to particular Message Queue is calculated based on the formula:
# ((Number of Rule Engine and Core Queues) * (Number of partitions per Queue) + (Number of transport queues)
#  + (Number of microservices) + (Number of JS executors)) * 1000 / POLL_INTERVAL_MS
# For example, number of requests based on default parameters is:

# Rule Engine queues:
# Main 10 partitions + HighPriority 10 partitions + SequentialByOriginator 10 partitions = 30
# Core queue 10 partitions
# Transport request Queue + response Queue = 2
# Rule Engine Transport notifications Queue + Core Transport notifications Queue = 2
# Total = 44
# Number of requests per second = 44 * 1000 / 25 = 1760 requests

# Based on the use case, you can compromise latency and decrease number of partitions/requests to the queue, if the message load is low.
# Sample parameters to fit into 10 requests per second on a "monolith" deployment: 

export TB_QUEUE_CORE_POLL_INTERVAL_MS=1000
export TB_QUEUE_CORE_PARTITIONS=2
export TB_QUEUE_RULE_ENGINE_POLL_INTERVAL_MS=1000
export TB_QUEUE_RE_MAIN_POLL_INTERVAL_MS=1000
export TB_QUEUE_RE_MAIN_PARTITIONS=2
export TB_QUEUE_RE_HP_POLL_INTERVAL_MS=1000
export TB_QUEUE_RE_HP_PARTITIONS=1
export TB_QUEUE_RE_SQ_POLL_INTERVAL_MS=1000
export TB_QUEUE_RE_SQ_PARTITIONS=1
export TB_QUEUE_TRANSPORT_REQUEST_POLL_INTERVAL_MS=1000
export TB_QUEUE_TRANSPORT_RESPONSE_POLL_INTERVAL_MS=1000
export TB_QUEUE_TRANSPORT_NOTIFICATIONS_POLL_INTERVAL_MS=1000
```
{: .copy-code}