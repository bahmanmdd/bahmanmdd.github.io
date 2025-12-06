---
title: Skills & Training
summary: Technical skills, languages, professional training, and code repositories
type: landing

design:
  spacing: '5rem'

sections:
  - block: resume-skills
    content:
      title: Technical Skills
      username: admin
    design:
      show_skill_percentage: false
  
  - block: markdown
    content:
      title: Languages
      text: |
        <style>
        .language-grid {
          display: grid;
          gap: 1.5rem;
          margin-top: 2rem;
        }
        
        .language-row {
          display: grid;
          grid-template-columns: 200px 1fr;
          align-items: center;
          gap: 1.5rem;
        }
        
        .language-name {
          font-weight: 600;
          color: #00d4ff;
          font-size: 1.1rem;
        }
        
        .language-note {
          font-size: 0.85rem;
          color: #888;
          margin-left: 0.5rem;
        }
        
        .cefr-bar-container {
          position: relative;
          background: rgba(0, 0, 0, 0.6);
          border: 1px solid #333;
          border-radius: 8px;
          padding: 8px;
          display: flex;
          gap: 4px;
        }
        
        .cefr-level {
          flex: 1;
          height: 35px;
          background: rgba(50, 50, 50, 0.5);
          border-radius: 4px;
          display: flex;
          align-items: center;
          justify-content: center;
          font-size: 0.75rem;
          font-weight: 600;
          color: #666;
          position: relative;
          transition: all 0.3s ease;
        }
        
        .cefr-level.filled {
          background: linear-gradient(135deg, #00d4ff 0%, #00a8cc 100%);
          color: #000;
          box-shadow: 0 0 15px rgba(0, 212, 255, 0.5);
        }
        
        .cefr-level.filled::after {
          content: '✓';
          position: absolute;
          right: 4px;
          top: 2px;
          font-size: 0.7rem;
        }
        </style>
        
        <div class="language-grid">
          <div class="language-row">
            <div class="language-name">
              Persian
              <span class="language-note">(mother tongue)</span>
            </div>
            <div class="cefr-bar-container">
              <div class="cefr-level filled">A1</div>
              <div class="cefr-level filled">A2</div>
              <div class="cefr-level filled">B1</div>
              <div class="cefr-level filled">B2</div>
              <div class="cefr-level filled">C1</div>
              <div class="cefr-level filled">C2</div>
            </div>
          </div>
          
          <div class="language-row">
            <div class="language-name">
              Azeri
              <span class="language-note">(bilingual)</span>
            </div>
            <div class="cefr-bar-container">
              <div class="cefr-level filled">A1</div>
              <div class="cefr-level filled">A2</div>
              <div class="cefr-level filled">B1</div>
              <div class="cefr-level filled">B2</div>
              <div class="cefr-level filled">C1</div>
              <div class="cefr-level filled">C2</div>
            </div>
          </div>
          
          <div class="language-row">
            <div class="language-name">English</div>
            <div class="cefr-bar-container">
              <div class="cefr-level filled">A1</div>
              <div class="cefr-level filled">A2</div>
              <div class="cefr-level filled">B1</div>
              <div class="cefr-level filled">B2</div>
              <div class="cefr-level filled">C1</div>
              <div class="cefr-level filled">C2</div>
            </div>
          </div>
          
          <div class="language-row">
            <div class="language-name">Turkish</div>
            <div class="cefr-bar-container">
              <div class="cefr-level filled">A1</div>
              <div class="cefr-level filled">A2</div>
              <div class="cefr-level filled">B1</div>
              <div class="cefr-level filled">B2</div>
              <div class="cefr-level">C1</div>
              <div class="cefr-level">C2</div>
            </div>
          </div>
          
          <div class="language-row">
            <div class="language-name">Dutch</div>
            <div class="cefr-bar-container">
              <div class="cefr-level filled">A1</div>
              <div class="cefr-level filled">A2</div>
              <div class="cefr-level filled">B1</div>
              <div class="cefr-level">B2</div>
              <div class="cefr-level">C1</div>
              <div class="cefr-level">C2</div>
            </div>
          </div>
          
          <div class="language-row">
            <div class="language-name">French</div>
            <div class="cefr-bar-container">
              <div class="cefr-level filled">A1</div>
              <div class="cefr-level filled">A2</div>
              <div class="cefr-level filled">B1</div>
              <div class="cefr-level">B2</div>
              <div class="cefr-level">C1</div>
              <div class="cefr-level">C2</div>
            </div>
          </div>
        </div>
    design:
      columns: '1'
  
  - block: markdown
    content:
      title: Professional Development
      text: |
        #### Advanced Transportation & AI
        
        - **TRAIL International Summer School** — Automated Driving (TRAIL Research School)
        - **Traffic Flow Modeling & Control** — Crete Short Course
        - **Discrete Choice Analysis** — Microeconomics & ML Approaches (TU Delft)
        - **SURF Academy** — Research Methods in Transportation (TRAIL Research School)
        
        #### AI & Machine Learning
        
        - Building Agentic RAG with LlamaIndex (Deeplearning.ai)
        - LLMOps & Finetuning Large Language Models (Deeplearning.ai)
        - Knowledge Graphs for RAG (Deeplearning.ai)
        
        #### Research & Academic Skills
        
        - **Grant Writing** — Scientific Writing for Research Proposals (University of Colorado, Coursera)
        - **Peer Review** — Managing Academic Publication Process (TU Delft)
        - **Teaching** — Development of Active Learning (TU Delft OpenCourseWare)
        - **Mentoring** — Supervising Graduate Students (TU Delft)
    design:
      columns: '1'
  
  - block: markdown
    content:
      title: Notable Open Source Contributions
      text: |
        - [HDLMF_GIN-GA](https://github.com/bahmanmdd/HDLMF_GIN-GA) — Hybrid deep learning optimization framework for network design using deep learning based surrogate modeling
        - [rr-measure-basic](https://github.com/RRinTransportation/rr-measure-basic) — Using LLMs for automated pipeline to assess reproducibility of transportation research papers
        - [TOD_simulation](https://github.com/bahmanmdd/TOD_simulation) — Teleoperated driving simulation framework
        - [DAP](https://github.com/bahmanmdd/DAP) — Java simulation tool for anchorage planning
        - [Research Dataset](https://doi.org/10.6084/m9.figshare.27889251.v3) — Transport network datasets for training graph neural network models
    design:
      columns: '1'
---
