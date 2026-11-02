---
title: Publications
cms_exclude: true

# View.
view: citation

# Optional header image (relative to `static/media/` folder).
banner:
  caption: ''
  image: ''
---

<div class="gs-tab-nav" role="tablist" aria-label="Publications and Software Tabs" style="margin-top: 2rem;">
  <button id="btn-publications" class="gs-tab-btn active" role="tab" aria-selected="true" aria-controls="pane-publications" onclick="pubSwitchTab('publications', true)">📄 Publications</button>
  <button id="btn-software" class="gs-tab-btn" role="tab" aria-selected="false" aria-controls="pane-software" onclick="pubSwitchTab('software', true)">💻 Software &amp; Data</button>
</div>

<div id="pane-software" class="gs-tab-pane" role="tabpanel" aria-labelledby="btn-software">
  <p style="font-size: 1rem; color: #cbd5e1; margin-bottom: 1.5rem;"><em>I release the code and data behind my papers under open licenses so that results can be reproduced and reused.</em></p>

  <div class="gs-table-wrap">
    <table class="gs-partner-table">
      <thead>
        <tr>
          <th>Name</th>
          <th>Description</th>
          <th>License</th>
          <th>Link</th>
          <th>Related paper</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>HDLMF_GIN-GA</strong></td>
          <td>Hybrid deep-learning–metaheuristic framework: a graph neural network surrogate inside a genetic algorithm for bi-level network design</td>
          <td>MIT</td>
          <td><a href="https://github.com/bahmanmdd/HDLMF_GIN-GA" target="_blank" rel="noopener">GitHub</a></td>
          <td><a href="/publications/j2024-hybrid-dl/">ESWA 2024</a></td>
        </tr>
        <tr>
          <td><strong>Equilibrium-Traffic-Networks</strong></td>
          <td>Three benchmark datasets of traffic networks with user-equilibrium solutions, for training and testing surrogate models</td>
          <td>CC BY 4.0</td>
          <td><a href="https://doi.org/10.6084/m9.figshare.27889251" target="_blank" rel="noopener">Figshare</a></td>
          <td><a href="/publications/j2024-hybrid-dl/">ESWA 2024</a></td>
        </tr>
        <tr>
          <td><strong>MOST</strong></td>
          <td>LLM-based pipeline that measures the availability of code and data in transportation research papers (developed within RERITE)</td>
          <td>Apache-2.0</td>
          <td><a href="https://github.com/RRinTransportation/OpenMOST" target="_blank" rel="noopener">GitHub</a></td>
          <td><a href="/publications/j2027-open-science-llm/">TR-C 2026</a></td>
        </tr>
        <tr>
          <td><strong>TOD_simulation</strong></td>
          <td>Agent-based discrete event simulation of teleoperated truck driving, used for fleet sizing</td>
          <td>MIT</td>
          <td><a href="https://github.com/bahmanmdd/TOD_simulation" target="_blank" rel="noopener">GitHub</a></td>
          <td><a href="/publications/j2026-trip/">TRIP 2026</a></td>
        </tr>
        <tr>
          <td><strong>GINGA-mini</strong></td>
          <td>Teaching mini-projects on graph neural networks and genetic algorithms for network design (ENS de Lyon transport week, 2025)</td>
          <td>MIT</td>
          <td><a href="https://github.com/bahmanmdd/GINGA-mini" target="_blank" rel="noopener">GitHub</a></td>
          <td>–</td>
        </tr>
        <tr>
          <td><strong>DAP</strong></td>
          <td>Java implementation of simultaneous perturbation stochastic approximation (SPSA) for anchorage planning</td>
          <td></td>
          <td><a href="https://github.com/bahmanmdd/DAP" target="_blank" rel="noopener">GitHub</a></td>
          <td><a href="/publications/j2020-anchorage/">ESWA 2020</a></td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<script>
function pubSwitchTab(tabId, updateUrl) {
  var validTabs = ['publications', 'software'];
  if (validTabs.indexOf(tabId) === -1) return;
  document.querySelectorAll('.gs-tab-btn').forEach(function(btn) {
    btn.classList.remove('active');
    btn.setAttribute('aria-selected', 'false');
  });
  var targetBtn = document.getElementById('btn-' + tabId);
  var softwarePane = document.getElementById('pane-software');
  var pubListContainer = document.querySelector('.page-body > .flex.flex-col.items-center');
  if (targetBtn) {
    targetBtn.classList.add('active');
    targetBtn.setAttribute('aria-selected', 'true');
  }
  if (tabId === 'software') {
    if (softwarePane) softwarePane.classList.add('active');
    if (pubListContainer) pubListContainer.style.display = 'none';
  } else {
    if (softwarePane) softwarePane.classList.remove('active');
    if (pubListContainer) pubListContainer.style.display = 'flex';
  }
  if (updateUrl && window.history && window.history.replaceState) {
    var newHash = tabId === 'publications' ? window.location.pathname : '#' + tabId;
    window.history.replaceState(null, '', newHash);
  }
}
function pubInitTabFromHash() {
  var pubListContainer = document.querySelector('.page-body > .flex.flex-col.items-center > div');
  if (pubListContainer) {
    pubListContainer.style.marginTop = '1rem';
  }
  var hash = (window.location.hash || '').replace(/^#/, '').toLowerCase();
  if (hash) {
    pubSwitchTab(hash, false);
  }
}
if (document.readyState === 'loading') {
  document.addEventListener('DOMContentLoaded', pubInitTabFromHash);
} else {
  pubInitTabFromHash();
}
window.addEventListener('hashchange', pubInitTabFromHash);
</script>
