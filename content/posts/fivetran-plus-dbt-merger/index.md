---
title: "Fivetran + dbt: The Quiet Power Shift No One's Talking About"
date: 2025-10-16
draft: false
description: "Fivetran and dbt's merger is a power shift that could redefine the modern data stack. Here's how open storage, metadata, and orchestration could reshape who truly controls the data ecosystem."
tags: ["data orchestration", "fivetran dbt merger", "modern data stack", "data engineering trends 2025", "apache iceberg"]
categories: ["data orchestration", "thought-leadership"]
---
When Fivetran and dbt announced their merger, the industry reaction was predictable: "Sure. Ingestion plus transformation. Clean vertical integration."

That reading entirely misses the point.

The merger isn't about efficiency, it's about **control** — who defines how data moves, how it's modeled, and ultimately, how it's understood.

Fivetran and dbt now own both the movement *and* the meaning of data. Add Iceberg, and storage becomes interchangeable. Add orchestration, and meaning becomes the organizing principle. The warehouse stops being the center of gravity. The leverage moves upward, to the layer that defines *what* the data means and *when* it becomes *real*.

And this isn't just theory. Snowflake's multi-billion-dollar business depends on customers running compute in its warehouses. If metadata and orchestration become the control plane — and compute becomes something you rent by the hour — that economic model starts to erode.

*This shift isn't just conceptual — it's structural.*

![Comparative diagram showing a “Warehouse-Centric Stack” on the left — Storage, Warehouse, Transform (dbt), and BI & Analytics — and a “Meaning-Centric Stack” on the right — Open Storage (Iceberg), Compute Engines (Snowflake, BigQuery, Trino), Metadata + Orchestration (Fivetran + dbt), and BI & Activation. An arrow curves upward between them labeled “Control moves upward — from compute to meaning,” illustrating how power in the data stack is shifting toward metadata and orchestration layers.](powershift-dbt-fivetran.png "Control in modern data architecture is moving from compute to meaning")

## From Warehouses to Meaning Engines
For the last decade, the warehouse was the stack. Everything pointed at it. Your data lived there, your SQL ran there, your budget burned there. Snowflake, BigQuery and Redshift became the gravitational pull of modern data.

This merger changes that gravity:
- **Fivetran** owns *movement* — every pipeline feeding the system.
- **dbt** controls *meaning* — the models that turn raw data into something usable.

Together, they own **intent**. And once you own intent, the warehouse becomes the executor of someone else's logic. It's still essential, but it's no longer in charge.

The stack is inverting. Not completely, not yet — but the motion is clear.

## Iceberg and the Rise of Open Storage
That inversion only became possible recently. Open table formats like **Apache Iceberg** broke the old bond between compute and storage, turning object storage into a query-ready, versioned substrate.

This is already playing out in the wild. Netflix runs the same Iceberg tables through Spark for ML and Trino for analytics without moving a byte. Coinbase queries S3 directly and bypasses Snowflake for half its workloads. The warehouse no longer owns the files; it just rents access to them.

Iceberg separates *where* data lives from *who controls* it — and that shift gives Fivetran and dbt new leverage that doesn't depend on owning compute at all. The warehouse isn't disappearing, but it has lost exclusivity.

## Power and Lock-In
For years, the warehouse defined the shape of every stack. Now the pieces that used to serve it — ingestion, transformation, lineage — are beginning to direct it instead. Metadata, not compute scale, is becoming the moat.

That raises an uncomfortable question: If Fivetran + dbt becomes the new control layer, are we just trading one lock-in for another? Probably — but this one sits on top of open storage. It's a different kind of dependency, one that is strategic rather than infrastructural. You can switch warehouses. You can't easily switch the semantics that define your business logic.

## The Next Frontier: Orchestration of Meaning
To finish the shift, Fivetran and dbt will need orchestration that can think — not just schedule, but reason.

It has to understand relationships like:
- "This Fivetran sync updates that dbt model"
- "That dbt model triggers this Census activation"
- "These three together define a data product"

Right now, no one does this perfectly. Airflow schedules tasks but doesn't really understand assets. Dagster gets closer: It treats data as a first-class entity, tracks lineage and reasons about dependencies.

If Fivetran + dbt build this themselves, it will look a lot like Dagster. If they don't, they'll need to partner — or buy. Building gives them total control but takes time and talent. Partnering is faster, but fractures the story.

Either way, they have about eighteen months before someone else defines what "metadata-aware orchestration" means.

## Why It Matters
This merger isn't about consolidation, it's about who defines *reality*. If Fivetran and dbt succeed, every other layer — storage, compute, even BI — becomes negotiable.

If they pull this off, your warehouse becomes swappable. Your BI tool can change. The only constant is the metadata layer that defines what everything means. For data teams, that could feel like freedom or fragmentation. You're betting your architecture on one vendor's vision of orchestration. That's a different bet than tying yourself to Snowflake's compute, but it's still a bet.

When metadata, lineage, and orchestration converge, the stack stops being a collection of tools and starts functioning as a *system of intent* — a network that understands not just how data moves, but *why*.

## The Question That Remains
So the question isn't about whether the merger "works". It's about what happens when the meaning layer becomes the layer that holds power. The warehouse solved compute at scale. This merger is trying to solve meaning at scale.

Whether Fivetran + dbt succeed or not, someone will — and that's when the modern stack stops being a loose federation of tools and becomes a system that thinks.

No matter what happens, the modern data stack is growing up.
