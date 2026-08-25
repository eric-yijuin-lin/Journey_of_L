#TeacherSelection 
## CPU v.s. GPU

| **單元**       | **CPU (Central Processing Unit)** | **GPU (Graphics Processing Unit)** |
| ------------ | --------------------------------- | ---------------------------------- |
| Control Unit | 複雜且佔比高（支援分支預測、亂序執行）               | 簡單且佔比低（多核心共用控制單元）                  |
| ALU          | 數量少、單核性能強                         | 數量極多、架構簡單（海量平行運算）                  |
| Cache        | 容量大且多階層（降低存取延遲）                   | 容量小（靠海量執行緒隱藏延遲）                    |
| 處理架構         | 序列處理，力求單一工作的低延遲                   | 平行處理，力求同時做更多的工作                    |
| 適用場景         | 低延遲、高指令複雜度的序列任務                   | 高吞吐量、低指令複雜度的大規模平行資料                |

Here's the full map:   
- 𝗖𝗣𝗨  — The Backbone 
	- 電腦的大腦，具備複雜的控制邏輯與多階層快取。擅長處理序列作業、邏輯判斷與通用運算。
	- General purpose. Sequential. Orchestration. 
	- Every AI pipeline starts and ends here 
	- Not the hero — the conductor Best for: Preprocessing, routing, managing I/O   
- 𝗚𝗣𝗨 — The Workhorse 
	- 擁有數千個平行運算核心（ALU）。最初專為圖像繪製設計，現廣泛用於矩陣運算、深度學習訓練與科學計算。
	- 16,896 CUDA cores running in parallel
	- The reason modern LLMs exist
	- $30K+ per H100, 700W draw — not subtle Best for: Training + inference at scale   
- 𝗧𝗣𝗨 — Google's Secret Weapon
	- Google 為深度學習量身打造的專用晶片（ASIC）。採用脈動陣列（Systolic Array）架構，專門加速矩陣乘法與張量運算。
	- Systolic array architecture — data flows in lockstep 
	- 2× cheaper than GPU, 2–3× better perf/watt
	- 9,216 TPUs in a single pod Best for: Google-scale tensor workloads   
- 𝗡𝗣𝗨 (Neural Processing Unit) — AI in Your Pocket
	- 專為邊緣端（如手機、筆電）設計的 AI 加速器。硬體電路高度模擬神經網路運算，主打**高能效比（低功耗、低發熱）**，常用於影像識別與端側 AI 任務。
	- On-device inference. No cloud. No latency.
	- INT8/INT4 quantized. Single-digit watts. → 5ms response. Data never leaves the device
	- Best for: Edge & mobile inference   
- 𝗟𝗣𝗨 (Language Processing Unit) — The Speed Demon
	- 由 Groq 提出、專為大語言模型（LLM）推論設計的晶片。採用晶片上高頻寬 SRAM，解決記憶體瓶頸，實現極高速的 Token 文字生成。
	- 230MB on-chip SRAM. Zero cache misses.
	- 241 tokens/sec. Deterministic every time.
	- 500 words generated in under 1 second
	- Best for: Real-time LLM serving   
- 𝗗𝗣𝗨 (Data Processing Unit) — The Invisible Layer
	- 專為資料中心與雲端架構設計的晶片。負責卸載（Offload）CPU 的**網路封包處理、儲存控制、資安加密與虛擬化管理**，讓 CPU 能集中資源處理應用程式。
	- SmartNIC that intercepts traffic at hardware level
	- Handles encryption, firewall, storage I/O
	- Frees the CPU entirely for AI workloads   Best for: Data center infrastructure

𝗧𝗵𝗲 𝗱𝗲𝗰𝗶𝘀𝗶𝗼𝗻 𝗳𝗿𝗮𝗺𝗲𝘄𝗼𝗿𝗸: 
- Latency matters most? → LPU or NPU
- Training a model? → GPU or TPU
- Massive scale on Google Cloud? → TPU
- Keeping data on-device? → NPU
- Securing data center traffic? → DPU
- Everything else? → CPU is still running the show
