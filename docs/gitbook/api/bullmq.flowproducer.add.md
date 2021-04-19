<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [bullmq](./bullmq.md) &gt; [FlowProducer](./bullmq.flowproducer.md) &gt; [add](./bullmq.flowproducer.add.md)

## FlowProducer.add() method

Adds a flow.

A flow is a tree-like structure of jobs that depend on each other. Whenever the children of a given parent are completed, the parent will be processed, being able to access the children's result data.

All Jobs can be in different queues, either children or parents, however this call would be atomic, either it fails and no jobs will be added to the queues, or it succeeds and all jobs will be added.

<b>Signature:</b>

```typescript
add(flow: FlowJob): Promise<JobNode>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  flow | FlowJob | An object with a tree-like structure where children jobs will be processed before their parents. |

<b>Returns:</b>

Promise&lt;[JobNode](./bullmq.jobnode.md)<!-- -->&gt;
