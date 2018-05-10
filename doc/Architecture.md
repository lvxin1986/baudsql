# Architecture Design of BaudSQL 

MySQL driver --> BaudSQL --> BaudEngine

## Data Model Mapping

table vs space

space = tables sharing the same partitioning key


row vs object

object fields = row fields + the field of 'tableid'

## Metadata Management

There is a 'system' DB on BaudEngine.

## SQL Parsing, Planning, and Executing


