---
layout: post
title: Spark Release 3.5.4
categories: []
tags: []
status: publish
type: post
published: true
meta:
  _edit_last: '4'
  _wpas_done_all: '1'
---

Spark 3.5.4 is the third maintenance release containing security and correctness fixes. This release is based on the branch-3.5 maintenance branch of Spark. We strongly recommend all 3.5 users to upgrade to this stable release.

### Notable changes

- [[SPARK-47702]](https://issues.apache.org/jira/browse/SPARK-47702): Remove Shuffle service endpoint from the locations list when RDD block is removed form a node
- [[SPARK-48155]](https://issues.apache.org/jira/browse/SPARK-48155): AQEPropagateEmptyRelation for join should check if remain child is just BroadcastQueryStageExec
- [[SPARK-49261]](https://issues.apache.org/jira/browse/SPARK-49261): Don't replace literals in aggregate expressions with group-by expressions
- [[SPARK-49294]](https://issues.apache.org/jira/browse/SPARK-49294): Add width attribute for shuffle-write-time checkbox
- [[SPARK-49501]](https://issues.apache.org/jira/browse/SPARK-49501): Fix double-escaping of table location
- [[SPARK-49595]](https://issues.apache.org/jira/browse/SPARK-49595): Fix `DataFrame.unpivot/melt` in Spark Connect Scala Client
- [[SPARK-49628]](https://issues.apache.org/jira/browse/SPARK-49628): ConstantFolding should copy stateful expression before evaluating
- [[SPARK-49695]](https://issues.apache.org/jira/browse/SPARK-49695): Postgres fix xor push-down
- [[SPARK-49699]](https://issues.apache.org/jira/browse/SPARK-49699): Disable PruneFilters for streaming workloads
- [[SPARK-49743]](https://issues.apache.org/jira/browse/SPARK-49743): OptimizeCsvJsonExpr should not change schema fields when pruning GetArrayStructFields
- [[SPARK-49782]](https://issues.apache.org/jira/browse/SPARK-49782): ResolveDataFrameDropColumns rule resolves UnresolvedAttribute with child output
- [[SPARK-49791]](https://issues.apache.org/jira/browse/SPARK-49791): Make DelegatingCatalogExtension more extendable
- [[SPARK-49804]](https://issues.apache.org/jira/browse/SPARK-49804): Fix to use the exit code of executor container always
- [[SPARK-49816]](https://issues.apache.org/jira/browse/SPARK-49816): Should only update out-going-ref-count for referenced outer CTE relation
- [[SPARK-49819]](https://issues.apache.org/jira/browse/SPARK-49819): Disable CollapseProject for correlated subqueries in projection over aggregate correctly
- [[SPARK-49829]](https://issues.apache.org/jira/browse/SPARK-49829): Fix the bug on the optimization on adding input to state store in stream-stream join
- [[SPARK-49836]](https://issues.apache.org/jira/browse/SPARK-49836): Fix possibly broken query when window is provided to window/session_window fn
- [[SPARK-49843]](https://issues.apache.org/jira/browse/SPARK-49843): Fix change comment on char/varchar columns
- [[SPARK-49959]](https://issues.apache.org/jira/browse/SPARK-49959): Fix ColumnarArray.copy() to read nulls from the correct offset
- [[SPARK-49979]](https://issues.apache.org/jira/browse/SPARK-49979): Fix AQE hanging issue when collecting twice on a failed plan
- [[SPARK-50021]](https://issues.apache.org/jira/browse/SPARK-50021): Fix `ApplicationPage` to hide App UI links when UI is disabled
- [[SPARK-50022]](https://issues.apache.org/jira/browse/SPARK-50022): Fix `MasterPage` to hide App UI links when UI is disabled
- [[SPARK-50087]](https://issues.apache.org/jira/browse/SPARK-50087): Robust handling of boolean expressions in CASE WHEN for MsSqlServer and future connectors
- [[SPARK-50176]](https://issues.apache.org/jira/browse/SPARK-50176): Disallow reattaching after the session is closed
- [[SPARK-50195]](https://issues.apache.org/jira/browse/SPARK-50195): Fix `StandaloneRestServer` to propagate `spark.app.name` to `SparkSubmit` properly
- [[SPARK-50210]](https://issues.apache.org/jira/browse/SPARK-50210): Fix `SparkSubmit` to show REST API `kill` response properly
- [[SPARK-50235]](https://issues.apache.org/jira/browse/SPARK-50235): Clean up ColumnVector resource after processing all rows in ColumnarToRowExec
- [[SPARK-50258]](https://issues.apache.org/jira/browse/SPARK-50258): Fix output column order changed issue after AQE optimization
- [[SPARK-50312]](https://issues.apache.org/jira/browse/SPARK-50312): SparkThriftServer createServer parameter passing error when kerberos is true
- [[SPARK-50421]](https://issues.apache.org/jira/browse/SPARK-50421): Fix executor related memory config incorrect when multiple resource profiles worked
- [[SPARK-50433]](https://issues.apache.org/jira/browse/SPARK-50433): Fix configuring log4j2 guide docs for Spark on YARN and UT
- [[SPARK-50463]](https://issues.apache.org/jira/browse/SPARK-50463): Fix `ConstantColumnVector` with Columnar to Row conversion
- [[SPARK-50483]](https://issues.apache.org/jira/browse/SPARK-50483): BlockMissingException should be thrown even if ignoreCorruptFiles is enabled
- [[SPARK-50492]](https://issues.apache.org/jira/browse/SPARK-50492): Fix java.util.NoSuchElementException when event time column is dropped after dropDuplicatesWithinWatermark
- [[SPARK-50498]](https://issues.apache.org/jira/browse/SPARK-50498): Avoid unnecessary py4j call in `listFunctions`
- [[SPARK-50505]](https://issues.apache.org/jira/browse/SPARK-50505): Fix `spark.storage.replication.proactive` default value documentation
- [[SPARK-50510]](https://issues.apache.org/jira/browse/SPARK-50510): Fix sporadic ReattachableExecuteSuite failure
- [[SPARK-50545]](https://issues.apache.org/jira/browse/SPARK-50545): `AccessControlException` should be thrown even if `ignoreCorruptFiles` is enabled

### Dependency changes
While being a maintenance release we did still upgrade some dependencies in this release they are:
- [[SPARK-50150]](https://issues.apache.org/jira/browse/SPARK-50150): Upgrade Jetty to 9.4.56.v20240826
- [[SPARK-50316]](https://issues.apache.org/jira/browse/SPARK-50316): Upgrade ORC to 1.9.5

You can consult JIRA for the [detailed changes](https://s.apache.org/spark-3.5.4).

We would like to acknowledge all community members for contributing patches to this release.
