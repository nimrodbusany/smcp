# S-MCP - Semantic Model Context Protocol

**A community initiative to add semantic understanding to Model Context Protocol (MCP) services.**

## Vision

We're building an open protocol that extends [Model Context Protocol](https://modelcontextprotocol.io) with ontology-based semantic annotations. Our goal: enable LLM agents to understand what services actually do through formal semantics.

## The Problem

Current LLM-to-service interactions rely on natural language descriptions:
- Services are discovered by name matching
- Parameters are understood through documentation
- No formal understanding of data relationships

## Our Approach

SMCP will add semantic layers to MCP:
- **Ontology Bindings**: Map services to domain ontologies (Gene Ontology, Schema.org, FHIR, etc.)
- **Semantic Discovery**: Find services by capability, not just keywords
- **Data Understanding**: Connect service data to formal concepts
- **Cross-domain Interoperability**: Enable services from different domains to work together

## Core Principles

Our design principles emerge from extensive analysis of successful and failed standardization efforts across semantic web services, data integration protocols, and modern API ecosystems:

### 1. **Extend, Don't Replace**
Following MCP's integration with existing tools, SMCP adds semantic annotations without breaking compatibility. Your MCP services continue to work exactly as before - semantics are purely additive.

### 2. **Pragmatic Design**
We learned from the complexity that hindered OWL-S and WSMO adoption. SMCP prioritizes practical implementation over theoretical completeness. If it doesn't help LLMs make better decisions, it doesn't belong in the protocol.

### 3. **Implementation-First**
Rather than designing in abstract, we're starting with concrete examples like Gene Ontology bindings. Real use cases drive the specification, not the other way around.

### 4. **Progressive Enhancement**
Inspired by web standards, semantic complexity is optional and progressive:
- Level 0: Standard MCP (zero changes required)
- Level 1: Basic type annotations  
- Level 2: Full semantic bindings
- Level 3: Reasoning and inference

### 5. **Dual-Layer Architecture**
Learning from R2RML's success in database mapping:
- **Meta-level bindings**: Service functions → Ontological operations
- **Data-level bindings**: Service data → Domain concepts

### 6. **Lightweight by Default**
Adopting Hydra's philosophy: the simplest useful semantic annotation should be trivial to add. Complexity is available but not required.

### 7. **Transformation-Ready**
Borrowing SAWSDL's lifting/lowering concepts to bridge between MCP's JSON world and semantic representations. Automatic where possible, customizable where needed.

## Why These Principles Matter

Our research revealed that successful protocols share common patterns:
- **Separation of concerns** (transport vs. semantics vs. data)
- **Backward compatibility** (critical for adoption)
- **Clear value proposition** (semantic understanding = better LLM decisions)
- **Community-driven evolution** (standards that ignore users fail)

Failed efforts typically suffered from:
- Over-engineering and complexity
- Ignoring existing ecosystems
- Top-down design without implementation feedback
- Unclear benefits for developers

## Current Status

🌱 **Early Stage - Join Us!**

We've developed:
- [x] Initial research and prior art analysis
- [ ] Draft specification v0.1
- [ ] Reference implementation
- [ ] Proof-of-concept examples
- [ ] Community feedback and iteration

## Call for Collaboration

We're seeking researchers and practitioners in:
- **Semantic Web Technologies**: RDF, OWL, SPARQL, ontology engineering
- **Domain Ontologies**: Life sciences, healthcare, finance, manufacturing
- **LLM Systems**: Tool use, agent architectures, prompt engineering
- **Protocol Design**: API standards, distributed systems

### How to Get Involved

1. **Review the draft specification** in [`/spec`](./spec)
2. **Join the discussion** in [GitHub Discussions](https://github.com/[org]/smcp/discussions)
3. **Share your use cases** - What semantic capabilities do your LLM agents need?
4. **Contribute examples** from your domain
5. **Help shape the protocol** through feedback and PRs

## Example Vision

Imagine an LLM that can:

```json
{
  "request": "Find all services that can analyze gene expression data",
  "semantic_query": {
    "operation_type": "http://purl.obolibrary.org/obo/OBI_0001463",
    "input_type": "http://purl.obolibrary.org/obo/SO_0000704",
    "output_includes": "http://purl.obolibrary.org/obo/GO_0010467"
  }
}
```

Instead of keyword matching, the LLM understands the formal semantics of what it needs.

## Research Context

This initiative is led by the **Knowledge Engineering and AI Lab** at Tel-Hai University (in establishment), but we envision SMCP as a community-driven standard that belongs to everyone who contributes.

## Get In Touch

- **Email**: nimrobu@telhai.ac.il
- **GitHub Discussions**: [Start a discussion](https://github.com/[org]/smcp/discussions)
- **Twitter**: [@smcp_protocol](https://twitter.com/smcp_protocol) (coming soon)

### For Researchers

We welcome academic collaboration. If you're working on:
- Semantic service description
- Ontology-based system integration  
- LLM tool grounding
- Knowledge representation for AI

Please reach out! We're open to joint publications and research partnerships.

### For Industry Practitioners

If you're building:
- Domain-specific MCP servers
- LLM agent systems
- Semantic data platforms
- Ontology-driven applications

Your real-world requirements will help shape a practical, implementable protocol.

## License

MIT License - see [LICENSE](./LICENSE)

## Acknowledgments

- Built upon [Model Context Protocol](https://modelcontextprotocol.io) by Anthropic
- Inspired by decades of Semantic Web research
- Guided by the principles of open collaboration

---

**Ready to help define how LLMs understand services?** Join the conversation in [Discussions](https://github.com/[org]/smcp/discussions) →
