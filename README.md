# HR Policy RAG Assistant

Local-first HR self-service demo that answers policy questions from approved documents and supports role-based employee workflows.

## Status

**Working demo.** It uses sample HR policies and demo employee records. Production use requires privacy review, authentication, access control and integration testing.

## Features

- Employee, Manager, HR and Admin roles
- HR policy document upload
- Document-grounded chatbot responses
- Leave balance and leave-history views
- Leave application and approval workflow
- Policy and company-information administration
- Local Ollama deployment option

## Example Questions

- How many annual leaves do I have?
- What is the maternity leave policy?
- Can I apply for compensatory leave?
- What documents are required for leave approval?
- What are the company attendance rules?

## Architecture

1. Approved documents are uploaded and indexed.
2. The retriever selects relevant policy passages.
3. The LLM generates an answer using only retrieved context.
4. User-specific questions call authorized employee-data tools.
5. The application logs access and workflow activity.

## Technology

Python · FastAPI · Ollama · RAG · Role Based Access · Excel Demo Storage

## Privacy Requirements

- Never expose one employee's salary, attendance or leave details to another employee.
- Separate policy knowledge from confidential employee records.
- Encrypt credentials and personal information.
- Keep an audit log of sensitive queries.
