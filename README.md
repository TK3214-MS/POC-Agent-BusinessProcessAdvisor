# Overview of the Business Process Advisor declarative agent sample

[![jp](https://img.shields.io/badge/lang-ja-green.svg)](README-JP.md)

![Business Process Advisor Start Screen](assets/BusinessProcessAdvisor1-EN.png)

The "Business Process Advisor" Declarative Agent is an open-source AI-driven tool designed to assist users in understanding complex business process by breaking them down into simple, intermediate, and detailed summaries. This agent acts as a supportive and knowledgeable consultant, dedicated to enhancing users' understanding of complex business process, clarifying desired technical approach using Microsoft services, and defining the right learning process tailored to their goals and needs.

Key features of the Business Process Advisor include:

- **Breaking Down Complex Business Process and Understand the pain point** : Simplifies complex business process into beginner, intermediate, and advanced levels, using analogies, metaphors, and different point of view. Provides glossaries and additional resources for further consideration.

- **Advise how users achieve business process modernization with Microsoft services**: Helps user identifying which Microsoft services can be used to achieve business process modernization.

- **Guiding Optimal Learning Processes**: Assists users in articulating their learning goals, assessing their preferred learning styles, and recommending suitable learning techniques and resources.

- **Creating Structured Learning Plans**: Develops structured study plans for specified topics, allowing users to revise and update the plans as needed.

- **Q&A Preparation**: Offers targeted Q&A discussion plans, explains the motivation of each Q&A items, provides practice questions, identifies knowledge gaps, simulates Q&A experiences, and recommends Q&A discussion strategies.

The Business Process Advisor maintains a professional and supportive tone throughout interactions, ensuring that conversations are contextual and relevant. It integrates with OneDrive, SharePoint, Web search, and Graph Connectors to enhance its capabilities. The agent is designed to adapt its content based on the user's needs, interests, and goals, presenting information in a brief, simple, and logical manner to avoid overwhelming the user.

This open-source project aims to empower individuals to achieve their goals of getting a big picture about how they modernize business process through structured guidance and support. By providing a customizable and extensible framework, the Business Process Advisor Declarative Agent can be adapted to various business process modernization contexts and user needs, making it a versatile tool for personal and professional development.

## Build a basic declarative agent

With the declarative agent, you can build a custom version of Copilot that can be used for specific scenarios, such as for specialized knowledge, implementing specific processes, or simply to save time by reusing a set of AI prompts. For example, a grocery shopping Copilot declarative agent can be used to create a grocery list based on a meal plan that you send to Copilot.

## Get started with the sample

> **Prerequisites**
>
> To run this app sample in your local dev machine, you will need:
>
> - [Node.js](https://nodejs.org/), supported versions: 16, 18
> - A [Microsoft 365 account for development](https://docs.microsoft.com/microsoftteams/platform/toolkit/accounts).
> - [Teams Toolkit Visual Studio Code Extension](https://aka.ms/teams-toolkit) version 5.0.0 and higher or [Teams Toolkit CLI](https://aka.ms/teamsfx-toolkit-cli)
> - [Microsoft 365 Copilot license](https://learn.microsoft.com/microsoft-365-copilot/extensibility/prerequisites#prerequisites)

![Business Process Advisor in action](assets/BusinessProcessAdvisor2.gif)

1. First, select the Teams Toolkit icon on the left in the VS Code toolbar.

2. In the Account section, sign in with your [Microsoft 365 account](https://docs.microsoft.com/microsoftteams/platform/toolkit/accounts) if you haven't already.

3. Create Teams app by clicking `Provision` in "Lifecycle" section.

4. Select `Preview in Copilot (Edge)` or `Preview in Copilot (Chrome)` from the launch configuration dropdown.

5. Once the Copilot app is loaded in the browser, click on the "…" menu and select "Copilot chats". You will see your declarative agent on the right rail. Clicking on it will change the experience to showcase the logo and name of your declarative agent.

6. Ask a question to your declarative agent and it should respond based on the instructions provided.

## What's included in the sample

| Folder       | Contents                                                                                 |
| ------------ | ---------------------------------------------------------------------------------------- |
| `appPackage` | Templates for the Teams application manifest, the GPT manifest and the API specification |
| `env`        | Environment files                                                                        |

The following files can be customized and demonstrate an example implementation to get you started.

| File                                 | Contents                                                                       |
| ------------------------------------ | ------------------------------------------------------------------------------ |
| `appPackage/declarativeAgent.json` | Define the behavior and configurations of the declarative agent.            |
| `appPackage/manifest.json`           | Teams application manifest that defines metadata for your declarative agent. |

The following are Teams Toolkit specific project files. You can [visit a complete guide on Github](https://github.com/OfficeDev/TeamsFx/wiki/Teams-Toolkit-Visual-Studio-Code-v5-Guide#overview) to understand how Teams Toolkit works.

| File           | Contents                                                                                                                                  |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `teamsapp.yml` | This is the main Teams Toolkit project file. The project file defines two primary things: Properties and configuration Stage definitions. |

## Sample Prompt

You can use prompts below to test out how Business Process Advisor agent works.

```
Give me recommended steps to modernize our current process like this with Microsoft services:

### Legacy Manual Inventory Management Process

1. **Stock Counting**:
   - Employees manually count the items in the store and the warehouse. This is often done using pen and paper or simple spreadsheets.
   - The counting process is typically scheduled periodically, such as weekly or monthly, to ensure inventory levels are accurate.

2. **Recording Inventory**:
   - After counting, employees record the inventory levels in a logbook or spreadsheet. This involves noting down the quantities of each item, their locations, and any discrepancies found during the count.
   - The recorded data is then manually entered into the company's inventory management system, if one exists.

3. **Reordering Stock**:
   - Based on the recorded inventory levels, employees determine which items need to be reordered. This decision is often made by comparing current stock levels against predefined reorder points.
   - Purchase orders are manually created and sent to suppliers. This can involve filling out order forms, sending emails, or making phone calls.

4. **Receiving Stock**:
   - When new stock arrives, employees manually check the received items against the purchase orders. This involves counting the items, inspecting them for quality, and noting any discrepancies.
   - The received stock is then manually recorded in the inventory system, and the physical items are placed in their designated locations in the store or warehouse.

5. **Updating Inventory Records**:
   - Throughout the day, as sales are made, employees manually update the inventory records to reflect the items sold. This can involve writing down sales in a logbook or updating a spreadsheet.
   - At the end of the day, these records are reconciled with the point-of-sale (POS) system to ensure accuracy.

### Challenges of Legacy Manual Inventory Management

- **Time-Consuming**: Manual counting and recording of inventory are labor-intensive and time-consuming tasks.
- **Prone to Errors**: Human errors in counting, recording, and data entry can lead to inaccurate inventory levels, resulting in stockouts or overstock situations.
- **Lack of Real-Time Data**: Manual processes do not provide real-time inventory data, making it difficult to make informed decisions quickly.
- **Inefficiency**: The manual process can be inefficient, especially for large inventories, leading to delays in reordering and receiving stock.
```

![Sample01](assets/Sample01.png)

```
Please tell us the value (man-hours reduced) to the organization that can be obtained by introducing Microsoft 365 Copilot.
```

![Sample02](assets/Sample02.png)

```
Based on this information, show the relationship between the license fee and the man-hour reduction effect that can be obtained, and draw the ROI in a graph
```

![Sample03](assets/Sample03.png)

```
I like that graph! I want you to create logo for this project to modernize current legacy business processes
```

![Sample04](assets/Sample04.png)

## Addition information and references

- [Declarative agents for Microsoft 365](https://aka.ms/teams-toolkit-declarative-agent)
- [Microsoft 365 Copilot Extensibility Sample](https://learn.microsoft.com/en-us/microsoft-365-copilot/extensibility/samples)