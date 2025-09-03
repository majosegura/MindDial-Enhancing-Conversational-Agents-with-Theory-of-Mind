# Do Theory-of-Mind Modules Help? Evaluating MindDial Across Booking and Purchase Scenarios

## Description

This project explores whether incorporating Theory of Mind (ToM) reasoning into conversational agents improves their ability to handle misunderstandings. We evaluate the MindDial framework under two realistic scenarios:

* **Booking scenario**: implicit scheduling conflict
* **Forgotten purchase scenario**: explicit duplication conflict

The study compares four configurations of conversational agents:

* No ToM
* First-order ToM
* Second-order ToM
* Full ToM: First-order, Second-order and common ground

## Table of Contents

* Introduction
* Methodology
* Results
* Limitations

## Introduction
In the last decade there has been a rise in the use of conversational agents, however, despite their popularity, these systems often lack the ability to establish common ground with users, a key feature in human interaction.

To address this limitation, **MindDial** was introduced. MindDial is a framework that generates free form responses using **Theory of Mind reasoning**.

Due to that, our research question is, How does integrating Theory of Mind reasoning into conversational agents affect their ability to resolve misunderstandings?

# Methodology

* Framework: **MindDial (2024)**
* Model: **GPT-OSS-20B** (chosen for open access)
* Scenarios:
  *  Booking: schedule dinner overlapping with a dentist appointment
  *  Forgotten Purchase: ordering milk when an order already includes it
*  Configurations tested: No ToM, First-order ToM, Second-order ToM, Full ToM
*  240 responses analyzed manually into three awareness levels:
  *  **1: No Awareness:** ignores conflict
  *  **2: Partial Awareness:** mentions conflict but no clarification
  *  **3: Full Awareness:** detects and asks clarification

# Results
* **Booking scenario:**
  * Harder to detect implicit conflicts
  * **Second-order ToM** showed best improvement in conflict detection
* **Forgotten Purchase scenario:**
  * ToM significantly improved awareness
  * **Second-order ToM (86.7%)** and **Full ToM (83.3%)** achieved highest full-awareness rates
 
# Limitations

* Only two scenarios tested
* Single model (GPT-OSS-20B)
* Manual categorization introduces subjectivity
* No real-user interactions
