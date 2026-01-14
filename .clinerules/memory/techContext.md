# Tech Context

## Technologies used
- **Programming Languages**: Python 3.11+
- **Tools**:
  - tshark, Zeek (PCAP dissection)
  - scapy (PCAP manipulation)
  - numpy, scipy, pandas (statistical analysis)
  - pytest (validation testing)

## Development setup
- **Environment**: VSCode + Dev Container
- **Containerization**: Docker 24+
- **Version Control**: Git with Conventional Commits
- **Dependency Management**: Poetry for Python

## Technical constraints
- System MUST have sufficient memory for concurrent PCAP processing.
- Python 3.11+ required.
- Docker 24+ required.
- OpenHands version compatibility TBD during implementation.

## Dependencies
- **Phase 1**:
  - OpenHands framework for execution environment.
  - Docker for container orchestration.
- **Phase 2**:
  - LangGraph for orchestration.
  - Qdrant for vector similarity.

## Tool usage patterns
- Direct Python access to `tshark`, `scapy`, `numpy`, `scipy`, `pandas`.
- Tools executed in containerized environment (dev container for Phase 1, Docker for Phase 2).
- All tool invocations and outputs are logged to Notebook.
- Tool execution failures are handled gracefully.
- Tool outputs are validated before use in hypotheses.
