---
title: "GREENSHIFT"
linkTitle: "GREENSHIFT"
summary: "GREEN Roadmap for Sustainable Hubs and Integrated Future Transport — ANR JCJC Research Project (2027–2031)"
date: '2026-08-18'
type: landing
aliases:
  - /projects/greenshift/
  - /project/greenshift/

design:
  spacing: '3rem'

sections:
  - block: markdown
    content:
      title: ""
      text: |
        <style>
        .gs-container {
          width: 100%;
          font-family: inherit;
        }
        .gs-header {
          margin-bottom: 2rem;
        }
        .gs-title {
          font-size: 2.3rem;
          font-weight: 800;
          margin-bottom: 0.5rem;
          background: linear-gradient(135deg, #00d4ff 0%, #10b981 100%);
          -webkit-background-clip: text;
          -webkit-text-fill-color: transparent;
        }
        .gs-subtitle {
          font-size: 1.15rem;
          color: #cbd5e1;
          margin-bottom: 1.25rem;
          font-weight: 500;
        }
        .gs-badges {
          display: flex;
          gap: 0.6rem;
          flex-wrap: wrap;
          margin-bottom: 1.5rem;
        }
        .gs-badge {
          display: inline-flex;
          align-items: center;
          padding: 0.35rem 0.85rem;
          border-radius: 9999px;
          font-size: 0.825rem;
          font-weight: 600;
          letter-spacing: 0.02em;
        }
        .gs-badge-cyan {
          background: rgba(0, 212, 255, 0.12);
          color: #00d4ff;
          border: 1px solid rgba(0, 212, 255, 0.35);
        }
        .gs-badge-green {
          background: rgba(16, 185, 129, 0.12);
          color: #10b981;
          border: 1px solid rgba(16, 185, 129, 0.35);
        }
        .gs-badge-purple {
          background: rgba(168, 85, 247, 0.12);
          color: #c084fc;
          border: 1px solid rgba(168, 85, 247, 0.35);
        }

        /* Tab Navigation */
        .gs-tab-nav {
          display: flex;
          gap: 0.5rem;
          border-bottom: 2px solid rgba(255, 255, 255, 0.1);
          padding-bottom: 0;
          margin-bottom: 2rem;
          overflow-x: auto;
          scrollbar-width: none;
        }
        .gs-tab-nav::-webkit-scrollbar {
          display: none;
        }
        .gs-tab-btn {
          display: inline-flex;
          align-items: center;
          gap: 0.4rem;
          padding: 0.75rem 1.2rem;
          font-size: 0.95rem;
          font-weight: 600;
          color: #94a3b8;
          cursor: pointer;
          background: transparent;
          border: none;
          border-bottom: 3px solid transparent;
          margin-bottom: -2px;
          white-space: nowrap;
          transition: all 0.2s ease-in-out;
          border-radius: 6px 6px 0 0;
        }
        .gs-tab-btn:hover {
          color: #f1f5f9;
          background: rgba(255, 255, 255, 0.04);
        }
        .gs-tab-btn.active {
          color: #00d4ff !important;
          border-bottom-color: #00d4ff !important;
          background: rgba(0, 212, 255, 0.08) !important;
        }

        /* Tab Panes */
        .gs-tab-pane {
          display: none;
        }
        .gs-tab-pane.active {
          display: block;
          animation: gsFadeIn 0.25s ease-in-out forwards;
        }

        @keyframes gsFadeIn {
          from { opacity: 0; transform: translateY(4px); }
          to { opacity: 1; transform: translateY(0); }
        }

        /* Card Grid & Cards */
        .gs-card-grid {
          display: grid;
          grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
          gap: 1.25rem;
          margin: 1.5rem 0;
        }
        .gs-card {
          background: rgba(255, 255, 255, 0.03);
          border: 1px solid rgba(255, 255, 255, 0.08);
          border-radius: 12px;
          padding: 1.35rem;
          transition: transform 0.2s ease, border-color 0.2s ease, box-shadow 0.2s ease;
        }
        .gs-card:hover {
          transform: translateY(-2px);
          border-color: rgba(0, 212, 255, 0.3);
          box-shadow: 0 8px 24px rgba(0, 0, 0, 0.25);
        }
        .gs-card-tag {
          display: inline-block;
          font-size: 0.75rem;
          font-weight: 700;
          text-transform: uppercase;
          letter-spacing: 0.05em;
          color: #00d4ff;
          margin-bottom: 0.5rem;
        }
        .gs-card-title {
          font-size: 1.1rem;
          font-weight: 700;
          margin-bottom: 0.6rem;
          color: #f8fafc;
        }
        .gs-card p {
          font-size: 0.925rem;
          color: #94a3b8;
          line-height: 1.55;
          margin: 0;
        }

        /* Table */
        .gs-table-wrap {
          width: 100%;
          overflow-x: auto;
          -webkit-overflow-scrolling: touch;
        }
        .gs-partner-table {
          width: 100%;
          min-width: 500px;
          border-collapse: collapse;
          margin: 1.5rem 0;
        }
        .gs-partner-table th, .gs-partner-table td {
          padding: 0.85rem 1rem;
          border-bottom: 1px solid rgba(255, 255, 255, 0.08);
          text-align: left;
          font-size: 0.925rem;
        }
        .gs-partner-table th {
          color: #00d4ff;
          font-weight: 600;
          background: rgba(255, 255, 255, 0.02);
        }

        /* Mobile responsiveness */
        @media (max-width: 600px) {
          .gs-card-grid {
            grid-template-columns: 1fr;
          }
          .gs-title {
            font-size: 1.8rem;
          }
          .gs-tab-btn {
            padding: 0.6rem 0.85rem;
            font-size: 0.85rem;
          }
        }

        /* Timeline */
        .gs-timeline {
          border-left: 2px solid rgba(0, 212, 255, 0.3);
          padding-left: 1.25rem;
          margin: 1.5rem 0;
        }
        .gs-timeline-item {
          position: relative;
          margin-bottom: 1.5rem;
        }
        .gs-timeline-item::before {
          content: '';
          position: absolute;
          left: -1.65rem;
          top: 0.35rem;
          width: 10px;
          height: 10px;
          border-radius: 50%;
          background: #00d4ff;
          box-shadow: 0 0 8px #00d4ff;
        }
        .gs-timeline-date {
          font-size: 0.85rem;
          font-weight: 700;
          color: #00d4ff;
          margin-bottom: 0.25rem;
        }
        </style>

        <div class="gs-container">

        <div class="gs-header">
          <div class="gs-title">GREENSHIFT</div>
          <div class="gs-subtitle">GREEN Roadmap for Sustainable Hubs and Integrated Future Transport</div>
          <div class="gs-badges">
            <span class="gs-badge gs-badge-cyan">🏛️ ANR JCJC 2026</span>
            <span class="gs-badge gs-badge-green">⏱️ 48 Months (Feb 2027 – Jan 2031)</span>
            <span class="gs-badge gs-badge-purple">👤 PI & Coordinator: Dr. Bahman Madadi (ENTPE)</span>
          </div>
        </div>

        <div class="gs-tab-nav">
          <button id="btn-overview" class="gs-tab-btn active" onclick="gsSwitchTab('overview')">🌿 Overview & Objectives</button>
          <button id="btn-wps" class="gs-tab-btn" onclick="gsSwitchTab('wps')">🔬 Work Packages</button>
          <button id="btn-team" class="gs-tab-btn" onclick="gsSwitchTab('team')">🤝 Consortium & Partners</button>
          <button id="btn-outputs" class="gs-tab-btn" onclick="gsSwitchTab('outputs')">💡 Expected Outputs</button>
          <button id="btn-news" class="gs-tab-btn" onclick="gsSwitchTab('news')">📢 News & Milestones</button>
        </div>

        <div id="pane-overview" class="gs-tab-pane active">
          <h3>Vision & Context</h3>
          <p>Electric vehicles (EVs) eliminate tailpipe emissions and are a cornerstone of transport decarbonization; however, widespread EV adoption alone cannot overcome urban spatial capacity limits, energy peak demands, or transport inequities. Their full potential is unlocked when integrated into a diverse, shared, and interconnected mobility ecosystem.</p>
          <p><strong>GREENSHIFT</strong> aims to determine detailed scientific and operational requirements for deploying an optimized network of <strong>multimodal mobility hubs</strong>—consolidating public transport, shared EVs, (e-)bicycles, micromobility, and fast charging in dedicated physical spaces. Co-designed with designated <strong>Zero-Emission Zones (ZEZs)</strong> and equity-sensitive incentive policies, GREENSHIFT establishes a validated simulation-optimization framework and interactive decision-support tools for an inclusive transition toward sustainable urban mobility.</p>

          <h3 style="margin-top: 2rem;">Core Research Objectives</h3>
          <div class="gs-card-grid">
            <div class="gs-card">
              <span class="gs-card-tag">Objective 1</span>
              <div class="gs-card-title">Infrastructure Optimization (RO1)</div>
              <p>Develop an integrated simulation-optimization framework combining multi-agent behavioral modeling with physics-informed graph neural network (PIGNN) surrogates and active learning to optimize hub network design at city scale.</p>
            </div>
            <div class="gs-card">
              <span class="gs-card-tag">Objective 2</span>
              <div class="gs-card-title">Incentives & Policy Design (RO2)</div>
              <p>Analyze and optimize multi-instrument incentive packages (e.g., dynamic pricing, tradable credit schemes, gamification, and targeted subsidies) interacting with ZEZ/LEZ access regulations to steer travel behavior while protecting vulnerable populations.</p>
            </div>
            <div class="gs-card">
              <span class="gs-card-tag">Objective 3</span>
              <div class="gs-card-title">Inclusive Transition Roadmaps (RO3)</div>
              <p>Design a participatory transition methodology combining quantitative transport models with Q-methodology and open-source interactive decision-support dashboards to build institutional legitimacy and public consensus.</p>
            </div>
          </div>
        </div>

        <div id="pane-wps" class="gs-tab-pane">
          <p>The project follows an incremental, cascading scientific structure coordinated from Lyon (primary continuous testbed) with international partner validation:</p>
          <div class="gs-card-grid">
            <div class="gs-card">
              <span class="gs-card-tag">WP0 · Management & Dissemination</span>
              <div class="gs-card-title">Project Management & Open Science</div>
              <p><strong>Lead:</strong> Dr. Bahman Madadi (ENTPE)<br>Coordinates project activities, operational continuity, ethics, FAIR data management (DMP OPIDoR), open-source releases, and scientific communication.</p>
            </div>
            <div class="gs-card">
              <span class="gs-card-tag">WP1 · Infrastructure AI & Optimization</span>
              <div class="gs-card-title">Simulation-Based Hub Optimization</div>
              <p><strong>Lead:</strong> Dr. Bahman Madadi (ENTPE)<br><strong>Partners:</strong> ENTPE, UGE, TU Delft<br>Combines dynamic agent-based multimodal choice modeling with Physics-Informed Graph Neural Network (PIGNN) surrogates and active learning for scalable network design.</p>
            </div>
            <div class="gs-card">
              <span class="gs-card-tag">WP2 · Behavioral Economics & Equity</span>
              <div class="gs-card-title">Multi-Instrument Incentive Strategies</div>
              <p><strong>Lead:</strong> Dr. Bahman Madadi (ENTPE)<br><strong>Partners:</strong> ENTPE, UGE, University of Luxembourg<br>Investigates coordinated bundles of push (ZEZ restrictions) and pull (pricing, tradable credit schemes, gamification) instruments, ensuring mobility equity for vulnerable groups.</p>
            </div>
            <div class="gs-card">
              <span class="gs-card-tag">WP3 · Governance & Transition</span>
              <div class="gs-card-title">Inclusive Transition Strategies</div>
              <p><strong>Lead:</strong> Dr. Bahman Madadi (ENTPE)<br><strong>Partners:</strong> ENTPE, UGE, DLR (German Aerospace Center)<br>Bridges quantitative models with participatory Q-methodology and interactive dashboards to co-create consensus-driven transition roadmaps with stakeholders.</p>
            </div>
          </div>
        </div>

        <div id="pane-team" class="gs-tab-pane">
          <h3>Academic Consortium</h3>
          <div class="gs-table-wrap">
          <table class="gs-partner-table">
            <thead>
              <tr>
                <th>Institution</th>
                <th>Key Contributors</th>
                <th>Core Contribution</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td><strong>ENTPE / E-Mob Lab (Host)</strong></td>
                <td>Dr. Bahman Madadi (Coordinator/PI)<br>Dr. Angelo Furno<br>Dr. Christine Buisson</td>
                <td>Project Coordination, AI/Surrogate Optimization, Stakeholder Engagement</td>
              </tr>
              <tr>
                <td><strong>Université Gustave Eiffel (UGE)</strong></td>
                <td>Dr. Ludovic Leclercq<br>Dr. Nour-Eddin El Faouzi</td>
                <td>Dynamic Traffic Modeling, Behavioral Incentives, Regional Mobility Policy</td>
              </tr>
              <tr>
                <td><strong>TU Delft (Netherlands)</strong></td>
                <td>Dr. Shadi Sharif Azadeh (SUM Lab)<br>Dr. Gonçalo Correia (hEAT Lab)</td>
                <td>Operations Research, Multimodal Hub Optimization, European Validation</td>
              </tr>
              <tr>
                <td><strong>University of Luxembourg</strong></td>
                <td>Prof. Francesco Viti (MobiLab)</td>
                <td>Mobility Behavior, Decision-Support Systems, Transferability Analysis</td>
              </tr>
              <tr>
                <td><strong>German Aerospace Center (DLR)</strong></td>
                <td>Dr. Dimitris Milakis</td>
                <td>Societal Acceptance, Qualitative Q-Methodology, Policy Governance</td>
              </tr>
            </tbody>
          </table></div>

          <h3 style="margin-top: 2rem;">Stakeholder & Ecosystem Partners</h3>
          <p>Collaborations with regional and national stakeholders include <strong>CARA European Cluster for Mobility Solutions</strong>, <strong>CEREMA</strong>, and <strong>SYTRAL Mobilités</strong> to facilitate public participation and real-world deployment roadmaps.</p>
        </div>

        <div id="pane-outputs" class="gs-tab-pane">
          <div class="gs-card-grid">
            <div class="gs-card">
              <span class="gs-card-tag">Output EO1</span>
              <div class="gs-card-title">Scalable Optimization Engine</div>
              <p>An open-source, scalable simulation-optimization framework combining MnMS with PIGNNs for city-scale mobility hub planning.</p>
            </div>
            <div class="gs-card">
              <span class="gs-card-tag">Output EO2</span>
              <div class="gs-card-title">Incentive & Equity Toolkit</div>
              <p>A validated methodology and toolset for designing and evaluating equity-constrained incentive packages interacting with ZEZs.</p>
            </div>
            <div class="gs-card">
              <span class="gs-card-tag">Output EO3</span>
              <div class="gs-card-title">Decision-Support Tool</div>
              <p>An open-source, interactive dashboard and validated transition roadmap enabling planners to explore progressive hub deployment scenarios.</p>
            </div>
            <div class="gs-card">
              <span class="gs-card-tag">Output EO4</span>
              <div class="gs-card-title">Open Science & Publications</div>
              <p>Peer-reviewed articles in top open-access journals (CC-BY), open datasets on <em>recherche.data.gouv.fr</em>, and open software on GitHub.</p>
            </div>
          </div>
        </div>

        <div id="pane-news" class="gs-tab-pane">
          <div class="gs-timeline">
            <div class="gs-timeline-item">
              <div class="gs-timeline-date">August 2026</div>
              <div style="font-weight: 600; color: #f1f5f9;">Grant Acceptance Announcement</div>
              <p style="font-size: 0.925rem; color: #94a3b8; margin-top: 0.25rem;">
                🎉 <strong>GREENSHIFT</strong> is officially accepted for funding under the French National Research Agency (ANR) <strong>2026 AAPG (JCJC)</strong> call under Theme H.18.
              </p>
            </div>
            <div class="gs-timeline-item">
              <div class="gs-timeline-date">February 2027</div>
              <div style="font-weight: 600; color: #f1f5f9;">Official Project Kickoff</div>
              <p style="font-size: 0.925rem; color: #94a3b8; margin-top: 0.25rem;">
                Official project launch and recruitment kickoff for Postdoctoral researchers and PhD candidates.
              </p>
            </div>
          </div>
        </div>

        </div>

        <script>
        function gsSwitchTab(tabId) {
          document.querySelectorAll('.gs-tab-btn').forEach(function(btn) {
            btn.classList.remove('active');
          });
          document.querySelectorAll('.gs-tab-pane').forEach(function(pane) {
            pane.classList.remove('active');
          });
          var targetBtn = document.getElementById('btn-' + tabId);
          var targetPane = document.getElementById('pane-' + tabId);
          if (targetBtn && targetPane) {
            targetBtn.classList.add('active');
            targetPane.classList.add('active');
          }
        }
        </script>
    design:
      columns: '1'
---
