<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:2563eb,100:8b5cf6&height=160&section=header&text=Rishab%20Malhotra&fontSize=48&fontColor=ffffff&fontAlignY=38&desc=Systems%20%C3%97%20AI%20Infrastructure%20%C2%B7%20Georgia%20Tech%20CS&descSize=17&descAlignY=60" alt="Rishab Malhotra" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=18&duration=45&pause=1800&color=4ADE80&background=0D1117&multiline=true&width=560&height=110&lines=%3E+Building+production+AI+infrastructure;%3E+Engineering+high-performance+C%2B%2B+systems;%3E+Turning+research+into+working+software" alt="Terminal intro" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/rishabmalhotra7580"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:rishab.malhotra7580@gmail.com"><img src="https://img.shields.io/badge/Email-8B5CF6?style=for-the-badge&logo=gmail&logoColor=white" /></a>
  <a href="https://github.com/Rishab-Mal?tab=repositories"><img src="https://img.shields.io/badge/All_Repos-24292F?style=for-the-badge&logo=github&logoColor=white" /></a>
</p>

<br/>

## About me

```cpp
struct Rishab {
    std::string school  = "Georgia Tech, B.S. Computer Science";
    std::string threads = "Intelligence + Systems & Architecture";
    std::vector<std::string> building = {
        "C++ servers benchmarked down to p99 latency",
        "physics-informed ML on a B200 SuperPOD",
        "real-time computer vision"
    };
    std::string next    = "Summer 2027: software, systems, AI infrastructure";
};
```

<br/>

## Flagship: [kvstore](https://github.com/Rishab-Mal/kvstore)

A multithreaded, Redis-style key-value server in C++20. Sharded in-memory store, CRC32-checksummed append-only log that survives `kill -9`, group-commit `fsync`, and a custom load generator. Tested under ASan, UBSan and TSan in CI.

<table>
  <tr>
    <td width="55%" valign="top">

```text
   clients ──TCP──▶ accept loop
                        │
                        ▼
          ┌──── thread pool ────┐
          │ frame → parse → run │
          └──────────┬──────────┘
                     ▼
   ┌────────┬────────┬────────┬────────┐
   │shard 0 │shard 1 │  ...   │shard 15│
   │rw-lock │rw-lock │        │rw-lock │
   └────────┴────────┴────────┴────────┘
                     │ writes
                     ▼
     append-only log ─▶ group-commit fsync
```

  </td>
    <td width="45%" valign="top">

**Sharding, 64 clients, 50% writes**

| | ops/sec | p99 |
|---|---:|---:|
| 1 global lock | 31.5K | 18.3 ms |
| 16 shards | **126.7K** | **3.8 ms** |
| | **4.0x** | **−79%** |

<sub>Median of 5 benchmark sessions. [Methodology](https://github.com/Rishab-Mal/kvstore#benchmarks)</sub>

  </td>
  </tr>
</table>

<br/>

## More projects

<table>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/Rishab-Mal/TheChaosWall">🌀 The Chaos Wall</a></h3>
      Can physics-informed ML beat chaos? Hamiltonian Neural Networks vs. LSTMs on a double pendulum. <b>500+ GB</b> of simulation data on UF's <b>B200 SuperPOD</b>. The HNN conserved energy where the LSTM drifted.
      <br/><br/>
      <code>PyTorch</code> <code>C++</code> <code>HPC</code>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/Rishab-Mal/High-Performance-Event-Driven-Backtester-C-20-">📈 Event-Driven Backtester</a></h3>
      Low-latency engine for testing trading strategies on historical tick data, designed to avoid look-ahead bias.
      <br/><br/>
      <code>C++20</code> <code>event-driven</code>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/Ryanqu27/SASEHacks-Visi">👁️ VISI</a></h3>
      🏆 <b>1st place, UF SASEHacks 2026.</b> Real-time assistant for visually impaired users: gesture recognition, face detection, LLM scene narration, and speech.
      <br/><br/>
      <code>Python</code> <code>OpenCV</code> <code>MediaPipe</code>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/UF-SASE-Web-Team/UF-SASE-Website">🌐 ufsase.com</a></h3>
      Production site serving <b>2,000+</b> users. Built front-end architecture and a component library with a 20-person team.
      <br/><br/>
      <code>React</code> <code>TypeScript</code> <code>Tailwind</code>
    </td>
  </tr>
</table>

<p align="center">
  <a href="https://github.com/Rishab-Mal/TheChaosWall"><img src="1785720388400.jpg" width="720" alt="The Chaos Wall research poster" /></a>
  <br/>
  <sub>The Chaos Wall research poster, Gator AI (2026)</sub>
</p>

<br/>

## Tech stack

| Domain | Tools |
|---|---|
| **Languages** | C++, Python, TypeScript, Java, C, SQL |
| **Systems** | Linux, POSIX sockets, multithreading, Docker, GitHub Actions |
| **AI / ML** | PyTorch, OpenCV, MediaPipe, SpeechBrain |
| **Backend & Web** | FastAPI, REST, WebSockets, React |
| **Cloud & Data** | GCP, Azure, MongoDB |

<br/>

<p align="center"><sub>Open to Summer 2027 internships in software, systems and AI infrastructure.</sub></p>
