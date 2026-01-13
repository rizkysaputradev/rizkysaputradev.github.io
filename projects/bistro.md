---
title: Byte Bistro Transport Protocols
subtitle: "Cross-platform, multithreaded real-time ambient sound engine built with Rust, C++, Python bindings, and SIMD-accelerated DSP"
layout: page
slider_key: bistro
repo_url: "https://github.com/rizkysaputradev/Byte-Bistro-Transport-Protocols"
---

<div class="project-layout">

  <!-- LEFT: structured writeup (rendered as real Markdown via markdownify) -->
  <div class="project-writeup">
    {% capture writeup %}

## Summary
**Byte Bistro** is an introductory to the foundation of **data communication** and **networking system** through a **low-level implementation** on a set of **transport protocols** over an **unreliable network**. Hereby, the data are sent through `“orders”` over a **User Datagram Protocol (UDP)** and stirred in its `loss`/`dup`/`reorder`/`delay`, which then compared with a **Go-Back-N (GBN)** vs **Selective Repeat (SR)** end-to-end inclusion of its **replayable experiments**, **structured logs/CSVs**, and **visual plots**

---

## Research Purpose
Reliable data transport is often assumed to be `“solved”` by a **Transmission Control Protocol (TCP)**. However, several considerations such as the **internal complexity**, **kernel coupling**, and **adaptive heuristics** in modern TCP stacks creates an ambiguity for its experimentation. In addition, **Transport protocols** are simpler to understand by its **out-of-order**, **loss**, **dupes**, **rate limits** and **latency jitters**.

**Byte-Bistro** solves this issue by providing a sandbox where:

- Every **packet**, **ack**, **retransmission**, **timeout**, and **ordering event** is fully observable.
- Channel conditions are **mathematically controllable** (`loss`, `duplication`, `reordering`, `rate limits`, `jitter distributions`).
- Protocol behavior which can be **decomposed**, **modified**, and **extended** without operating the system interference.

Paired with a controlled channel and a server `“cook”` time (processing latency), where it can isolated throguh its protocol behavior vs application latency in order to quantify the differences on the CSVs and visual plots. This is critical due to its protocol theory that must not stop at derivations, as it must be validated against its empirical runtime.

---

## Future Roadmaps
- **FEC (Forward Error Correction)** layer for burst losses.
- **Congestion Control** toy modules (AIMD, Reno-like).
- **Bi-directional data** (client → server → client flows).
- **Throughput & goodput reporting** alongside RTT.
- **pcap** capture hooks for Wireshark-friendly traces.
- **Property-based tests** (quickcheck-style) for channel and protocol invariants.
- **Threads** for multi-client load.
- **Protocol plug-in API** to allow custom transports.

{% endcapture %}

    {{ writeup | markdownify }}
  </div>

  <!-- RIGHT: slider first, then quick facts -->
  <div class="project-media">

    {% assign slider_images = site.data.project_sliders[page.slider_key] %}
    {% include project_slider.html images=slider_images %}

    <div class="mini-card" style="margin-top: 12px;">
      <div class="mini-title">Detailed Specifications</div>
      <div class="mini-body">
        <ul style="margin: 10px 0 0; padding-left: 18px;">
          <li><strong>Domain:</strong> Data Communication, Computer Networks, System Programming, Real-Time System</li>
          <li><strong>Core:</strong> UDP, GBN, SR, Concurrency</li>
          <li><strong>Transport Protocols:</strong> GBN, SR</li>
          <li><strong>Focus:</strong> Network Simulation, Multithreading, Protocol Communication</li>
        </ul>

        <div style="margin-top: 12px; display: flex; gap: 10px; flex-wrap: wrap;">
          <a class="btn" href="{{ page.repo_url }}" target="_blank" rel="noopener">View Repository</a>
          <a class="btn secondary" href="/projects/">All Projects</a>
        </div>
      </div>
    </div>

  </div>

</div>