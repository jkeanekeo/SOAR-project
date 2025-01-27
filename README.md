# SOAR Project

## Description
This project integrates Lima Charlie (EDR) with Tines (SOAR) to create an automated workflow for detecting and responding to security threats. It's part of a series focusing on building a Security Operations Center (SOC) workflow.

## Features
- Automated detection using Lima Charlie EDR
- Integration with Tines for orchestration and response
- Slack notifications for real-time alerts
- Email notifications with detailed detection information
- User prompt for machine isolation decisions
- Automated machine isolation via Lima Charlie (optional)

## Prerequisites
- Lima Charlie EDR account
- Tines account
- Slack workspace (for notifications)
- Email account (for notifications)

## Installation

### Lima Charlie Setup
1. Set up Lima Charlie EDR on target machines
2. Configure detection rules in Lima Charlie

### Tines Configuration
1. Create a new story in Tines
2. Set up the webhook for Lima Charlie integration
3. Configure Slack integration in Tines
4. Set up email actions in Tines
5. Create a user prompt page for isolation decisions

## Usage

### Workflow Overview
1. Lima Charlie detects a threat
2. Detection details are sent to Tines via webhook
3. Tines processes the detection and:
   - Sends a Slack notification
   - Sends an email notification
   - Prompts the user for isolation decision
4. If user chooses to isolate, Tines triggers Lima Charlie to isolate the machine

### Key Components
- **Lima Charlie**: Detects threats and sends data to Tines
- **Tines**: 
  - Retrieves detections from Lima Charlie
  - Sends notifications to Slack and email
  - Creates user prompts for decision-making
  - Triggers machine isolation in Lima Charlie (if chosen)

## Configuration Details

### Slack Integration
- Create a dedicated #alerts channel in Slack
- Use the channel ID in Tines for message routing

### Email Notifications
- Configure email settings in Tines
- Customize email content with detection details

### User Prompt
- Create a page in Tines for user decision on machine isolation
- Include relevant detection details in the prompt

## Contact
- Justin Keanekeo
- Email: j.keanekeo@gmail.com

## Acknowledgements
- Lima Charlie for EDR capabilities
- Tines for SOAR functionalities
- Slack for real-time notifications
