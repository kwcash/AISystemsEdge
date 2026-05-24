# AISystemsEdge File Classification Map

| Original Path | Classification | Future Location | Action | Notes |
|---|---|---|---|---|
| tradingagents/graph/trading_graph.py | CORE | core/orchestration | preserve | Primary orchestration spine |
| tradingagents/graph/propagation.py | CORE | core/orchestration | preserve | Workflow propagation engine |
| tradingagents/graph/checkpointer.py | CORE | core/checkpoints | preserve | Persistence/recovery logic |
| tradingagents/graph/reflection.py | CORE | core/memory | preserve/adapt | Reflection and learning logic |
| tradingagents/graph/signal_processing.py | CORE | core/runtime | adapt | Generalize beyond trading signals |
| tradingagents/graph/conditional_logic.py | CORE | core/runtime | preserve | Decision routing engine |
| tradingagents/graph/setup.py | CORE | core/runtime | preserve | Runtime initialization |
| tradingagents/graph/analyst_execution.py | DOMAIN | domain/workflows | redesign | Enterprise workflow execution |
| tradingagents/default_config.py | CORE | core/runtime | preserve/adapt | System configuration layer |

| tradingagents/llm_clients/base_client.py | CORE | core/llm_clients | preserve | Provider abstraction foundation |
| tradingagents/llm_clients/factory.py | CORE | core/llm_clients | preserve | Client creation/orchestration |
| tradingagents/llm_clients/model_catalog.py | CORE | core/llm_clients | preserve/adapt | Model registry |
| tradingagents/llm_clients/capabilities.py | CORE | core/llm_clients | preserve | Capability abstraction |
| tradingagents/llm_clients/validators.py | CORE | core/llm_clients | preserve | Validation layer |
| tradingagents/llm_clients/api_key_env.py | CORE | core/runtime | preserve | Environment abstraction |
| tradingagents/llm_clients/openai_client.py | CORE | core/llm_clients | preserve | OpenAI provider |
| tradingagents/llm_clients/google_client.py | CORE | core/llm_clients | preserve | Google provider |
| tradingagents/llm_clients/anthropic_client.py | CORE | core/llm_clients | preserve | Anthropic provider |
| tradingagents/llm_clients/azure_client.py | CORE | core/llm_clients | preserve | Enterprise provider |

| tradingagents/agents/utils/memory.py | CORE | core/memory | preserve | Memory persistence |
| tradingagents/agents/utils/structured.py | CORE | core/schemas | preserve | Structured outputs |
| tradingagents/agents/utils/agent_states.py | CORE | core/runtime | preserve | State management |
| tradingagents/agents/utils/agent_utils.py | CORE | core/utils | preserve | Shared utilities |
| tradingagents/agents/schemas.py | CORE | core/schemas | preserve | Shared schemas |

| tradingagents/agents/managers/research_manager.py | DOMAIN | domain/agents | redesign | Strategic coordinator |
| tradingagents/agents/managers/portfolio_manager.py | DOMAIN | domain/agents | redesign | Enterprise coordinator |
| tradingagents/agents/trader/trader.py | DOMAIN | domain/agents | redesign | Operations engine |

| tradingagents/agents/researchers/bull_researcher.py | DOMAIN | domain/agents | redesign | Positive assessment agent |
| tradingagents/agents/researchers/bear_researcher.py | DOMAIN | domain/agents | redesign | Risk assessment agent |

| tradingagents/agents/risk_mgmt/aggressive_debator.py | DOMAIN | domain/agents | redesign | Risk posture engine |
| tradingagents/agents/risk_mgmt/conservative_debator.py | DOMAIN | domain/agents | redesign | Risk posture engine |
| tradingagents/agents/risk_mgmt/neutral_debator.py | DOMAIN | domain/agents | redesign | Risk posture engine |

| tradingagents/agents/analysts/news_analyst.py | DOMAIN | domain/agents | redesign | Intelligence agent |
| tradingagents/agents/analysts/sentiment_analyst.py | DOMAIN | domain/agents | redesign | Stakeholder analysis |
| tradingagents/agents/analysts/social_media_analyst.py | DOMAIN | domain/agents | redesign | External signal analysis |
| tradingagents/agents/analysts/market_analyst.py | DOMAIN | domain/agents | redesign | Operational telemetry analysis |
| tradingagents/agents/analysts/fundamentals_analyst.py | DOMAIN | domain/agents | redesign | Structural analysis |

| tradingagents/dataflows/interface.py | CORE | core/runtime | preserve | Data abstraction interface |
| tradingagents/dataflows/config.py | CORE | core/runtime | preserve | Data configuration |
| tradingagents/dataflows/utils.py | CORE | core/utils | preserve | Shared utilities |

| tradingagents/dataflows/alpha_vantage.py | DOMAIN | domain/dataflows | isolate | Financial-specific |
| tradingagents/dataflows/alpha_vantage_common.py | DOMAIN | domain/dataflows | isolate | Financial-specific |
| tradingagents/dataflows/alpha_vantage_fundamentals.py | DOMAIN | domain/dataflows | isolate | Financial-specific |
| tradingagents/dataflows/alpha_vantage_indicator.py | DOMAIN | domain/dataflows | isolate | Financial-specific |
| tradingagents/dataflows/alpha_vantage_news.py | DOMAIN | domain/dataflows | isolate | Financial-specific |
| tradingagents/dataflows/alpha_vantage_stock.py | DOMAIN | domain/dataflows | isolate | Financial-specific |

| tradingagents/dataflows/y_finance.py | DOMAIN | domain/dataflows | isolate | Financial-specific |
| tradingagents/dataflows/yfinance_news.py | DOMAIN | domain/dataflows | isolate | Financial-specific |
| tradingagents/dataflows/stockstats_utils.py | DOMAIN | domain/dataflows | isolate | Trading-specific |
| tradingagents/dataflows/stocktwits.py | DOMAIN | domain/dataflows | isolate | Trading-specific |
| tradingagents/dataflows/reddit.py | DOMAIN | domain/context_providers | adapt | General external sentiment source |

| cli/main.py | DOMAIN | domain/workflows | redesign | Interactive execution entry |
| cli/config.py | CORE | core/runtime | preserve | CLI/runtime config |
| cli/models.py | CORE | core/schemas | preserve | CLI schemas |
| cli/utils.py | CORE | core/utils | preserve | CLI helpers |
| cli/stats_handler.py | DOMAIN | domain/workflows | redesign | Reporting/telemetry |
| cli/announcements.py | DOMAIN | domain/prompts | redesign | Messaging layer |

| tests/test_checkpoint_resume.py | CORE | tests | preserve | Infrastructure validation |
| tests/test_memory_log.py | CORE | tests | preserve | Memory validation |
| tests/test_structured_agents.py | CORE | tests | preserve | Structured execution |
| tests/test_signal_processing.py | CORE | tests | preserve | Signal engine testing |

| Dockerfile | CORE | root | preserve | Runtime container |
| docker-compose.yml | CORE | root | preserve/adapt | Multi-service orchestration |
| requirements.txt | CORE | root | preserve | Dependency management |
| pyproject.toml | CORE | root | preserve | Package management |
| README.md | CORE | root | rewrite | Platform identity |