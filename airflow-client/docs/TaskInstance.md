

# TaskInstance


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**taskId** | **String** |  |  [optional]
**dagId** | **String** |  |  [optional]
**dagRunId** | **String** | The DagRun ID for this task instance  *New in version 2.3.0*  |  [optional]
**executionDate** | **String** |  |  [optional]
**startDate** | **String** |  |  [optional]
**endDate** | **String** |  |  [optional]
**duration** | **BigDecimal** |  |  [optional]
**state** | **TaskState** |  |  [optional]
**tryNumber** | **Integer** |  |  [optional]
**maxTries** | **Integer** |  |  [optional]
**hostname** | **String** |  |  [optional]
**unixname** | **String** |  |  [optional]
**pool** | **String** |  |  [optional]
**poolSlots** | **Integer** |  |  [optional]
**queue** | **String** |  |  [optional]
**priorityWeight** | **Integer** |  |  [optional]
**operator** | **String** | *Changed in version 2.1.1*&amp;#58; Field becomes nullable.  |  [optional]
**queuedWhen** | **String** |  |  [optional]
**pid** | **Integer** |  |  [optional]
**executorConfig** | **String** |  |  [optional]
**slaMiss** | [**SLAMiss**](SLAMiss.md) |  |  [optional]



