# Echo Token-Auction Ads

Contextual advertising platform that inserts relevant ads into LLM conversations. Uses AI for real-time ad generation with vector-based targeting and revenue sharing.

## Key Features

- AI ad generation with OpenAI/Anthropic
- Sub-100ms ad insertion latency
- Vector-based semantic targeting
- VCG auction research platform
- Real-time analytics and optimization
- PCI compliant payment processing
- User engagement rewards

## Architecture

25+ microservices across 5 layers:

**Frontend**
- Chat Interface - React/Next.js WebSocket UI
- Advertiser Dashboard - Campaign management

**Gateway** 
- Request Routing - Cloudflare Workers edge routing
- Authentication - Supabase Auth with OAuth/MFA
- Rate Limiting - Redis distributed limiting

**Core Business**
- Conversation - Multi-LLM routing and streaming
- Ad Generation - AI contextual ad creation
- Auction Engine - Shadow VCG auction research
- Context Analysis - Semantic conversation analysis

**Advertiser Management**
- Ad Upload - Multi-format content ingestion
- Web Scraping - Product information extraction
- Google Ads Integration - OAuth API sync
- Advertisement Storage - Content catalog

**Financial**
- Billing - Stripe payment processing
- Revenue Tracking - Financial analytics
- User Rebate - Engagement rewards
- Settlement - Multi-party reconciliation

**ML/AI**
- ML Pipeline - Model lifecycle management
- Model Training - Distributed training infrastructure
- AI Content Generation - RLHF training
- Recommendation Engine - Personalized ad selection

**Infrastructure**
- Event Bus - Apache Kafka (1M+ events/sec)
- Vector Database - Embedding storage
- Caching - Redis distributed caching
- Metrics Collection - Real-time observability

## Tech Stack

**Core**
- Database: Supabase PostgreSQL with RLS
- Real-time: Supabase WebSocket streaming  
- Auth: Supabase Auth with OAuth/MFA
- Edge: Cloudflare Workers, Vercel

**AI/ML**
- LLMs: OpenAI GPT-4, Anthropic Claude
- ML: TensorFlow.js/PyTorch pipelines
- Vector: Supabase pgvector
- Serving: TensorFlow Serving

**Payments**
- Processing: Stripe PCI-compliant
- Analytics: Custom financial reporting
- Compliance: Multi-currency tax handling

**Messaging**
- Streaming: Apache Kafka/Confluent
- Processing: Apache Flink

## Documentation

- [Service Docs](./module_design_docs/)
- [API Documentation](./docs/API.md)
- [ML Operations](./docs/ML_OPS.md)