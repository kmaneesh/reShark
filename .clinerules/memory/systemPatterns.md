# System Patterns

## System architecture

1. **Storage (File System)**
   - PCAP repository
   - Notebook (JSON/Markdown)
   - Rulebook (Python/YAML grammars)
   - Cookbook (Markdown documentation)
   - Analysis logs and archives

2. **Execution (VSCode + Dev Container)**
   - Direct Python execution
   - Interactive debugging
   - Reproducible dev environment
   - Manual orchestration scripts
   - Direct tool access (tshark, scapy)

3. **Intelligence (Scopes)**
   - Observer: Measures and detects patterns
   - Theorist: Generates hypotheses
   - Validator: Tests and falsifies
   - Archivist: Manages memory

## Key technical decisions
- Use of containerized development environment for consistency.
- Utilization of tshark, Zeek, and scapy for PCAP processing and manipulation.
- Statistical analysis with numpy, scipy, and pandas.
- Hypothesis generation and validation using test suites.

## Design patterns in use
- Observer pattern for data collection and monitoring.
- Theorist pattern for hypothesis generation based on collected data.
- Validator pattern for testing hypotheses against data.
- Archivist pattern for managing memory and persistence of analysis results.

## Component relationships
- **Scopes**:
  - **Observer**: Measures and detects patterns in PCAP data.
  - **Theorist**: Generates hypotheses based on Observer's findings.
  - **Validator**: Tests hypotheses using test suites.
  - **Archivist**: Manages Notebook, Rulebook, and Cookbook.

## Critical implementation paths
- Phase 1 focuses on manual execution and debugging within VSCode + Dev Container.
- Phase 2 introduces autonomous execution with OpenHands and LangGraph for orchestration.
