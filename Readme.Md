# Proposal AI Agent setup Documentation

# AI-Powered Proposal & Invoice Generation System

## Key Resources

- **Relevance AI Agent Template**: https://app.relevanceai.com/agents/d7b62b/ae71bf9dff7e-424b-9a5e-e00b1c92391e/ec7526e4-3aae-481a-829f-3f2da1dde041/clone
- **Google Doc Template**: https://docs.google.com/document/d/1C7gWU9yxP5uxoFSmR9HfRtunjr5AP2XtjNlF1raJwUw/edit?tab=t.0

## System Overview

An automated workflow that converts meeting transcripts into professional proposals and invoices using AI tools and integrations.

## Visual Workflow References

1. **Relevance AI Dashboard** 
- Shows the agent configuration interface
- Displays available templates and tools

![](https://github.com/Chakri1407/ProposalAI_Setup/blob/master/ss/Screenshot%202025-02-14%20181250.png)

1. **Stripe Integration Flow** 
    - Webhook initialization
    - Customer creation
    - Invoice item generation
    - Invoice creation and finalization
    - Webhook response handling
    
![](https://github.com/Chakri1407/ProposalAI_Setup/blob/master/ss/Screenshot%202025-02-14%20180122.png)
    
2. [**Make.com](http://make.com/) Workflow** (Image 3)
    - Complete integration flow showing:
        - Initial webhook trigger
        - Router configuration
        - FirefliesAI integration
        - Google Docs connection
        - Tools and text processing
        - Final Relevance AI messaging

![](https://github.com/Chakri1407/ProposalAI_Setup/blob/master/ss/Screenshot%202025-02-14%20175700.png)

## Workflow Steps

### 1. Meeting Transcription (FirefliesAI)

- Captures and transcribes meeting content
- Generates structured meeting notes and key points
- Outputs meeting summary for proposal generation

### 2. Initial Processing ([Make.com](http://make.com/) Router)

- Receives transcribed content from FirefliesAI webhook
- Routes data to appropriate processing streams:
    - Proposal generation path
    - Invoice generation path

### 3. AI Processing (Relevance AI)

- Analyzes meeting transcript
- Extracts key requirements and deliverables
- Generates proposal content using AI template
- Formats information for document generation

### **Relevance AI / Transcription Agent working**

![](https://github.com/Chakri1407/ProposalAI_Setup/blob/master/ss/Screenshot%202025-02-14%20193728.png)

### 4. Document Generation

- Creates proposal document using Google Docs template
- Populates template with AI-generated content
- Includes standard terms and pricing structure
- Generates professional formatting

### 5. Invoice Processing (Stripe)

- Creates customer profile
- Generates invoice items based on proposal
- Creates draft invoice
- Finalizes invoice with payment details

### 6. Notification System

- Sends webhook notifications at key stages
- Updates relevant team members via Slack
- Tracks proposal and invoice status
- Confirms successful document generation
- Sends confirmation email

### Email Confirmation

![](https://github.com/Chakri1407/ProposalAI_Setup/blob/master/ss/Screenshot%202025-02-14%20193711.png)

## Integration Points

- FirefliesAI → [Make.com](http://make.com/) (Webhook)
- [Make.com](http://make.com/) → Relevance AI (API)
- Relevance AI → Google Docs (API)
- [Make.com](http://make.com/) → Stripe (API)
- System → Slack (Notifications)

## System Requirements

- Active subscriptions to: FirefliesAI, [Make.com](http://make.com/), Relevance AI, Stripe
- Configured Google Workspace account
- Slack workspace with appropriate channels
- Webhook endpoints properly configured

## Pending :

- creating contents of a sales call in a mp4 format to generate text for firefly Ai.
