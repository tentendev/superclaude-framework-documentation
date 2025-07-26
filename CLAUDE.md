# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is the documentation repository for SuperClaude Framework v3.0 - a comprehensive enhancement system for Claude Code that adds intelligent routing, specialized commands, and expert personas for software development workflows.

## Repository Structure

The repository contains user-facing documentation files that explain the SuperClaude Framework:

- `superclaude-user-guide.md` - Main user guide and overview
- `commands-guide.md` - Detailed guide to all 17 SuperClaude commands
- `flags-guide.md` - Complete reference for command flags and options
- `personas-guide.md` - Guide to the 11 AI specialist personas
- `installation-guide.md` - Installation and setup instructions

## Content Architecture

The documentation follows a structured approach:

### Command System (commands-guide.md)
- **17 specialized commands** organized by category:
  - Development: `/workflow`, `/implement`, `/build`, `/design`
  - Analysis: `/analyze`, `/troubleshoot`, `/explain`
  - Quality: `/improve`, `/cleanup`, `/test`
  - Management: `/estimate`, `/task`, `/spawn`
  - Utilities: `/document`, `/git`, `/load`, `/index`

### Persona System (personas-guide.md)
- **11 AI specialists** with auto-activation:
  - Technical: architect, frontend, backend, security, performance
  - Process: analyzer, qa, refactorer, devops
  - Communication: mentor, scribe

### Flag System (flags-guide.md)
- **Smart auto-activation** based on context
- **Manual override** capabilities when needed
- **Performance optimization** flags for large operations

### Installation System (installation-guide.md)
- **Multi-platform support** (Windows, macOS, Linux)
- **Installation profiles** (minimal, quick, developer)
- **Dependency management** and troubleshooting

## Documentation Principles

The documentation follows these key principles:

1. **Simplicity First** - Users don't need to memorize complex systems
2. **Auto-Activation Focus** - Most capabilities work automatically
3. **Progressive Disclosure** - Basic usage is simple, advanced features available when needed
4. **Honest Communication** - Acknowledges rough edges and limitations
5. **Evidence-Based** - Focuses on practical usage over theoretical complexity

## Key Features Documented

### Intelligent Routing System
- **Complexity Detection** - Automatically determines appropriate tools and experts
- **Domain Recognition** - Identifies frontend, backend, security, and other specialized work
- **Resource Management** - Optimizes token usage and performance
- **Wave Orchestration** - Multi-stage execution for complex operations

### Auto-Activation Patterns
- **Context-Aware** - Commands activate appropriate specialists automatically
- **Keyword Detection** - Recognizes security, performance, and domain-specific work
- **Fallback Strategies** - Graceful degradation when specialized tools unavailable

### Quality Gates and Validation
- **8-Step Validation Cycle** - Comprehensive quality assurance
- **Evidence Generation** - Metrics and documentation for all changes
- **Risk Assessment** - Proactive identification of potential issues

## Working with This Documentation

When editing these files:

1. **Maintain User-Friendly Tone** - Keep the approachable, honest communication style
2. **Update Cross-References** - Ensure all guides stay synchronized
3. **Preserve Auto-Activation Focus** - Emphasize that complexity is handled automatically
4. **Include Practical Examples** - Show real usage patterns, not just theory
5. **Validate Technical Accuracy** - Ensure all command examples and flags are correct

## Content Guidelines

- Use emoji sparingly but consistently (🚀 for quick start, 🎯 for focus areas, etc.)
- Include both "don't overthink it" quick starts and detailed references
- Acknowledge v3.0 beta status and ongoing improvements
- Provide multiple paths (minimal to advanced) for different user needs
- Include troubleshooting and "what if it doesn't work" scenarios

## Testing Documentation Changes

When updating documentation:
1. Ensure all command examples are valid SuperClaude syntax
2. Verify flag combinations work as described
3. Test auto-activation triggers mentioned in examples
4. Check that installation instructions work across platforms
5. Validate cross-references between guides remain accurate