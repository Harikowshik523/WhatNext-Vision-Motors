# WhatNext Vision Motors

## Project Overview
WhatNext Vision Motors is a Salesforce-based automotive CRM application designed to streamline vehicle ordering, dealer management, inventory tracking, and order processing.

## Problem Statement
Customers often face challenges in identifying the nearest dealer and checking vehicle availability before placing orders. Manual order processing can also lead to delays and inaccuracies.

## Solution
This Salesforce application automates the vehicle ordering process by:
- Suggesting the nearest dealer based on customer location.
- Preventing orders for out-of-stock vehicles.
- Automatically updating order status through scheduled automation.
- Managing vehicle inventory efficiently.

## Features
- Vehicle Management
- Dealer Management
- Customer Management
- Order Management
- Stock Availability Validation
- Automated Order Status Updates
- Reports and Dashboards

## Technologies Used
- Salesforce Platform
- Custom Objects
- Custom Fields
- Validation Rules
- Flows
- Reports & Dashboards

## Apex Components

### Trigger
- VehicleOrderTrigger
  - Executes before and after insert/update events on Vehicle_Order__c.
  - Delegates business logic to VehicleOrderTriggerHandler.

### Apex Classes

#### VehicleOrderTriggerHandler
Features:
- Prevents orders when vehicle stock is unavailable.
- Automatically decreases stock quantity when an order is confirmed.
- Uses Trigger Handler Pattern for better maintainability.

#### VehicleOrderBatch
Features:
- Processes pending orders in bulk.
- Checks stock availability.
- Confirms eligible orders automatically.
- Updates inventory records.

#### VehicleOrderBatchScheduler
Features:
- Schedules VehicleOrderBatch execution daily.
- Automates order reconciliation process.

## Author
Hari Kowshik Kota  
B.Tech CSE  
VR Siddhartha Engineering College
