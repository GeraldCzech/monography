# BEBA Information Model v1

Status: canonical working architecture

## Purpose

This document defines the fundamental information model of the BEBA research system. It specifies which scientific objects exist, what they represent, and how they relate to one another.

The model is independent of dissertation chapters, papers, software tools, and AI systems.

## Design Philosophy

The repository is knowledge-centric, not document-centric.

Papers, dissertation chapters, presentations, and journal articles are views on an underlying knowledge base. The primary unit is scientific knowledge, not the document in which it later appears.

## Core Object Types

### Concept

A scientific idea or phenomenon.

Examples:
- Epistemic Uncertainty
- Information Asymmetry
- Credence Goods
- Trust
- Warm Glow
- Brand Equity
- Commitment

A concept is not necessarily measurable. It may be theoretical, empirical, motivational, institutional, or behavioural.

### Theory

An explanatory framework that connects concepts.

Examples:
- Information Economics
- Signalling Theory
- Theory of Planned Behaviour
- Integrated Behavioural Model
- Impure Altruism
- Relationship Marketing

### Model

A formal or semi-formal representation of one or more theories.

Examples:
- Faircloth model
- Boenigk and Becker model
- Rios Romero et al. model
- BEBA

Models specify relations between constructs and may be empirically tested.

### Construct

A measurable latent or observed variable used in empirical modelling.

Examples:
- Brand Trust
- Brand Commitment
- Brand Image
- Donation Intention
- Donation Behaviour

### Scale

A measurement instrument or item family.

Examples:
- FC_BI
- FC_BP
- BO_TR
- BO_CO
- RO_BW
- OF02_01

### Claim

The smallest reusable scientific knowledge unit.

A claim is an evidence-related statement, for example:
- Trust is more proximal to donation behaviour than mere awareness.
- Warm Glow may bypass brand-mediated mechanisms.
- Awareness is necessary but insufficient for resource mobilisation.

Claims can be supported, contradicted, refined, or superseded.

### Evidence

An empirical or theoretical observation that supports or contradicts a claim.

Evidence comes from papers, datasets, experiments, SEM results, meta-analyses, reviews, and replication studies.

### Paper

A scientific publication or manuscript. Papers are sources, not knowledge objects.

### Chapter

A presentation unit in the dissertation. Chapters organise knowledge for argumentation.

### Figure

A graphical representation of concepts, claims, models, or theoretical relations.

## Knowledge Hierarchy

Evidence -> Claims -> Concepts -> Theories -> Models -> Chapters / Papers

The hierarchy should not be reversed. A chapter does not define the knowledge base; it draws from it.

## Canonical vs Working Objects

Objects may have one of four statuses:

- candidate: generated from literature or analysis, not yet reviewed.
- active: currently used in the BEBA programme.
- canonical: accepted as stable for the current dissertation version.
- superseded: replaced but retained for auditability.

## Versioning Rule

Definitions, construct mappings, and theoretical roles must not change silently. Significant changes require an ADR or DecisionLog entry.

## Guiding Principle

The dissertation documents the research programme. It is not the research programme itself.
