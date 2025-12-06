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
        .language-proficiency {
          width: 90vw;
          max-width: none;
          margin-left: calc(50% - 45vw);
          margin-right: calc(50% - 45vw);
          margin-top: 2rem;
          margin-bottom: 2rem;
        }
        
        .level-markers {
          display: flex;
          margin-bottom: 0.5rem;
          padding-left: 180px;
          position: relative;
          gap: 8px;
        }
        
        .level-marker {
          flex: 1;
          text-align: center;
          font-size: 0.9rem;
          font-weight: 600;
          color: #00d4ff;
          position: relative;
        }
        
        .level-marker::before {
          content: '';
          position: absolute;
          left: 0;
          top: 24px;
          width: 1px;
          height: 10px;
          background: rgba(255, 255, 255, 0.3);
        }
        
        .level-marker:last-child::after {
          content: '';
          position: absolute;
          right: 0;
          top: 24px;
          width: 1px;
          height: 10px;
          background: rgba(255, 255, 255, 0.3);
        }
        
        .language-row {
          display: flex;
          align-items: center;
          margin-bottom: 0.8rem;
          gap: 10px;
        }
        
        .language-label {
          min-width: 160px;
          font-weight: 600;
          color: #00d4ff;
          font-size: 1.05rem;
        }
        
        .language-note {
          display: block;
          font-size: 0.75rem;
          color: #888;
          margin-top: 2px;
        }
        
        .progress-container {
          flex: 1;
          height: 28px;
          background: rgba(0, 0, 0, 0.6);
          border: 1px solid #333;
          border-radius: 6px;
          position: relative;
          overflow: hidden;
        }
        
        .progress-bar {
          height: 100%;
          background: linear-gradient(90deg, #00d4ff 0%, #00a8cc 100%);
          box-shadow: 0 0 20px rgba(0, 212, 255, 0.6);
          transition: width 0.5s ease;
          position: relative;
        }
        
        .progress-bar::after {
          content: '';
          position: absolute;
          right: 0;
          top: 0;
          bottom: 0;
          width: 2px;
          background: rgba(0, 0, 0, 0.5);
        }
        
        .level-dividers {
          position: absolute;
          top: 0;
          left: 0;
          right: 0;
          bottom: 0;
          display: flex;
          pointer-events: none;
          gap: 8px;
        }
        
        .level-divider {
          flex: 1;
          border-left: 1px solid rgba(255, 255, 255, 0.15);
        }
        
        .level-divider:first-child {
          border-left: none;
        }
        </style>
        
        <div class="language-proficiency">
          <div class="level-markers">
            <div class="level-marker">A1</div>
            <div class="level-marker">A2</div>
            <div class="level-marker">B1</div>
            <div class="level-marker">B2</div>
            <div class="level-marker">C1</div>
            <div class="level-marker">C2</div>
          </div>
          
          <div class="language-row">
            <div class="language-label">
              Persian
              <span class="language-note">(mother tongue)</span>
            </div>
            <div class="progress-container">
              <div class="progress-bar" style="width: 100%;"></div>
              <div class="level-dividers">
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
              </div>
            </div>
          </div>
          
          <div class="language-row">
            <div class="language-label">
              Azeri
              <span class="language-note">(bilingual)</span>
            </div>
            <div class="progress-container">
              <div class="progress-bar" style="width: 100%;"></div>
              <div class="level-dividers">
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
              </div>
            </div>
          </div>
          
          <div class="language-row">
            <div class="language-label">English</div>
            <div class="progress-container">
              <div class="progress-bar" style="width: 100%;"></div>
              <div class="level-dividers">
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
              </div>
            </div>
          </div>
          
          <div class="language-row">
            <div class="language-label">Turkish</div>
            <div class="progress-container">
              <div class="progress-bar" style="width: 66.67%;"></div>
              <div class="level-dividers">
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
              </div>
            </div>
          </div>
          
          <div class="language-row">
            <div class="language-label">Dutch</div>
            <div class="progress-container">
              <div class="progress-bar" style="width: 50%;"></div>
              <div class="level-dividers">
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
              </div>
            </div>
          </div>
          
          <div class="language-row">
            <div class="language-label">French</div>
            <div class="progress-container">
              <div class="progress-bar" style="width: 50%;"></div>
              <div class="level-dividers">
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
                <div class="level-divider"></div>
              </div>
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
