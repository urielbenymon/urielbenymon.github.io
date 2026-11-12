---
layout: page
title: PostgreSQL Index Benchmarking
description: A Java/JDBC benchmarking harness for exploring PostgreSQL index performance across database operations.
importance: 3
---

## Overview

This project developed a Java/JDBC benchmarking harness to investigate how PostgreSQL indexing methods behave as database tables grow.

The harness was created during the Columbia University RISE research program (April–July 2025), under the mentorship of Professor Paul Blaer.

**Repository:** [PostgreSQL JDBC Index Timer](https://github.com/urielbenymon/postgresql-jdbc-index-timer)

## Implementation

The harness uses Java, JDBC, Maven, and PostgreSQL to execute timed database operations on tables containing synthetic records.

It examines seven indexing configurations:

1. B-tree
2. Hash
3. GiST
4. GIN
5. BRIN
6. SP-GiST
7. No index (sequential-scan baseline)

The experiments cover insertion, search, and deletion operations at increasing table sizes.

## Benchmarking Approach

The implementation measures elapsed time around JDBC operations and reports timings in nanoseconds and milliseconds.

Search and deletion tests use fixed random seeds to support repeatable target selection.

The harness also examines different comparison operators where supported by the indexing method.

## Limitations

This was an exploratory benchmarking project rather than a controlled performance study.

Measurements were collected without repeated trials or warm-up runs. Timings include JDBC overhead, and PostgreSQL query-plan selection was not systematically verified.

Consequently, the results should not be interpreted as definitive performance rankings between index types.

## Research Context

This project provided an initial foundation for subsequent research on B-tree indexing behavior and database optimization.

That work was presented in the poster *Exploring Improvements to B-Tree Index Structures for Database Optimization* at the Columbia Undergraduate Research Symposium (2025) and Columbia GS Research Festival (2026).
