# Zoho CRM Web Tab Widget
## Comprehensive Requirements Document
**Document Synchronization Intelligence & AI-Powered Document Search**

**Status:** Requirements Finalized  
**Date:** September 4, 2026  
**Version:** 1.0

---

## EXECUTIVE SUMMARY

This document defines the complete requirements for building a **Zoho CRM Web Tab Widget** that provides:

1. **Dashboard** — Advanced analytics for CRM attachments and Google Drive synchronization
2. **AI Chatbot** — Intelligent conversational search and analysis of indexed documents

The widget will consume data from an existing Zoho CRM → Google Drive synchronization integration and layer advanced visualization, analytics, and AI-powered document intelligence on top.

**Primary Goal:** Enable users to have a real-time visual overview of their document ecosystem and ask AI anything about those documents, replacing manual document searching with intelligent conversational search.

---

## 1. PROJECT VISION & USE CASES

### 1.1 Core Purpose
**Document Synchronization Intelligence & AI-Powered Document Search**

Users should be able to:
- Monitor the real-time status of CRM attachment synchronization to Google Drive
- Understand their document ecosystem through visually rich, interactive analytics
- Ask natural-language questions about any document or set of documents
- Retrieve, summarize, and analyze information without manually searching files

### 1.2 Target Users
**Multi-team organization:** Sales, Support, Accounts, Finance teams managing CRM attachments

Persona examples:
- **Sales Manager:** "Show me all quotations for this customer and compare with previous ones"
- **Account Manager:** "Which deals don't have current contracts?"
- **Finance:** "Find all invoices over ₹10,00,000 from the last quarter"
- **Support:** "What documents are available for this customer's issue?"

### 1.3 Key Benefits
- ⚡ **Fast discovery:** Instead of searching manually, ask AI and get instant answers
- 📊 **Visibility:** Real-time dashboard shows sync health and document statistics
- 🔍 **Intelligence:** AI understands document content, not just metadata
- 📁 **Centralization:** One place to monitor and search all CRM documents
- 🔐 **Security:** Respects CRM permissions and document access controls
- 📈 **Analytics:** Track sync trends, document usage, and AI interactions

---

## 2. DASHBOARD MODULE REQUIREMENTS

### 2.1 Visualization Design Philosophy

**Modern, Visually Rich, Enterprise-Grade Analytics Platform**

The dashboard should look and feel like an advanced SaaS analytics platform, not a basic CRM report. Design principles:

- **Advanced Visualizations:** Animated bar/line charts, interactive donut/pie charts, circular gauges, 3D-style charts, real-time trend animations
- **Colorful & Professional:** Use a vibrant but professional color palette suitable for enterprise SaaS
- **Interactive & Responsive:** Hover animations, drill-down capabilities, smooth transitions
- **Information Hierarchy:** Clear prioritization of metrics; no information overload
- **Performance:** Fast loading, smooth animations that don't impact usability
- **Accessibility:** Readable colors, proper contrast, clear labels

**Visual Elements:**
- 📊 Animated bar/line charts for trends
- 🍩 Interactive donut/pie charts for distribution
- 🎯 Circular gauges for sync health and success rates
- ⚡ Animated KPI/stat cards
- 🔄 Sync status animations (pending, in-progress, completed)
- ✨ Smooth hover, transition, and loading animations
- 🌈 Glowing effects and gradient backgrounds where appropriate

### 2.2 Core KPI Cards & Metrics

#### Synchronization Overview
```
┌─────────────────────────────────────────────┐
│ 📎 Total CRM Attachments          1,247     │
│ ☁️  Synced to Google Drive          958     │
│ ⚠️  Non-Synchronized Files          189     │
│ ❌ Failed Synchronizations           100    │
│                                             │
│ 📈 Sync Success Rate              76.8%    │
│    (animated gauge/progress)                │
└─────────────────────────────────────────────┘
```

**Required Metrics:**
- Total CRM attachments (all time)
- Total files synced to Google Drive
- Non-synchronized files count
- Failed sync count
- Successful sync count
- Sync success rate (%) - with animated gauge
- Total file size (GB/MB)
- Storage utilization

#### Time-Based Metrics
- Files synced today
- Files synced this week
- Files synced this month
- Trend chart (daily/weekly sync volume)

#### File Type Distribution
```
┌──────────────────────────────────┐
│ File Type        Count      %    │
├──────────────────────────────────┤
│ PDF              342       27.4% │
│ DOCX             281       22.5% │
│ JPG              156       12.5% │
│ XLSX             98         7.8% │
│ PNG              87         7.0% │
│ Other            303       24.3% │
└──────────────────────────────────┘
```

Display as:
- Interactive bar chart
- Pie chart with percentages
- Filterable list
- Show count and total size per type

#### CRM Module Distribution
```
Accounts:  345 attachments (27.6%)
Deals:     428 attachments (34.3%)
Contacts:  287 attachments (23.0%)
Leads:     187 attachments (15.0%)
```

Display as:
- Horizontal bar chart
- Click to filter/drill-down

#### Sync Status Breakdown
```
✅ Synced:           958 files
⏳ Syncing:           12 files
⚙️  Pending:          34 files
❌ Failed:          100 files
🔒 Sensitivity Hold: 143 files
```

#### Recent Synchronization Activity
- Last 15–20 sync events with:
  - File name
  - CRM module/record
  - Sync status (✅ Synced / ❌ Failed / ⏳ Pending)
  - Timestamp
  - Size
  - Duration
  - Google Drive link

#### Failed Synchronization Details
- File name
- CRM record
- Error code and message
- Last attempt time
- Retry count
- Manual retry option

#### Non-Synchronized Files
- File name
- CRM record
- Attachment ID
- Size
- Age (how long not synced)
- Reason (if known)

#### File Size Statistics
- Total storage used
- Average file size
- Largest file
- Distribution by size range
- Growth trend

#### Google Drive Integration Info
- Drive folder path/link
- Total files in Drive
- Drive storage quota
- Drive storage used
- Sync folder organization structure

### 2.3 Dashboard Features

**Search & Filters**
- Filter by CRM module (Accounts, Deals, Contacts, Leads, etc.)
- Filter by file type
- Filter by sync status (synced/failed/pending/not synced)
- Filter by date range
- Filter by size range
- Multi-select filters

**Drill-Down & Details**
- Click on any metric to see detailed breakdown
- Click on file type to see all files of that type
- Click on module to see all files from that module
- Click on date to see activity for that day

**Export & Reporting**
- Export dashboard snapshot
- Export metrics data (CSV)
- Scheduled email reports (future)

**Real-Time Updates**
- Auto-refresh every 30–60 seconds
- Event-driven updates when sync completes
- Manual refresh button
- "Last updated" timestamp

---

## 3. AI CHATBOT MODULE REQUIREMENTS

### 3.1 Chatbot Core Capabilities

The chatbot should act as an **intelligent document assistant** that understands:
- **Context:** Current CRM record (Account, Deal, etc.) or organization-wide scope
- **Intent:** Search, summarize, extract, compare, analyze
- **Content:** Document text, extracted data, metadata
- **Permissions:** User's access to documents

#### Capability Matrix

| Capability | Description | Example |
|-----------|-------------|---------|
| **Document Search** | Find files by name, type, CRM record | "Find the latest quotation for ABC Ltd" |
| **File Discovery** | Identify relevant files for queries | "Show me all contracts for this customer" |
| **Content Understanding** | Read and understand document contents | "What's in this PDF?" |
| **Question Answering** | Answer questions about documents | "What is the invoice amount?" |
| **Information Extraction** | Extract specific data from documents | "Extract all customer names from this file" |
| **Summarization** | Summarize individual or multiple files | "Summarize this contract" |
| **Comparison** | Compare information across files | "Compare this quotation with the previous one" |
| **Source Attribution** | Show which file the answer came from | "Answer + link to source document" |
| **File Retrieval** | Open/download relevant files | Provide Google Drive and CRM links |
| **Sync Intelligence** | Answer about sync status | "Which files failed to sync this week?" |
| **Multi-Document Reasoning** | Reason across multiple files | "Find all invoices for this customer and calculate total" |

### 3.2 Example User Interactions

**Basic Document Search**
```
User: "Find the quotation for ABC Private Ltd"
AI: "I found 3 quotations for ABC Private Ltd:
    1. quotation_ABC_2026-08.pdf (Aug 2026) - ₹2,45,000
    2. quotation_ABC_2026-05.pdf (May 2026) - ₹1,98,000
    3. quotation_ABC_2025-11.pdf (Nov 2025) - ₹1,50,000
    
    The latest is from August 2026 with amount ₹2,45,000.
    
    📄 Open in CRM | ☁️ Open in Drive"
```

**Content-Based Questions**
```
User: "What is mentioned in this PDF?"
AI: "This PDF is a quotation for ABC Private Ltd dated August 15, 2026.

Key Details:
- Quotation Amount: ₹2,45,000
- Items: Product A (20 units), Product B (15 units)
- Terms: Net 30 days
- Valid until: September 15, 2026

Source: quotation_ABC_2026-08.pdf | 📄 View in CRM"
```

**Filtered Searches**
```
User: "Find all JPG files uploaded for this customer"
AI: "I found 7 JPG files for this customer:
    1. product_photo_1.jpg (May 2026)
    2. invoice_scan_2026-03.jpg (March 2026)
    3. signature_page.jpg (March 2026)
    ... [and 4 more]"
```

**Information Extraction**
```
User: "What is the invoice amount mentioned in the document?"
AI: "The invoice amount is ₹2,45,000.

Additional Details:
- Invoice Number: INV-2026-1045
- Due Date: September 20, 2026
- Paid: No

Source: invoice_scan_2026-09.pdf"
```

**Summarization**
```
User: "Summarize this document"
AI: "[Summary of main contract terms, obligations, dates, amounts]

Full document: contract_ABC_2026-01.pdf | 📄 View"
```

**Sync Intelligence**
```
User: "Are there any files that have not been synchronized to Google Drive?"
AI: "Yes, there are 34 non-synchronized files:
    
    By Type:
    - PDF: 12 files
    - DOCX: 8 files
    - JPG: 10 files
    - Other: 4 files
    
    Oldest: quotation_xyz.pdf (Not synced for 5 days)
    
    Would you like me to retry these syncs?"
```

**Multi-File Analysis**
```
User: "Compare this customer's quotation with their previous quotations"
AI: "Comparison for ABC Private Ltd:

Latest (Aug 2026): ₹2,45,000
Previous (May 2026): ₹1,98,000 (+23.7%)
Previous (Nov 2025): ₹1,50,000 (+63.3%)

The quotation amount has increased 63% over the past year,
likely due to increased quantity and product variations.

Sources:
- quotation_ABC_2026-08.pdf
- quotation_ABC_2026-05.pdf
- quotation_ABC_2025-11.pdf"
```

### 3.3 Search Scope

#### Current Record Scope (Default)
- When the widget opens from an Account, Deal, Contact, or Lead record
- Search and chat are scoped to that record's attachments and related Google Drive files
- Users can ask: "Summarize the documents for this deal" or "Show me all JPG files"

#### Organization-Wide Scope (Optional)
- User can toggle to search across entire organization
- Enables cross-record analysis and comparisons
- Example: "Find all contracts with this company across all deals"
- Must respect user's CRM permissions and access controls

#### UI for Scope Selection
```
🤖 AI Document Assistant

Search scope: [Current Record ▼]
  ● Current Record
  ○ Current Module (all Deals)
  ○ Entire Organization
  
Ask anything about your documents...
```

### 3.4 Supported Document Types

**Text-Based Documents**
- PDF (both text and scanned/image-based)
- DOCX, DOC (Microsoft Word)
- TXT (plain text)
- CSV, TSV (spreadsheets as text)
- XLS, XLSX (Excel spreadsheets)

**Image-Based Documents (with OCR)**
- JPG, JPEG
- PNG
- Scanned PDFs (image-based)
- Screenshots
- Invoices, receipts, contracts (as images)

**Archives & Other**
- ZIP files (metadata extraction, file listing)
- Other supported file types (metadata only)

### 3.5 Document Processing

**For Text Documents:**
1. Download from CRM/Google Drive
2. Extract text
3. Clean and normalize
4. Chunk into semantic pieces
5. Generate OpenAI embeddings
6. Store in PostgreSQL + pgvector

**For Image/Scanned Documents:**
1. Download from CRM/Google Drive
2. Detect format
3. Run OCR (extract text from images)
4. Extract structured data if applicable (tables, forms)
5. Clean and normalize
6. Chunk into pieces
7. Generate embeddings
8. Store with OCR confidence metadata

**Metadata Storage:**
- File name
- File type
- File size
- CRM module and record ID
- Google Drive file ID and folder
- Sync status
- Creation/modification dates
- Access permissions (who can view)
- Sensitivity classification
- Extracted content summary

---

## 4. CRM MODULES & ATTACHMENT TRACKING

### 4.1 Primary Modules (Phase 1 Focus)

| Module | Priority | Use Case |
|--------|----------|----------|
| Accounts | PRIMARY | Company-level documents, agreements, contracts |
| Deals | PRIMARY | Quotations, proposals, invoices, contracts |
| Contacts | HIGH | Customer-specific documents |
| Leads | HIGH | Prospect-related documents |

### 4.2 Secondary Modules (for Dashboard Tracking)

| Module | Use Case |
|--------|----------|
| Products | Product specifications, datasheets |
| Quotes | Formal quotations and supporting docs |
| Sales Orders | Order documentation |
| Invoices | Invoice attachments |
| Purchase Orders | Purchasing documents |
| Cases | Support/customer issue documents |

### 4.3 Extensibility

The architecture must support:
- Adding new CRM modules with minimal code changes
- Enabling/disabling modules via configuration
- Custom modules created by users
- Different attachment tracking policies per module (future)

### 4.4 Module-Level Statistics

Dashboard should show:
- Attachment count per module
- Sync status breakdown per module
- File type distribution per module
- Sync success rate per module
- Storage usage per module
- Growth trends per module

---

## 5. EXISTING ZOHO CRM → GOOGLE DRIVE INTEGRATION

### 5.1 Current State

An automatic synchronization integration already exists and is production-ready. It provides:

**Functionality:**
- Automatic detection of new CRM attachments
- Uploading files to corresponding Google Drive folders
- Support for multiple file types (images, PDFs, documents, spreadsheets, archives)
- Tracking synchronization status (success, failure, pending)
- Error handling and retry logic
- Handling of Zoho API rate limits
- Generation of Google Drive file links
- Handling of non-synchronized and failed files

**Metadata Captured:**
- Attachment ID, file name, file type, size
- CRM module and record ID
- Google Drive file ID, folder ID, URL
- Sync status, timestamps
- Error codes and messages

### 5.2 New Widget's Role

The Web Tab Widget **does not replace** the existing integration. Instead, it:

1. **Consumes** synchronization data from the existing integration
2. **Provides** centralized monitoring and analytics
3. **Adds** AI-powered document intelligence
4. **Displays** sync health, trends, failures, and recoveries

### 5.3 Data Flow

```
┌────────────────────────────┐
│  Zoho CRM Attachments      │
│  (User uploads document)   │
└──────────────┬─────────────┘
               │
               ↓
┌────────────────────────────────┐
│  Existing Sync Integration      │
│  (Automatic CRM → GDrive)       │
└──────────────┬─────────────────┘
               │
               ├─→ Google Drive (File Storage)
               │
               ├─→ Zoho CRM Sync Logs (Metadata)
               │   └─ Custom Module: Document Sync Logs
               │
               ├─→ PostgreSQL (Analytics Backend)
               │
               └─→ New Web Tab Widget
                   ├─ Dashboard (Analytics)
                   └─ AI Chatbot (Document Intelligence)
```

---

## 6. DATA STORAGE & ARCHITECTURE

### 6.1 Zoho CRM Custom Module: "Document Sync Logs"

**Purpose:** Track each attachment synchronization event

**Fields:**
```
Sync Log Record
├── CRM Module (Accounts, Deals, Contacts, Leads, etc.)
├── CRM Record ID (UUID from Zoho)
├── CRM Record Name (Account name, Deal name, etc.)
├── Attachment ID (Zoho attachment ID)
├── File Name (original filename)
├── File Type (PDF, DOCX, JPG, etc.)
├── File Size (bytes)
├── Google Drive File ID
├── Google Drive Folder ID
├── Google Drive URL
├── Sync Status (Synced, Failed, Pending, Not Synced)
├── Sync Started At (timestamp)
├── Sync Completed At (timestamp)
├── Last Attempt (timestamp)
├── Retry Count (number)
├── Error Code (if failed)
├── Error Message (if failed)
├── Sync Duration (seconds)
├── Uploaded By (user who attached file)
├── Last Updated (timestamp)
└── Metadata (JSON for additional data)
```

**Benefits:**
- Persistent record of all sync events
- Enables dashboard analytics via Zoho API
- Supports reporting and auditing
- Forms the foundation for sync history

### 6.2 PostgreSQL Backend Database

**Purpose:** Store application data for dashboard analytics, AI indexing, and audit trails

**Primary Tables:**

#### sync_logs
```sql
CREATE TABLE sync_logs (
  id UUID PRIMARY KEY,
  zoho_sync_log_id VARCHAR,
  crm_module VARCHAR,
  crm_record_id VARCHAR,
  crm_record_name VARCHAR,
  attachment_id VARCHAR,
  file_name VARCHAR,
  file_type VARCHAR,
  file_size BIGINT,
  gdrive_file_id VARCHAR,
  gdrive_folder_id VARCHAR,
  gdrive_url VARCHAR,
  sync_status VARCHAR, -- synced, failed, pending, not_synced
  sync_started_at TIMESTAMP,
  sync_completed_at TIMESTAMP,
  retry_count INT,
  error_code VARCHAR,
  error_message TEXT,
  sync_duration INT, -- seconds
  user_id VARCHAR,
  created_at TIMESTAMP,
  updated_at TIMESTAMP,
  INDEX (crm_module, crm_record_id, sync_status, created_at)
);
```

#### documents
```sql
CREATE TABLE documents (
  id UUID PRIMARY KEY,
  sync_log_id UUID REFERENCES sync_logs,
  file_name VARCHAR,
  file_type VARCHAR,
  file_size BIGINT,
  gdrive_file_id VARCHAR,
  crm_module VARCHAR,
  crm_record_id VARCHAR,
  gdrive_folder_id VARCHAR,
  content_hash VARCHAR, -- for deduplication
  has_text_content BOOLEAN,
  has_images BOOLEAN,
  page_count INT, -- for PDFs
  extracted_summary TEXT, -- brief summary of content
  sensitivity_level VARCHAR, -- public, internal, confidential, highly_confidential
  access_permissions JSONB, -- who can access
  created_at TIMESTAMP,
  updated_at TIMESTAMP,
  indexed_at TIMESTAMP,
  INDEX (crm_module, crm_record_id, file_type, created_at)
);
```

#### document_chunks
```sql
CREATE TABLE document_chunks (
  id UUID PRIMARY KEY,
  document_id UUID REFERENCES documents,
  chunk_index INT,
  chunk_text TEXT,
  embedding vector(1536), -- OpenAI embeddings
  chunk_metadata JSONB, -- page number, section, etc.
  start_char INT,
  end_char INT,
  created_at TIMESTAMP,
  INDEX USING ivfflat (embedding vector_cosine_ops) -- pgvector index
);
```

#### chat_sessions
```sql
CREATE TABLE chat_sessions (
  id UUID PRIMARY KEY,
  user_id VARCHAR,
  crm_record_id VARCHAR,
  scope VARCHAR, -- current_record, org_wide
  started_at TIMESTAMP,
  last_message_at TIMESTAMP,
  created_at TIMESTAMP,
  INDEX (user_id, created_at)
);
```

#### chat_messages
```sql
CREATE TABLE chat_messages (
  id UUID PRIMARY KEY,
  session_id UUID REFERENCES chat_sessions,
  role VARCHAR, -- user, assistant
  content TEXT,
  retrieved_document_ids UUID[],
  retrieval_scores FLOAT8[],
  tokens_used INT,
  response_time_ms INT,
  created_at TIMESTAMP,
  INDEX (session_id, created_at)
);
```

#### sync_errors
```sql
CREATE TABLE sync_errors (
  id UUID PRIMARY KEY,
  sync_log_id UUID REFERENCES sync_logs,
  error_code VARCHAR,
  error_message TEXT,
  retry_count INT,
  next_retry_at TIMESTAMP,
  resolved BOOLEAN,
  resolved_at TIMESTAMP,
  created_at TIMESTAMP,
  INDEX (sync_log_id, resolved, next_retry_at)
);
```

#### audit_logs
```sql
CREATE TABLE audit_logs (
  id UUID PRIMARY KEY,
  user_id VARCHAR,
  action VARCHAR, -- document_accessed, query_executed, sync_completed, etc.
  resource_type VARCHAR, -- document, chat_session, etc.
  resource_id VARCHAR,
  details JSONB,
  created_at TIMESTAMP,
  INDEX (user_id, resource_type, created_at)
);
```

#### integration_settings
```sql
CREATE TABLE integration_settings (
  id UUID PRIMARY KEY,
  setting_key VARCHAR UNIQUE,
  setting_value JSONB,
  updated_at TIMESTAMP
);
```

### 6.3 Vector Store: PostgreSQL + pgvector

**Purpose:** Store and retrieve document embeddings for semantic search

**Architecture:**
- Use pgvector PostgreSQL extension
- Store OpenAI embeddings (1536-dimensional vectors) in document_chunks table
- Enable similarity search with cosine distance metric
- Combine with metadata and keyword search for hybrid retrieval

**Benefits:**
- Single database (PostgreSQL) — simpler infrastructure
- Embeddings stored alongside metadata
- Can query semantic similarity + CRM metadata in one transaction
- No need for separate vector database (initially)

**Scaling Note:** If document volume grows significantly (100K+ documents), consider migrating to dedicated vector database (Qdrant, Weaviate, Pinecone) while keeping PostgreSQL for metadata.

---

## 7. AI & RAG ARCHITECTURE

### 7.1 AI/LLM Provider

**Primary:** OpenAI (GPT-4 for reasoning, text-davinci-003 for embeddings)

**Why OpenAI:**
- Strong document understanding and multi-step reasoning
- Powerful embeddings for semantic search
- Function calling support for structured queries
- File search capabilities (beta)
- Production-grade reliability

**Future Flexibility:**
- Design with provider abstraction layer
- Support Claude (Anthropic) as secondary option
- Support Gemini (Google) for Drive integration
- Support Zoho Zia (native CRM AI)

### 7.2 RAG (Retrieval-Augmented Generation) Strategy

**Flow:**
```
User Query
  ↓
1. Intent Recognition
  (What does the user want? Search? Summarize? Extract?)
  ↓
2. Scope Determination
  (Current record or org-wide?)
  ↓
3. Hybrid Retrieval
  ├─ Semantic Search (vector similarity via pgvector)
  ├─ Keyword Search (full-text + regex)
  └─ Metadata Filtering (CRM module, file type, date, etc.)
  ↓
4. Permission Verification
  (Can this user access these documents?)
  ↓
5. Document Chunk Ranking
  (Score and rank results by relevance and confidence)
  ↓
6. LLM Processing
  (Feed top results to OpenAI LLM)
  ↓
7. Answer Generation
  (LLM generates natural language answer with citations)
  ↓
8. Response with Sources
  User sees: Answer + Source documents + Google Drive links + CRM links
  ↓
9. Audit Logging
  (Log query, documents retrieved, response, user action)
```

### 7.3 Hybrid Retrieval Components

#### Semantic Search (Vector Similarity)
```python
# Find semantically similar document chunks
similar_chunks = db.query(
  "SELECT document_id, chunk_text, similarity FROM documents 
   WHERE embedding <=> query_embedding < 0.5
   ORDER BY embedding <=> query_embedding
   LIMIT 10"
)
```
**Use for:** Content-based searches, understanding document meaning

#### Keyword Search (Full-Text + Metadata)
```sql
SELECT documents FROM documents 
WHERE file_name ILIKE '%invoice%' 
  AND file_type = 'PDF'
  AND crm_module = 'Deals'
  AND created_at > '2026-08-01'
```
**Use for:** Exact file names, known documents, quick lookup

#### Metadata Filtering
```sql
WHERE crm_module IN ('Accounts', 'Deals')
  AND crm_record_id = 'xxx'
  AND file_type IN ('PDF', 'DOCX')
  AND sync_status = 'synced'
  AND sensitivity_level IN ('public', 'internal')
```
**Use for:** Scope queries, permission-based filtering

#### CombinedQuery Example
```
User: "Find the latest quotation for ABC Private Ltd with amount > ₹2,00,000"

1. Semantic: Find chunks mentioning "quotation" + "ABC" + "amount"
2. Keyword: file_name LIKE '%quotation%'
3. Metadata: file_type = 'PDF', crm_module = 'Deals', 
   crm_record_name LIKE '%ABC%'
4. Temporal: created_at in last 90 days
5. Permission: user can access Deals records
6. Combine results by relevance score
7. Feed top 3 results to LLM to extract amount and determine "latest"
```

### 7.4 Document Processing Pipeline

**Input:** Zoho CRM attachment or Google Drive file

**Steps:**

1. **Download**
   - Fetch file from Zoho CRM or Google Drive
   - Store temporarily in backend

2. **File Type Detection**
   - Identify format (PDF, DOCX, JPG, etc.)
   - Route to appropriate processor

3. **Text Extraction**
   - For PDF: Use PyPDF2 or pdfplumber
   - For DOCX: Use python-docx
   - For TXT/CSV: Direct read
   - For XLS/XLSX: Use openpyxl

4. **OCR for Images**
   - For JPG/PNG: Pytesseract + Tesseract OCR
   - For scanned PDFs: Pytesseract on each page
   - Extract text, preserve page/location info
   - Extract tables if detected
   - Generate confidence scores

5. **Structured Data Extraction**
   - Extract tables from PDFs/images
   - Parse forms and key-value pairs
   - Identify document type (invoice, contract, quotation, etc.)
   - Extract key metadata (amounts, dates, names)

6. **Text Cleaning & Normalization**
   - Remove extra whitespace
   - Fix encoding issues
   - Standardize dates and numbers
   - Remove headers/footers if needed

7. **Chunking**
   - Split into semantic chunks (paragraphs, sections)
   - Or fixed-size chunks (500-1000 tokens)
   - Preserve chunk boundaries (no mid-sentence breaks)
   - Add context metadata (page number, section name, etc.)

8. **Embedding Generation**
   - Use OpenAI text-embedding-3-small or text-embedding-3-large
   - Batch processing for efficiency
   - Cache embeddings to avoid re-processing

9. **Vector Store Indexing**
   - Store chunks in PostgreSQL + pgvector
   - Create vector index (ivfflat for faster search)
   - Store metadata (page, section, file_id, etc.)

10. **Audit & Logging**
    - Log ingestion timestamp, token count, duration
    - Store OCR confidence scores
    - Track any errors or warnings

**Error Handling:**
- Corrupt file → skip, log error
- Unsupported format → log warning
- OCR confidence too low → flag for manual review
- Embedding generation failure → retry with backoff

### 7.5 Query Processing & Response

**User Query Flow:**

1. **Receive Query**
   ```
   User: "What is the total amount in the quotations for ABC Ltd?"
   Scope: Current Record (Deal)
   ```

2. **Intent Classification**
   - Is this a search query?
   - Is this asking for analysis/comparison?
   - Is this asking for summarization?
   - What entities are mentioned? (company name, document type, amount)

3. **Retrieve Context**
   - If in current record scope: get that record's attachments
   - If org-wide: query all accessible documents
   - Check user's CRM permissions

4. **Hybrid Search**
   - Semantic: Find chunks matching "quotation", "ABC Ltd", "amount"
   - Keyword: file_type = 'PDF', file_name LIKE '%quotation%'
   - Metadata: sync_status = 'synced', sensitivity allowed
   - Score and rank by relevance

5. **Permission Verification**
   - For each retrieved document, check user can access it
   - For sensitive documents, verify explicit permission
   - Remove unauthorized results

6. **Prepare Context for LLM**
   ```
   Retrieved Context:
   [Document 1: quotation_ABC_2026-08.pdf]
   - Amount: ₹2,45,000
   - Date: Aug 2026
   - Status: Approved
   
   [Document 2: quotation_ABC_2026-05.pdf]
   - Amount: ₹1,98,000
   - Date: May 2026
   - Status: Rejected
   
   User Question: "What is the total amount in the quotations for ABC Ltd?"
   ```

7. **LLM Processing**
   - Send context + question to OpenAI
   - LLM generates answer from provided context
   - LLM cites sources

8. **Generate Response**
   ```
   AI: "The total amount in the quotations for ABC Ltd is ₹4,43,000.
   
   Breakdown:
   - Latest (Aug 2026): ₹2,45,000 (Approved)
   - Previous (May 2026): ₹1,98,000 (Rejected)
   
   Source Documents:
   - quotation_ABC_2026-08.pdf
   - quotation_ABC_2026-05.pdf
   
   [📄 View in CRM] [☁️ Open in Drive]"
   ```

9. **Log Interaction**
   ```sql
   INSERT INTO chat_messages (
     session_id, role, content, 
     retrieved_document_ids, response_time_ms
   ) VALUES (...)
   ```

---

## 8. BACKEND TECHNOLOGY STACK

### 8.1 API Framework

**Technology:** Python + FastAPI

**Why FastAPI:**
- Modern, fast, Python-based (strong AI/ML ecosystem)
- Asynchronous I/O (async/await) for I/O-heavy operations
- Automatic API documentation (Swagger/OpenAPI)
- Built-in validation and serialization
- Easy integration with background tasks and job queues
- Excellent for microservices

**Architecture:**
```
FastAPI Application
├── Auth Routes (Zoho OAuth 2.0, Google OAuth 2.0)
├── Dashboard API Routes
│   ├── /api/dashboard/kpis
│   ├── /api/dashboard/sync-trends
│   ├── /api/dashboard/file-types
│   ├── /api/dashboard/module-stats
│   └── /api/dashboard/recent-activity
├── Chatbot API Routes
│   ├── /api/chat/sessions
│   ├── /api/chat/messages (POST)
│   ├── /api/chat/search
│   └── /api/chat/retrieve-document
├── Document Processing Routes
│   ├── /api/documents/ingest
│   ├── /api/documents/index
│   └── /api/documents/list
├── Settings Routes
│   ├── /api/settings/sync-config
│   └── /api/settings/integration-status
└── Background Tasks
    ├── Sync attachment scanning
    ├── Document ingestion/indexing
    ├── Embedding generation
    └── Retry failed syncs
```

### 8.2 Databases

#### Primary: PostgreSQL
- **Purpose:** Store application data, metadata, audit logs
- **Hosting:** AWS RDS (managed PostgreSQL)
- **Version:** PostgreSQL 14+
- **Extensions:** pgvector (for embeddings), uuid-ossp

**Connection Pooling:**
- Use pgBouncer or SQLAlchemy pool (async)
- Min pool size: 5, Max: 20
- Connection timeout: 30 seconds

#### Data Persistence:
- Regular backups (daily, 7-day retention)
- Point-in-time recovery enabled
- Encryption at rest (AWS KMS)

### 8.3 Caching & Background Jobs

**Redis (AWS ElastiCache)**
- **Purpose:** Caching, session storage, job queue coordination
- **Use Cases:**
  - Cache frequently accessed dashboard metrics
  - Store chat session data
  - Coordinate Celery task queue
  - Rate limiting for API calls

**Celery + Redis**
- **Purpose:** Background job processing
- **Tasks:**
  - Sync attachment detection (scheduled, every 5–15 min)
  - Document ingestion and OCR
  - Embedding generation (batch)
  - Failed sync retries
  - Periodic maintenance tasks

**Example Celery Setup:**
```python
# tasks.py
@shared_task
def process_document(document_id):
    # Download, extract text, OCR, chunk, embed
    pass

@shared_task
def sync_attachments_background():
    # Check Zoho CRM for new attachments
    # Create sync jobs
    pass

# Scheduled
periodic_tasks = {
    'sync-attachments': {
        'task': 'app.tasks.sync_attachments_background',
        'schedule': crontab(minute='*/10'),  # Every 10 min
    },
}
```

### 8.4 AI & Embeddings

**OpenAI API**
- **Embeddings Model:** text-embedding-3-small or 3-large
- **LLM Model:** gpt-4-turbo or gpt-4
- **API Key:** Stored in AWS Secrets Manager
- **Rate Limiting:** Implement with Redis

```python
import openai

# Embedding
embedding = openai.Embedding.create(
    input=text,
    model="text-embedding-3-small"
)

# Chat/Completion
response = openai.ChatCompletion.create(
    model="gpt-4-turbo",
    messages=[
        {"role": "system", "content": "You are a document assistant..."},
        {"role": "user", "content": user_query}
    ],
    temperature=0.7,
    max_tokens=500
)
```

### 8.5 Hosting & Deployment

**Development:**
- Run locally: `uvicorn main:app --reload`
- Connect to local PostgreSQL or AWS RDS

**Staging:**
- AWS App Runner (managed container service)
- Pulls from ECR (Elastic Container Registry)

**Production:**
```
┌────────────────────────────────────────────┐
│         AWS Infrastructure                  │
├────────────────────────────────────────────┤
│                                              │
│  ┌──────────────────────────────────────┐  │
│  │  Application Load Balancer (HTTPS)   │  │
│  └────────────┬─────────────────────────┘  │
│               │                             │
│  ┌────────────▼─────────────────────────┐  │
│  │  ECS Fargate (FastAPI Container)     │  │
│  │  - Auto-scaling (2-10 tasks)         │  │
│  │  - Health checks                     │  │
│  └────────────┬─────────────────────────┘  │
│               │                             │
│  ┌────────────┼──────────────────────────┐ │
│  │            │                          │ │
│  ▼            ▼                          ▼ │
│┌──────┐   ┌─────────┐   ┌────────────┐   │
││ RDS  │   │ElastiCache│ │   S3       │   │
││  PG  │   │  Redis   │ │(file cache)│   │
│└──────┘   └─────────┘   └────────────┘   │
│                                              │
└────────────────────────────────────────────┘
```

**Cost Optimization:**
- Use Reserved Instances for predictable workloads
- Auto-scaling based on CPU/memory
- Scheduled scaling (lower capacity at night)
- S3 for long-term document storage

### 8.6 Monitoring & Logging

**CloudWatch (AWS)**
- Application logs
- Metrics: CPU, memory, request count, error rate
- Alarms for errors, high latency

**Error Tracking:**
- Sentry or similar for exception tracking
- Real-time alerts for errors

**Performance Monitoring:**
- Datadog or New Relic for APM
- Track API latency, database queries
- Identify bottlenecks

---

## 9. AUTHENTICATION & AUTHORIZATION

### 9.1 OAuth 2.0 Architecture

**Authentication Flow (Server-Side Confidential)**

```
┌──────────────────┐
│   Zoho Web Tab   │
│    (Frontend)    │
└────────┬─────────┘
         │ Authenticated user session
         │ (No tokens in JS)
         ↓
┌──────────────────────────────────┐
│   FastAPI Backend (Secure)       │
│  ┌──────────────────────────────┐│
│  │  Zoho OAuth Tokens           ││
│  │  - Access Token (1 hour)     ││
│  │  - Refresh Token (long-lived)││
│  │  - Encrypted at rest         ││
│  └──────────────────────────────┘│
│  ┌──────────────────────────────┐│
│  │  Google OAuth Tokens         ││
│  │  - Access Token              ││
│  │  - Refresh Token (offline)   ││
│  │  - Encrypted at rest         ││
│  └──────────────────────────────┘│
└────┬────────────────────────┬────┘
     │                        │
     ↓                        ↓
┌─────────────────┐  ┌──────────────┐
│  Zoho CRM API   │  │ Google Drive  │
│   (OAuth 2.0)   │  │   (OAuth 2.0) │
└─────────────────┘  └──────────────┘
```

### 9.2 Zoho CRM OAuth 2.0 Integration

**Setup:**
1. Register app in Zoho Developer Console
2. Get Client ID and Client Secret
3. Configure redirect URI: `https://backend.example.com/auth/zoho/callback`

**Token Management:**
```python
# Initial authorization
@app.get("/auth/zoho/authorize")
async def zoho_authorize():
    # Redirect to Zoho OAuth consent
    return RedirectResponse(zoho_auth_url)

# Callback (after user consents)
@app.get("/auth/zoho/callback")
async def zoho_callback(code: str):
    # Exchange code for tokens
    token_response = await zoho_client.get_token(code)
    
    # Store encrypted refresh token in database
    user = await db.get_user(zoho_user_id)
    user.zoho_refresh_token = encrypt(token_response.refresh_token)
    user.zoho_access_token = encrypt(token_response.access_token)
    user.zoho_token_expires_at = token_response.expires_in
    await db.save(user)
    
    # Create session cookie
    response = RedirectResponse("/dashboard")
    response.set_cookie("session_id", session_id, secure=True, httponly=True)
    return response

# Auto-refresh tokens
async def get_zoho_access_token(user_id: str):
    user = await db.get_user(user_id)
    
    if user.zoho_token_expires_at < time.time():
        # Refresh
        new_tokens = await zoho_client.refresh_token(
            decrypt(user.zoho_refresh_token)
        )
        user.zoho_access_token = encrypt(new_tokens.access_token)
        user.zoho_token_expires_at = new_tokens.expires_in
        await db.save(user)
    
    return decrypt(user.zoho_access_token)
```

### 9.3 Google Drive OAuth 2.0 Integration

**Setup:**
1. Create OAuth 2.0 credentials in Google Cloud Console
2. Get Client ID and Client Secret
3. Configure redirect URI: `https://backend.example.com/auth/google/callback`

**Token Management:**
```python
@app.get("/auth/google/authorize")
async def google_authorize():
    # Request offline access for refresh token
    return RedirectResponse(google_auth_url)

@app.get("/auth/google/callback")
async def google_callback(code: str):
    token_response = await google_client.get_token(code)
    
    user = await db.get_user(zoho_user_id)
    user.google_refresh_token = encrypt(token_response.refresh_token)
    user.google_access_token = encrypt(token_response.access_token)
    await db.save(user)
    
    return RedirectResponse("/dashboard")

async def get_google_access_token(user_id: str):
    user = await db.get_user(user_id)
    
    if user.google_token_expires_at < time.time():
        new_tokens = await google_client.refresh_token(
            decrypt(user.google_refresh_token)
        )
        user.google_access_token = encrypt(new_tokens.access_token)
        await db.save(user)
    
    return decrypt(user.google_access_token)
```

### 9.4 Session Management

**Session Storage (Redis):**
```python
# Create session after OAuth
session_data = {
    'user_id': zoho_user_id,
    'email': user_email,
    'zoho_org_id': org_id,
    'permissions': ['view_dashboard', 'use_ai', ...],
    'auth_time': datetime.now(),
}
redis.set(f"session:{session_id}", json.dumps(session_data), ex=86400)

# Session verification middleware
@app.middleware("http")
async def verify_session(request: Request, call_next):
    session_id = request.cookies.get("session_id")
    if not session_id:
        return RedirectResponse("/login")
    
    session_data = redis.get(f"session:{session_id}")
    if not session_data:
        return RedirectResponse("/login")
    
    request.state.user = json.loads(session_data)
    response = await call_next(request)
    return response
```

### 9.5 Authorization Layers

**Role-Based Access Control (RBAC):**

| Role | Dashboard Access | Chatbot | Sync Logs | Settings |
|------|------------------|---------|-----------|----------|
| Admin | All data | All docs | All | Full |
| Manager | Team data | Team docs | Team | Partial |
| User | Own data | Own docs | Own | None |

**Document-Level Access:**
- Respect Zoho CRM record permissions (who can view that Account/Deal)
- Respect document sensitivity classifications
- Combine CRM permissions + sensitivity level

```python
async def can_user_access_document(user_id: str, document_id: str):
    doc = await db.get_document(document_id)
    user = await db.get_user(user_id)
    
    # Check CRM record permission
    crm_permission = await zoho_client.check_record_permission(
        user_id, doc.crm_module, doc.crm_record_id
    )
    if not crm_permission:
        return False
    
    # Check sensitivity level
    if doc.sensitivity_level == 'highly_confidential':
        return user.has_explicit_permission(doc.id)
    
    return True

# In chatbot retrieval
async def search_documents(query: str, user_id: str, scope: str):
    results = hybrid_search(query)
    
    # Filter by permission
    filtered = [
        doc for doc in results 
        if await can_user_access_document(user_id, doc.id)
    ]
    
    return filtered
```

### 9.6 Security Best Practices

**Token Security:**
- ✅ HTTPS only (TLS 1.2+)
- ✅ Tokens stored in encrypted backend database
- ✅ Never expose tokens in frontend JavaScript
- ✅ Use httponly cookies for session management
- ✅ Implement token rotation (refresh before expiry)
- ✅ Implement token revocation on logout

**Additional Security:**
- ✅ CSRF protection (state parameter in OAuth flow)
- ✅ Prevent clickjacking (X-Frame-Options header)
- ✅ Prevent XSS (Content-Security-Policy)
- ✅ Rate limiting on authentication endpoints
- ✅ Audit logging for sensitive operations
- ✅ Multi-tenant isolation (if applicable)

---

## 10. DOCUMENT SENSITIVITY & ACCESS CONTROL

### 10.1 Classification Framework

**Four-Level Sensitivity Model:**

| Level | Definition | AI Access | Examples |
|-------|-----------|-----------|----------|
| 🟢 **Public** | Shareable, no restrictions | Allowed | Product brochures, public announcements |
| 🔵 **Internal** | General business use | Authorized users | Internal reports, general procedures |
| 🟠 **Confidential** | Restricted, business-sensitive | Restricted users | Customer contracts, quotations, pricing |
| 🔴 **Highly Confidential** | Strictly restricted | Explicitly authorized only | Financial data, legal docs, strategic plans |

### 10.2 Classification Assignment

**Automatic Classification (on ingestion):**
```python
async def classify_document(file_name: str, content: str) -> str:
    # Keyword-based rules
    if any(keyword in file_name.lower() for keyword in 
           ['contract', 'agreement', 'quotation']):
        return 'confidential'
    
    if any(keyword in file_name.lower() for keyword in 
           ['financial', 'invoice', 'payroll']):
        return 'highly_confidential'
    
    if any(keyword in file_name.lower() for keyword in 
           ['product', 'spec', 'manual']):
        return 'internal'
    
    # Default
    return 'internal'
```

**Manual Override:**
- Admins can manually set sensitivity level
- Classification can be changed later if needed

### 10.3 Access Control Enforcement

**Permission Check:**
```python
async def verify_document_access(
    user_id: str,
    document_id: str
) -> bool:
    """
    Verify user can access document considering:
    1. CRM record permissions
    2. Document sensitivity
    3. Explicit permissions
    """
    doc = await db.get_document(document_id)
    user = await db.get_user(user_id)
    
    # Always check CRM record permission first
    can_access_record = await check_crm_permission(
        user_id, doc.crm_module, doc.crm_record_id
    )
    if not can_access_record:
        return False
    
    # Check sensitivity level
    if doc.sensitivity_level == 'public':
        return True
    elif doc.sensitivity_level == 'internal':
        return user.role in ['admin', 'manager', 'user']
    elif doc.sensitivity_level == 'confidential':
        return user.role in ['admin', 'manager'] or \
               user.id in doc.explicit_permissions
    elif doc.sensitivity_level == 'highly_confidential':
        return user.id in doc.explicit_permissions
    
    return False
```

### 10.4 AI Chatbot Behavior

**When User Requests Restricted Document:**

Scenario: User asks for a highly confidential document they can't access

```
User: "What are the financial projections for this deal?"

AI: "I found a document related to financial projections,
    but I cannot share it because you don't have access to 
    confidential financial documents.
    
    Contact your manager or document owner for access."

# The AI does NOT:
# - Reveal document name or contents
# - Explain why they don't have access (minimal info)
# - Show metadata about the document
```

### 10.5 Audit Logging for Sensitive Access

**Every sensitive document access is logged:**
```sql
INSERT INTO audit_logs (
  user_id,
  action,
  resource_type,
  resource_id,
  document_id,
  sensitivity_level,
  access_granted,
  reason,
  created_at
) VALUES (
  'user123',
  'document_accessed',
  'document',
  'doc456',
  'doc456',
  'highly_confidential',
  true,
  'admin_explicit_permission',
  NOW()
);
```

### 10.6 Configurable Retention & Archiving

**Sensitive Document Policies:**
- Auto-delete logs for sensitive docs after 90 days (configurable)
- Archive sensitive docs after 2 years (configurable)
- Require re-authentication for accessing archived sensitive docs
- Alert admins of unusual access patterns

---

## 11. OCR & IMAGE PROCESSING

### 11.1 Priority & Scope

**Priority:** HIGH (Phase 1 requirement)

**Rationale:**
- Real-world CRM attachments include scanned PDFs, receipts, invoices, contracts as images
- Without OCR, significant portion of documents would be unsearchable
- Users expect to ask questions about ALL document types

**Scope:**
- Scanned/image-based PDFs
- JPG, JPEG, PNG files
- Screenshots
- Business documents captured as images (invoices, receipts, forms)

### 11.2 OCR Implementation

**Technology:** Tesseract OCR (via Pytesseract)

**Setup:**
```python
import pytesseract
from PIL import Image
import pdf2image

# Convert PDF page to image and OCR
def ocr_pdf_page(pdf_path: str, page_num: int) -> str:
    images = pdf2image.convert_from_path(pdf_path, first_page=page_num, last_page=page_num)
    text = pytesseract.image_to_string(images[0], lang='eng')
    return text

# OCR from JPG/PNG
def ocr_image(image_path: str) -> str:
    image = Image.open(image_path)
    text = pytesseract.image_to_string(image, lang='eng')
    return text
```

### 11.3 OCR Workflow

**For Image-Based PDFs:**
```
Scanned PDF
  ↓
1. Detect if PDF is image-based or text-based
   (Try extracting text; if empty, it's image-based)
  ↓
2. Convert PDF to images (pdf2image)
  ↓
3. For each page:
   - Run Tesseract OCR
   - Extract text, confidence score
   - Preserve page metadata
  ↓
4. Combine all pages
  ↓
5. Clean and normalize OCR output
  ↓
6. Index as searchable text
```

**For Images (JPG, PNG):**
```
Image File
  ↓
1. Run Tesseract OCR
  ↓
2. Extract text + confidence
  ↓
3. Detect if image contains:
   - Table/structured data
   - Handwriting
   - Form fields
  ↓
4. Extract structured data if detected
  ↓
5. Clean and normalize
  ↓
6. Index
```

### 11.4 Quality & Confidence Scoring

**OCR Confidence Tracking:**
```python
import pytesseract
import re

def ocr_with_confidence(image):
    # Get OCR with confidence data
    data = pytesseract.image_to_data(image, output_type=Output.DICT)
    
    # Calculate average confidence
    confidences = [int(conf) for conf in data['conf'] if int(conf) > 0]
    avg_confidence = sum(confidences) / len(confidences) if confidences else 0
    
    return {
        'text': pytesseract.image_to_string(image),
        'confidence': avg_confidence,
        'word_confidences': confidences
    }

# Store confidence score in document_chunks
if ocr_result['confidence'] < 60:
    # Flag for manual review
    chunk.metadata['ocr_confidence_low'] = True
    chunk.metadata['ocr_confidence_score'] = ocr_result['confidence']
```

**User Notification:**
- When chatbot retrieves low-confidence OCR text, append note:
  ```
  "Note: This information was extracted from a scanned document 
   with moderate confidence (65%). Please verify the accuracy."
  ```

### 11.5 Structured Data Extraction

**Phase 1:** Extract plain OCR text
**Phase 2:** Detect and extract tables, forms, structured data

Example Phase 2:
```python
# Detect table structure
def detect_tables(image):
    # Use OpenCV + table detection
    tables = table_detector.detect(image)
    
    for table in tables:
        # Extract table data
        rows, cols = extract_table_structure(table)
        # Convert to CSV/dict format
    
    return tables
```

### 11.6 Example OCR Workflow

**User uploads:** `invoice_scan_2026-09-04.pdf` (scanned image-based PDF)

**System processes:**
1. Detects PDF is image-based
2. Converts to images (10 pages)
3. Runs OCR on each page
4. Extracts text: "Invoice INV-2026-1045, Amount: ₹2,45,000, Date: Sep 4, 2026"
5. Chunks text
6. Generates embeddings
7. Indexes in PostgreSQL + pgvector

**User asks:** "What is the invoice amount?"
**AI finds:** Invoice document via semantic search
**AI answers:** "The invoice amount is ₹2,45,000."

---

## 12. WEB TAB UI/UX STRUCTURE

### 12.1 Overall Layout Architecture

**Tab-Based Navigation:**
```
┌─────────────────────────────────────────────────────┐
│  Zoho CRM Web Tab: Document Intelligence Widget    │
├─────────────────────────────────────────────────────┤
│                                                      │
│  [📊 Dashboard] [💬 Chatbot] [📋 Sync Logs] [⚙️ Settings]
│                                                      │
│ ┌────────────────────────────────────────────────┐ │
│ │                                                 │ │
│ │         [Active Tab Content]                   │ │
│ │                                                 │ │
│ │         (Dashboard / Chatbot / etc.)            │ │
│ │                                                 │ │
│ └────────────────────────────────────────────────┘ │
│                                                      │
└─────────────────────────────────────────────────────┘
```

**Tabs:**

1. **Dashboard** (default)
   - Real-time KPIs, charts, analytics
   - Sync health, file statistics
   - Recent activity
   - Filters and drill-down

2. **AI Chatbot**
   - Conversation interface
   - Document search
   - File retrieval and Q&A

3. **Sync Logs**
   - Detailed sync history
   - Failed syncs with error messages
   - Manual retry options
   - Timestamps and durations

4. **Settings**
   - Integration configuration
   - Sync preferences
   - Classification rules
   - Account settings

### 12.2 Dashboard Layout

**Visual Grid Structure:**
```
┌─────────────────────────────────────────────────────┐
│  Last updated: 10:42 AM  [↻ Refresh]                │
├─────────────────────────────────────────────────────┤
│                                                      │
│  ┌──────────────┐ ┌──────────────┐ ┌─────────────┐ │
│  │ Attachments  │ │ Synced       │ │ Failed      │ │
│  │  1,247       │ │ 958          │ │ 100         │ │
│  └──────────────┘ └──────────────┘ └─────────────┘ │
│                                                      │
│  ┌───────────────────────────────────────────────┐  │
│  │  Sync Health Gauge: 76.8% ✓                  │  │
│  │  [████████░] - Great                          │  │
│  └───────────────────────────────────────────────┘  │
│                                                      │
│  ┌──────────────────────┐  ┌────────────────────┐   │
│  │ Sync Trend (7 days)  │  │ File Type Dist.    │   │
│  │ [Animated Line Chart]│  │ [Interactive Pie]  │   │
│  └──────────────────────┘  └────────────────────┘   │
│                                                      │
│  ┌──────────────────────┐  ┌────────────────────┐   │
│  │ Module Stats         │  │ Recent Activity    │   │
│  │ [Bar Chart]          │  │ [Activity List]    │   │
│  └──────────────────────┘  └────────────────────┘   │
│                                                      │
│  ┌───────────────────────────────────────────────┐  │
│  │ Failed Syncs & Non-Synced Files               │  │
│  │ [Detailed Table with Drill-down]              │  │
│  └───────────────────────────────────────────────┘  │
│                                                      │
└─────────────────────────────────────────────────────┘
```

**Key Sections:**

1. **Top Bar**
   - Last updated timestamp
   - Refresh button
   - Date range filter
   - Module/file type filters

2. **KPI Cards (Row 1)**
   - Total Attachments
   - Synced Files
   - Failed Syncs
   - Non-Synced Files

3. **Sync Health Gauge**
   - Animated circular gauge
   - Success rate percentage
   - Visual feedback (green/yellow/red)

4. **Trend Charts (Row 2)**
   - Sync trend line chart (7/30/90 days)
   - File type distribution pie chart

5. **Module Stats & Activity (Row 3)**
   - Module-wise breakdown bar chart
   - Recent sync activity timeline

6. **Failed & Non-Synced Details (Row 4)**
   - Expandable table
   - Error messages
   - Retry options
   - Size and age information

### 12.3 Chatbot Layout

```
┌─────────────────────────────────────────────────────┐
│  AI Document Assistant                              │
├─────────────────────────────────────────────────────┤
│                                                      │
│  Search scope: [Current Record ▼]                   │
│    ● Current Record                                 │
│    ○ Current Module                                 │
│    ○ Entire Organization                           │
│                                                      │
├─────────────────────────────────────────────────────┤
│                                                      │
│  ┌─────────────────────────────────────────────┐   │
│  │ Chat History                                 │   │
│  │                                              │   │
│  │ AI: Hello! I can help you search and       │   │
│  │     analyze your documents...                │   │
│  │                                              │   │
│  │ You: Find the quotation for ABC Ltd        │   │
│  │                                              │   │
│  │ AI: I found 3 quotations:                  │   │
│  │     1. quotation_ABC_2026-08.pdf...         │   │
│  │     [with responses and file links]         │   │
│  │                                              │   │
│  └─────────────────────────────────────────────┘   │
│                                                      │
│  ┌─────────────────────────────────────────────┐   │
│  │ Ask anything about your documents...         │   │
│  │ [Text Input Field]              [Send ➤]     │   │
│  └─────────────────────────────────────────────┘   │
│                                                      │
└─────────────────────────────────────────────────────┘
```

**Features:**
- Scope selector (Current Record / Org-wide)
- Scrollable chat history
- AI response with source file links
- Text input with send button
- Quick action buttons ("Summarize this deal's files", etc.)

### 12.4 Sync Logs Layout

```
┌─────────────────────────────────────────────────────┐
│  Synchronization History                            │
├─────────────────────────────────────────────────────┤
│                                                      │
│  Filters: [Module ▼] [Status ▼] [Date ▼] [Search]  │
│                                                      │
│  ┌──────────────────────────────────────────────┐  │
│  │ File Name    │ Module │ Status  │ Time │ Act│  │
│  ├──────────────────────────────────────────────┤  │
│  │ quotation... │ Deals  │ ✅ Sync │10am │ ↗  │  │
│  │ invoice...   │ Invoic │ ❌ Fail │ 9am │⟲ ↗ │  │
│  │ contract...  │ Accou  │⏳ Pend  │ 8am │ ↗  │  │
│  │ ...          │ ...    │ ...     │ ... │... │  │
│  └──────────────────────────────────────────────┘  │
│                                                      │
│  Detail view on click:                              │
│  ┌──────────────────────────────────────────────┐  │
│  │ File: quotation_ABC_2026-08.pdf              │  │
│  │ Module: Deals | Record: ABC Deal #123        │  │
│  │ Size: 245 KB | Synced at: 10:42 AM          │  │
│  │ Duration: 2.3 seconds                        │  │
│  │ Google Drive: [Link] | CRM: [Link]          │  │
│  └──────────────────────────────────────────────┘  │
│                                                      │
└─────────────────────────────────────────────────────┘
```

**Failed Sync Details:**
```
┌──────────────────────────────────────────────────┐
│ ❌ Failed Sync Details                            │
├──────────────────────────────────────────────────┤
│                                                   │
│ File: invoice_scan_2026-09-04.pdf                │
│ Error Code: API_RATE_LIMIT_EXCEEDED              │
│ Message: "Zoho API rate limit reached..."        │
│ Last Attempt: 2026-09-04 14:22:15                │
│ Retry Count: 2 of 5                              │
│ Next Retry: 2026-09-04 14:30:00 (in 5 min)      │
│                                                   │
│ [Manual Retry] [Skip] [Delete]                   │
│                                                   │
└──────────────────────────────────────────────────┘
```

### 12.5 Settings Layout

```
┌─────────────────────────────────────────────────────┐
│  Widget Settings                                    │
├─────────────────────────────────────────────────────┤
│                                                      │
│  Sync Configuration                                 │
│  ├─ Sync Frequency: [Every 15 min ▼]               │
│  ├─ Auto-Retry Failed: [ON/OFF]                    │
│  ├─ Max Retry Count: [5]                           │
│  └─ Retry Delay: [5 minutes ▼]                     │
│                                                      │
│  Document Settings                                 │
│  ├─ Auto-Classify Docs: [ON/OFF]                   │
│  ├─ Enable OCR: [ON/OFF]                           │
│  └─ OCR Languages: [English, Hindi ▼]              │
│                                                      │
│  AI Chatbot Settings                               │
│  ├─ Response Length: [Medium ▼]                    │
│  ├─ Include Sources: [ON/OFF]                      │
│  └─ Confidence Threshold: [0.7]                    │
│                                                      │
│  Integration Status                                │
│  ├─ Zoho CRM: ✅ Connected                         │
│  ├─ Google Drive: ✅ Connected                     │
│  ├─ OpenAI: ✅ Connected                           │
│  └─ [Re-authorize All]                             │
│                                                      │
│  Data & Privacy                                    │
│  ├─ Audit Logs: [View]                             │
│  ├─ Data Retention: [90 days ▼]                    │
│  └─ [Clear Cache] [Reset Widget]                   │
│                                                      │
└─────────────────────────────────────────────────────┘
```

### 12.6 Dashboard Refresh Strategy

**Auto-Refresh Logic:**
```
On Page Load
  ↓
Fetch latest KPIs from PostgreSQL
  ↓
Display dashboard with data
  ↓
Set timer for auto-refresh (30–60 seconds)
  ↓
Every 30-60 seconds:
  ├─ Fetch latest sync counts
  ├─ Update KPI cards (if changed)
  ├─ Update recent activity list
  └─ Animate transitions
  ↓
When sync job completes (via WebSocket/polling):
  ├─ Update related metrics immediately
  └─ Show animation/notification
  ↓
When user clicks "Refresh":
  ├─ Force immediate fetch
  ├─ Show loading indicator
  └─ Update all metrics
```

**Important:** Dashboard refresh queries PostgreSQL, NOT Zoho/GDrive APIs, for fast performance.

---

## 13. AUDIT & LOGGING REQUIREMENTS

### 13.1 Chatbot Interaction Logging

**Every chatbot query must be logged with:**

```sql
INSERT INTO chat_messages (
  id,
  session_id,
  user_id,
  role,              -- 'user' or 'assistant'
  content,           -- the message text
  intent,            -- search, summarize, extract, etc.
  scope,             -- current_record, org_wide
  retrieved_document_ids,    -- [doc1_id, doc2_id, ...]
  retrieval_scores,          -- [0.89, 0.76, ...]
  retrieval_method,          -- semantic, keyword, metadata
  ai_model,                  -- gpt-4-turbo
  tokens_used,               -- prompt + completion tokens
  response_time_ms,          -- latency in milliseconds
  error_occurred,            -- true/false
  error_message,             -- if error
  user_feedback,             -- helpful, not_helpful, neutral (optional)
  created_at
);
```

### 13.2 Document Access Logging

**When a document is accessed via AI or dashboard:**

```sql
INSERT INTO audit_logs (
  user_id,
  action,                  -- 'document_accessed'
  resource_type,           -- 'document'
  resource_id,             -- document_id
  context,                 -- 'chatbot_query', 'dashboard_view', 'file_download'
  access_granted,          -- true/false
  reason_denied,           -- if access denied
  document_sensitivity,
  created_at
);
```

### 13.3 Synchronization Logging

**Every sync event:**

```sql
INSERT INTO sync_logs (
  -- [all sync metadata as defined in section 6.2]
  user_id,                 -- who triggered/initiated
  sync_duration,           -- how long it took
  file_size_synced,        -- total bytes
  error_count,             -- if partial failure
  created_at
);
```

### 13.4 Analytics & Insights

**Dashboard Analytics from Logs:**

```python
# Total AI queries
SELECT COUNT(*) FROM chat_messages WHERE created_at > DATE_SUB(NOW(), INTERVAL 30 DAY)

# Most common questions
SELECT content, COUNT(*) as frequency 
FROM chat_messages 
WHERE role = 'user' 
GROUP BY content 
ORDER BY frequency DESC 
LIMIT 10

# Documents accessed most frequently
SELECT document_id, COUNT(*) as access_count
FROM audit_logs
WHERE action = 'document_accessed'
GROUP BY document_id
ORDER BY access_count DESC

# Successful vs failed queries
SELECT 
  CASE WHEN error_occurred THEN 'failed' ELSE 'successful' END as status,
  COUNT(*) as count,
  AVG(response_time_ms) as avg_response_ms
FROM chat_messages
GROUP BY status

# AI usage by module
SELECT crm_module, COUNT(*) as query_count
FROM chat_messages
GROUP BY crm_module
ORDER BY query_count DESC

# Sync success rate by module
SELECT 
  crm_module,
  COUNT(*) as total_syncs,
  SUM(CASE WHEN sync_status = 'synced' THEN 1 ELSE 0 END) as successful,
  ROUND(SUM(CASE WHEN sync_status = 'synced' THEN 1 ELSE 0 END) * 100.0 / COUNT(*), 2) as success_rate
FROM sync_logs
GROUP BY crm_module
```

### 13.5 Privacy & Data Minimization

**In audit logs, DO NOT store:**
- ❌ Full document contents
- ❌ Sensitive data extracted from documents
- ❌ Personal information (names, emails) unless necessary
- ❌ Passwords or API keys

**Store instead:**
- ✅ Document ID, file name, file type
- ✅ CRM record reference
- ✅ Access decision (allowed/denied)
- ✅ Query intent (not the full query if sensitive)
- ✅ Retrieval confidence scores

**Retention Policies:**
- Standard logs: 90 days
- Sensitive document access: 180 days
- Authentication logs: 1 year
- Configurable per organization

---

## 14. INITIAL DEVELOPMENT SCOPE (MVP)

### Phase 1: Core Features (Months 1–3)

**Backend Infrastructure:**
- [ ] FastAPI project setup
- [ ] PostgreSQL + pgvector database
- [ ] Zoho OAuth 2.0 integration
- [ ] Google OAuth 2.0 integration
- [ ] Session management

**Dashboard Module:**
- [ ] KPI card calculations
- [ ] Sync statistics queries
- [ ] Recent activity retrieval
- [ ] Dashboard API endpoints
- [ ] Basic charts (bar, pie, line)
- [ ] Filters and drill-down logic
- [ ] Auto-refresh mechanism

**AI Chatbot Module:**
- [ ] Document ingestion pipeline
- [ ] Text extraction (PDFs, DOCX, TXT)
- [ ] OCR for images and scanned PDFs
- [ ] Text chunking and embedding generation
- [ ] pgvector similarity search
- [ ] Hybrid retrieval (semantic + keyword)
- [ ] OpenAI LLM integration
- [ ] Chat session management
- [ ] Query logging

**Frontend (Web Tab):**
- [ ] React-based tab interface
- [ ] Dashboard visualization components
- [ ] Chatbot UI
- [ ] Sync logs display
- [ ] Settings page
- [ ] OAuth redirect handling
- [ ] Session/auth state management

**Integrations:**
- [ ] Zoho CRM API (read attachments, queries)
- [ ] Google Drive API (list/download files)
- [ ] OpenAI API (embeddings + LLM)
- [ ] Zoho Custom Module CRUD (sync logs)

**Testing & Deployment:**
- [ ] Unit tests (backend)
- [ ] Integration tests
- [ ] AWS setup (App Runner)
- [ ] Monitoring and logging
- [ ] Security audit

### Phase 2: Enhancements (Months 4–6)

- [ ] Organization-wide search toggle in chatbot
- [ ] Advanced analytics dashboard
- [ ] Document sensitivity classification (automatic + manual)
- [ ] Improved OCR and table extraction
- [ ] Multi-file reasoning and comparison
- [ ] User feedback mechanism
- [ ] Better response formatting and citations
- [ ] Caching layer optimization
- [ ] Celery background tasks for heavy processing

### Phase 3: Advanced Features (Months 7–9)

- [ ] Handwriting OCR
- [ ] Complex layout understanding
- [ ] Confidence scoring and credibility indicators
- [ ] Document recommendations
- [ ] Predictive analytics
- [ ] Cross-module document linking
- [ ] Advanced permission management
- [ ] Custom classification rules
- [ ] Scheduled reports and digest emails

### Success Criteria for MVP

✅ Dashboard displays real-time sync KPIs with visually impressive charts
✅ AI chatbot successfully retrieves and answers questions about documents
✅ Users can search current record or opt into organization-wide
✅ OCR extracts text from scanned documents and makes them searchable
✅ Permission controls prevent unauthorized access
✅ Audit logs track all interactions
✅ System handles 1000+ documents without performance degradation
✅ Average AI query response time < 3 seconds
✅ Synchronization success rate > 95%

---

## 15. TECHNICAL ARCHITECTURE DIAGRAM

```
┌────────────────────────────────────────────────────────────────┐
│                     End User (Browser)                         │
│                   Zoho CRM → Web Tab                           │
└───────────────────────┬────────────────────────────────────────┘
                        │ HTTPS
                        ▼
        ┌───────────────────────────────────┐
        │   Zoho CRM Web Tab Frontend        │
        │  ┌─────────────────────────────┐  │
        │  │ ├─ Dashboard Tab            │  │
        │  │ ├─ Chatbot Tab              │  │
        │  │ ├─ Sync Logs Tab            │  │
        │  │ └─ Settings Tab             │  │
        │  └─────────────────────────────┘  │
        │  (React, State Management)        │
        └───────────────────┬───────────────┘
                            │ API Calls
                            ▼
        ┌────────────────────────────────────────────────┐
        │         FastAPI Backend (Python)               │
        │         Running on AWS                         │
        │                                                 │
        │  ┌──────────────────────────────────────────┐ │
        │  │ API Routes & Endpoints                   │ │
        │  ├─ Authentication (Zoho/Google OAuth)     │ │
        │  ├─ Dashboard APIs                         │ │
        │  ├─ Chatbot APIs                           │ │
        │  ├─ Document Processing APIs               │ │
        │  └─ Settings APIs                          │ │
        │  └──────────────────────────────────────────┘ │
        │                    │                           │
        │  ┌─────────────────┼─────────────────┐        │
        │  │                 │                 │        │
        │  ▼                 ▼                 ▼        │
        │ ┌──────────┐  ┌─────────┐  ┌──────────────┐ │
        │ │Middleware│  │Routers  │  │Background   │ │
        │ │Auth      │  │Logic    │  │Tasks (Celery│ │
        │ │Logging   │  │RAG      │  │+Redis)      │ │
        │ │Security  │  │Retrieval│  │             │ │
        │ └──────────┘  └─────────┘  └──────────────┘ │
        │                                                 │
        └────┬─────────────────────────────────────┬───┘
             │                                     │
             │ (via OAuth 2.0 tokens)              │ (background jobs)
             ▼                                     ▼
    ┌──────────────────┐                    ┌─────────────┐
    │ External APIs    │                    │Redis Queue  │
    │                  │                    │Celery       │
    │ ├─Zoho CRM API   │                    │             │
    │ ├─Google Drive   │                    └─────────────┘
    │ └─OpenAI API     │
    └──────────┬───────┘
               │
    ┌──────────┴──────────────────────────────────────┐
    │                                                 │
    ▼                                                 ▼
┌────────────────────┐                        ┌────────────────────┐
│  AWS RDS           │                        │  AWS ElastiCache   │
│  PostgreSQL        │                        │  Redis             │
│                    │                        │                    │
│ ├─sync_logs        │                        │ ├─Sessions         │
│ ├─documents        │                        │ ├─Caches           │
│ ├─document_chunks  │                        │ ├─Job Queue        │
│ │  (+ embeddings)  │                        │ └─Rate Limiting    │
│ ├─chat_sessions    │                        │                    │
│ ├─chat_messages    │                        └────────────────────┘
│ ├─audit_logs       │
│ └─integration_settings
│                    │
│ Extensions:        │
│ ├─pgvector (for    │
│ │  vector search)  │
│ └─uuid-ossp        │
│                    │
└────────────────────┘
         │
         │ (Semantic Search via pgvector)
         │
    ┌────▼────────────────────────────────────────┐
    │ Vector Search (pgvector extension)          │
    │ OpenAI Embeddings (1536-dimensional)        │
    │ Cosine Similarity Search on document_chunks │
    └─────────────────────────────────────────────┘

External Services (APIs):
┌──────────────────────────────────────────────────────────────┐
│  Zoho CRM API     │  Google Drive  │  OpenAI API             │
│                  │                │                         │
│ ├─Attachments    │ ├─File listing │ ├─text-embedding-3-*   │
│ ├─Records        │ ├─Download     │ ├─gpt-4-turbo          │
│ ├─OAuth token    │ ├─Upload       │ └─Token management     │
│ └─Metadata       │ └─Folder ops   │                         │
└──────────────────────────────────────────────────────────────┘
```

---

## 16. DEVELOPMENT ROADMAP & NEXT STEPS

### Phase 0: Planning & Design (Current)

**Activities:**
- ✅ Requirements gathering (THIS DOCUMENT)
- ⏭️ Detailed data schema design
- ⏭️ API endpoint specification
- ⏭️ UI/UX mockups
- ⏭️ Security & OAuth flow diagrams
- ⏭️ Document processing pipeline design
- ⏭️ Cost estimation

**Deliverables:**
- Requirements document (✅ done)
- Data schema ERD
- API specification (OpenAPI/Swagger)
- UI mockups (Figma)
- Architecture diagrams
- Security checklist

### Phase 1: MVP Development (Months 1–3)

**Sprint 1: Backend Setup**
- FastAPI project structure
- PostgreSQL + pgvector setup
- Zoho & Google OAuth
- Initial API routes

**Sprint 2: Dashboard API**
- KPI endpoints
- Sync statistics queries
- Chart data endpoints
- Filtering and aggregation

**Sprint 3: AI Chatbot Backend**
- Document ingestion pipeline
- Text extraction & OCR
- Embedding generation
- RAG retrieval endpoints

**Sprint 4: Frontend Development**
- React components
- Tab navigation
- Dashboard visualizations
- Chatbot UI

**Sprint 5: Integration & Testing**
- End-to-end testing
- Performance optimization
- Security hardening
- AWS deployment

### Phase 2: Enhancement (Months 4–6)

- Org-wide search
- Advanced analytics
- Document classification
- Better OCR
- Feedback mechanism

### Phase 3: Advanced (Months 7–9)

- Handwriting OCR
- Confidence scoring
- Document recommendations
- Custom rules
- Email reports

---

## 17. SUCCESS METRICS & KPIs

### Dashboard KPIs

- **Sync Health:** > 95% success rate
- **Performance:** Dashboard loads in < 2 seconds
- **Accuracy:** Sync metrics match actual file counts
- **Availability:** > 99.5% uptime

### AI Chatbot KPIs

- **Response Time:** < 3 seconds for 95% of queries
- **Accuracy:** > 90% of answers are correct/helpful
- **Retrieval Precision:** Top-k documents contain relevant information > 85% of the time
- **User Satisfaction:** > 4/5 stars (if feedback collected)

### Adoption KPIs

- **Active Users:** Target 80% of team using widget within 3 months
- **Query Volume:** Average 10+ AI queries per user per week
- **Dashboard Views:** Dashboard viewed > 100 times/day

---

## 18. COMPLIANCE & SECURITY

### Data Protection

- ✅ GDPR compliance (if EU users)
- ✅ Data encryption at rest and in transit
- ✅ Regular security audits
- ✅ PII data minimization in logs

### API Security

- ✅ OAuth 2.0 for all integrations
- ✅ HTTPS/TLS 1.2+
- ✅ Rate limiting
- ✅ Request signing/validation
- ✅ CORS configuration

### Audit & Compliance

- ✅ Complete audit trail of all document access
- ✅ User activity logging
- ✅ Admin dashboards for compliance
- ✅ Data retention policies
- ✅ Export capabilities for compliance

---

## 19. DOCUMENT INFORMATION

**Title:** Zoho CRM Web Tab Widget — Comprehensive Requirements Document  
**Version:** 1.0  
**Date:** September 4, 2026  
**Status:** Requirements Finalized, Ready for Design Phase  
**Prepared By:** Karthick  
**Next Review:** Upon completion of Phase 0 deliverables

---

## 20. APPENDIX: QUICK REFERENCE

### Key Technology Choices

| Component | Technology | Rationale |
|-----------|-----------|-----------|
| Frontend | React + TypeScript | Modern, component-based, strong Zoho compatibility |
| Backend API | Python + FastAPI | AI/ML ecosystem, async support, fast development |
| Database | PostgreSQL + pgvector | Relational + vector search in one database |
| Vector DB | pgvector extension | Integrated with PostgreSQL, simple infrastructure |
| LLM | OpenAI (GPT-4) | Strong reasoning, embeddings, production-grade |
| Caching | Redis | Session storage, cache layer, job coordination |
| Job Queue | Celery + Redis | Background processing, retries, scheduling |
| Hosting | AWS | ECS/Fargate, RDS, ElastiCache, S3 |
| OCR | Tesseract | Open-source, reliable, good quality |
| PDF Processing | PyPDF2 + pdfplumber | Python libraries, good text extraction |

### API Endpoints (Preview)

```
Dashboard:
GET  /api/dashboard/kpis
GET  /api/dashboard/sync-trends
GET  /api/dashboard/file-type-stats
GET  /api/dashboard/module-stats
GET  /api/dashboard/recent-activity
GET  /api/dashboard/failed-syncs
GET  /api/dashboard/non-synced-files

Chatbot:
GET  /api/chat/sessions
POST /api/chat/messages
GET  /api/chat/search
GET  /api/chat/retrieve-document

Documents:
POST /api/documents/ingest
POST /api/documents/index
GET  /api/documents/list

Settings:
GET  /api/settings/sync-config
PUT  /api/settings/sync-config
GET  /api/settings/integration-status
POST /api/settings/reconnect-oauth
```

### Common Questions

**Q: Will this replace Zoho's native attachment storage?**
A: No. The widget provides analytics and AI on top of existing attachments and Drive sync.

**Q: What if sync fails between CRM and Drive?**
A: The existing sync integration handles retries. The widget shows failed syncs and provides manual retry.

**Q: Can we use a different LLM provider?**
A: Yes. The architecture uses a provider abstraction layer, so Claude, Gemini, or Zia can be added later.

**Q: How large can files be?**
A: Depends on Zoho's limits. OCR/embedding takes longer for large PDFs, but should work for typical business documents.

**Q: Is the AI data private?**
A: Yes. Documents are indexed in your backend (PostgreSQL). OpenAI sees only the text sent for embedding/LLM, which is handled securely.

---

**END OF REQUIREMENTS DOCUMENT**
