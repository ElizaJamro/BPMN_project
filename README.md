## Project Goal
The purpose of this project is to model the complaint handling process in accordance with the **BPMN 2.0 notation standard**.  
The process includes:
- verification of submitted complaints,  
- communication with the client,  
- decision-making regarding acceptance or rejection,  
- realization of the complaint through refund, replacement, or repair.  

---

## Process Diagram
![Process](https://github.com/user-attachments/assets/78ce248d-29d0-4df4-acd2-3625e7693ab3)

---

## Subprocess: Complaint Realization
![Subprocess](https://github.com/user-attachments/assets/5a34a21a-32bd-4601-93e6-b041771bc5a7)

## BPMN Elements Used
- XOR gateways for exclusive decisions  
- Event-Based Gateway for customer appeal or 14-day timeout  
- Boundary events (message, timer)  
- Message flows for external communication  
- Data objects and stores

## Tools
- bpmn.io  

## How to Open the Diagrams
1. Download  `.bpmn` file
2. Open it in free online editor [bpmn.io](https://bpmn.io/).  
3. For a quick preview, see the exported images in `/screenshots`.

## Logic & Design Challenges
- **Appeal handling**: modeled with an Event-Based Gateway to capture either a message from the client or a 14-day timeout.   
- **Subprocess extraction**: complaint realization was moved into its own subprocess to keep the main process clean.  
- **Message vs. sequence flows**: strictly separated communication with external participants from internal flows.  
