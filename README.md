SONDERBYTE: Aggregate ⬛🟩

"We don't build scripts to read files. We build logic gates to filter mud."

1. The Operational Context

The modern Small-to-Medium Business (SMB) ecosystem is plagued by the SaaS Archipelago—a fragmented landscape where critical financial data is locked inside vendor platforms (like QuickBooks Online). When users export this data, vendors provide heavily formatted, human-readable CSVs filled with metadata, blank columns, and timestamps. We refer to this as "The Mud."

SonderByte: Aggregate is a Sovereign Middleware Protocol designed to ingest this chaotic data, sanitize it, and structure it for advanced predictive analytics.

This specific repository houses the core Aggregate Engine, starting with the Data Airlock—the secure intake manifold that protects the mathematical core from operating system friction and corrupted data streams.

2. Architectural Philosophy

This system actively rejects the "Fragile Bricklayer" approach (hardcoding row numbers and assuming perfect data) in favor of a "Sovereign Architect" methodology.

Decoupled Intake: The Airlock (validate_local_file) knows nothing about Profit & Loss math. It only validates file existence, clears OS-level file locks (e.g., files left open in Excel), and cascades through text encodings.

The Semantic Filter: The Engine (get_input_file) does not count rows. It operates as a "Hunter," utilizing try/except mathematical gates to actively search for numbers while silently incinerating SaaS metadata headers and footers.

The Biological Constant: The system expects human error. If a user inputs january_data instead of january_data.csv, the command prompt silently appends the extension and routes the path to the correct /Data_Input directory.

3. Pipeline Topography

(Note: GitHub natively renders this diagram)

graph TD
    %% Theme
    classDef default fill:#000,stroke:#00ff41,stroke-width:2px,color:#00ff41;
    classDef error fill:#330000,stroke:#ff0000,stroke-width:2px,color:#ff0000;
    
    A([User CLI Input]) --> B{Smart Router}
    B -->|Appends .csv & Locates| C(The Airlock: validate_local_file)
    
    C --> D{OS Diagnostics}
    D -->|Missing/Excel Lock| E[Reject Payload]:::error
    D -->|Verified| F{Encoding Cascader}
    
    F -->|UTF-8 / CP1252| G(The Engine: get_input_file)
    F -->|Corrupted Bytes| E
    
    G --> H{Semantic Gate}
    H -->|Text/Metadata| I[Incinerate Noise]
    H -->|Valid Floats| J[(Structured Memory Array)]


4. The Ignition Protocol

This system relies strictly on the Python Standard Library (os, csv, io). Zero external dependencies or bloated virtual environments are required for the core ingestion layer.

1. Clone the Vault:

Currently not Available for Public.


2. Prepare the Environment:
Ensure you have a directory named Data_Input in the root folder, containing your target QBO CSV exports.

3. Engage the Engine:

python local_airlock.py


Follow the Commander Prompt in the terminal. You can type the exact file path, or simply type the name of the file (e.g., january_report), and the Smart Router will handle the rest.

5. Future Roadmap

Phase 1 (In Progress): Local File Airlock and Semantic Filtering.

Phase 2 (Pending): Integration of the mathematical engine to aggregate margins and identify target anchors across multiple time series.

Phase 3 (Pending): Connecting the output JSON stream to the predictive SLA forecasting module.
