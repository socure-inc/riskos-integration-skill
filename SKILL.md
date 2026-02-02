---
name: riskos-skill
description: This skill focuses on Socure RiskOS Evaluation API integreation
---

# RiskOS Skill

RiskOS™ is a unified platform for identity verification and fraud prevention. It helps reduce compliance costs and streamline fraud management by providing end-to-end fraud, compliance, and risk decisioning capabilities. The platform connects applications to Socure's products using REST APIs and webhooks, enabling real-time user evaluations, fraud detection, and automated compliance decisions.

Use ask_docs to learn more about RiskOS features and capabilities

## When to Use

- Use this skill when building Socure RiskOS Evaluation API client

## Instructions
Guide the user through the process of building RiskOS API Client step by step.

### Plan
Set up the development environment — first, ask me which programming language and framework I want to use.
Guide the user through the process of obtaining an API key for RiskOS — use the ask_docs tool to read API and SDK Keys documentation first
Use the ask_docs tool to read about Sandbox and Prod Environments, understand that list_use_cases, list_workflows and get_checklist pull the data from Sandbox environment
Select a use case — use the list_use_cases tool to retrieve the list of available use cases and ask me which one need to be implemented
Find the live workflow — use the list_workflows tool to identify active workflows. If there is no workflows - remind me to activate one in the RiskOS dashboard.
Read the Integration Guides for the selected use case using ask_docs tool
Use the get_checklist tool to retrieve the checklist for the selected use case and work with me through the integration checklist 
Read the OpenAPI specification stored at references/riskos-api-spec.json file. There are also number of specific postman examples for various use cases in the references directory, check if there is a relevant one
Check if there is a Postman example for the selected use case in the references folder:
   * references/consumer_onboarding - Postman collection for Consumer Onboarding use case. Each file represents a different example
If there is no Postman example for the selected use case, use the consumer onboarding example

### Guidelines
You MUST include all references provided by OWL in your answer.
You MUST make all links in your response clickable.
You MUST use ask_docs tool to search for any information you do not already know.
You MUST NOT use web search to find any answers related to Socure or RiskOS.
You MUST download and review the api_spec tool output to understand the RiskOS API data model for the selected use case.
You MUST plan implementing the tests and run them after each change
If list_workflows returns an empty result, remind me that only live workflows are available for evaluation.
In that case, use ask_docs tool to guide me through the process of activating a workflow in the RiskOS dashboard.
