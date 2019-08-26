# Kafka Streams

Some notes taken while reading about Kafka

## What's Kafka Streams

It's an easy data processing and transformation library within Kafka.

- Standard Java Application
- No need to create a separate cluster
- Highly scalable, elastic and fault tolerant, since it's integrated with Kafka capabilities
- Provides exactly once capabilities
- One record at a time (No batching)
- Works for any application size

## Streams Topology

Streams - They are sequences of immutable data records, that fully ordered, can be replayed, 
and is fault tolerant

Stream processor - Is a node in the processor topology. It transforms incoming streams, record
by record, and may create a new stream from it.

Topology - Is a graph of processors chained together by streams.

Source processor - Is a stream processor in the topology which reads directly from a Kafka Topic. 
It has no predecessors and doesn't transform the data.

Sink processor - Is a processor that does not have children. It sends the stream data directly to a Kafka
topic.

