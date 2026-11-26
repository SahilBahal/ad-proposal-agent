# Ad Proposal Agent: Sample Data (Synthetic)

> **Synthetic data.** Northline Media and every advertiser, agency, person and number in this file are fictional, created for a portfolio demo.

This folder is the knowledge base and test set for the Ad Proposal Agent demo. It models a mid-size digital publisher, **Northline Media**, that sells newsletter, podcast, display/video and branded content inventory.

## Folders
| Folder | What's in it | Used for |
|---|---|---|
| `knowledge_base/rate_cards/` | 2027 pricing for every product | RAG: pricing |
| `knowledge_base/audience/` | Audience profiles per newsletter and podcast | RAG: matching briefs to products |
| `knowledge_base/policies/` | Discounts, ad guidelines, inventory availability | RAG: rules the agent must follow |
| `knowledge_base/past_proposals/` | 5 past proposals with full pricing math | RAG: examples of good output |
| `knowledge_base/case_studies/` | 2 campaign results | RAG: proof points for proposals |
| `test_briefs/` | 10 incoming advertiser briefs | Agent input / test set |
| `test_briefs/expected_results.csv` | Which docs each brief should retrieve and what the agent should catch | Retrieval + agent evaluation |

## How pricing works (summary)
Base rate × seasonal premium → volume discount → bundle discount (max 20% combined) → agency commission (if agency). Full rules in `policies/pricing_and_discount_policy.md`.

## Edge cases built into the test briefs
Sold-out dates, a restricted category, a below-minimum budget, a missing budget, a political ad (not accepted), Q4 premium pricing, a crypto legal review, and a discount request above policy.
