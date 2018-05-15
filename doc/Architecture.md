# Architecture Design of BaudSQL 

MySQL driver --> BaudSQL --> BaudEngine

## Compatible with MySQL
BaudSql is compatible with mysql protocol,uses could connect to baudsql through mysql driver.

## Support pluggable Engine

BaudSQL is native supported by BaudEngine,and we suggest users use BaudEngine  which  engine we will give priority to support.

BaudSQL is designed to be decoupled with specified engine.So far we can only support BaudEngine,but we will eventually support multiple engines.

We will provide a unified engine interface specification, users can also implement their own engine according to the interface specification which we provide.

## Distributed Transaction

BaudSQL implement distributed transactions based on two-phase commit.

## Data Model Mapping

table vs space

space = tables sharing the same partitioning key


row vs object

object fields = row fields + the field of 'tableid'

## Metadata Management

There is a 'system' DB on BaudEngine.

The partitioning key,partitioning algorithm,tables,databases,baudegines are included in the 'system' db.

## BaudSqlService

BaudSqlService is primarily responsible for metadata management, modification, presentation, notification, and provides metadata management and browsing interfaces.

## SQL Parsing, Planning, and Executing


