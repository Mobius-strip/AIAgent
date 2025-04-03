# Food Delivery Support System

A modular, extensible system for handling food delivery customer support queries using LangGraph, OpenAI, and computer vision capabilities.

## Features

- AI-powered classification of customer complaints
- Automated refund processing with receipt verification
- Vision-based verification of issues and bill amounts
- Conversational agent for customer support
- Estimated delivery time information
- Service complaint handling
- Human escalation path for complex issues

## Project Structure

```
food_delivery_support/
├── config.py           # Configuration settings and constants
├── models.py           # Model setup for LLMs and vision models
├── schemas.py          # Type definitions and data schemas
├── nodes.py            # Node implementation functions
├── conditionals.py     # Conditional routing functions
├── graph.py            # Graph construction logic
├── main.py             # Main application entry point
├── setup.py            # Installation and setup script
└── README.md           # Project documentation
```

## Installation

1. Run the setup script to install required packages and configure environment:

```bash
python setup.py
```

2. Enter your OpenAI API key when prompted.

## Usage

Run the main application to start the support agent:

```bash
python main.py
```

Follow the prompts to interact with the support system.

## Workflow

1. User submits an initial complaint
2. System classifies the complaint as refundable or non-refundable
3. For refundable issues:
   - System verifies the problem with image proof
   - System verifies bill amount with receipt image
   - System processes the refund
4. For non-refundable
