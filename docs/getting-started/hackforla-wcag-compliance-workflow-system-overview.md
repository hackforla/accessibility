# Compliance Workflow — System Overview

<style>
  .diagram {
    background: #ffffff;
    border: 1.5px solid #dde2ea;
    border-radius: 12px;
    padding: 40px 48px 48px;
    width: 100%;
    margin: 24px 0;
  }

  .diagram h2.diagram-title {
    font-family: monospace;
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: #7a8599;
    margin-bottom: 32px;
    padding-bottom: 16px;
    border-bottom: 1.5px solid #eaecf0;
  }

  .diagram-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 16px;
  }

  .diagram-group-label {
    font-family: monospace;
    font-size: 10px;
    font-weight: 500;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    margin-bottom: 10px;
  }

  .diagram-group {
    border-radius: 8px;
    padding: 18px;
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  .diagram-group.people    { background: #eef4ff; border: 1.5px solid #c5d8f8; }
  .diagram-group.people .diagram-group-label { color: #3b6ecf; }

  .diagram-group.tools     { background: #f0faf4; border: 1.5px solid #b6e4c8; }
  .diagram-group.tools .diagram-group-label { color: #2a7a50; }

  .diagram-group.artifacts { background: #fdf4ff; border: 1.5px solid #ddb8f5; }
  .diagram-group.artifacts .diagram-group-label { color: #7c3aaf; }

  .diagram-card {
    background: #ffffff;
    border-radius: 6px;
    padding: 14px 16px;
    border: 1.5px solid transparent;
    flex: 1;
  }

  .diagram-group.people .diagram-card    { border-color: #c5d8f8; }
  .diagram-group.tools .diagram-card     { border-color: #b6e4c8; }
  .diagram-group.artifacts .diagram-card { border-color: #ddb8f5; }

  .diagram-card-title {
    font-size: 13.5px;
    font-weight: 600;
    color: #1a1f2e;
    margin-bottom: 8px;
    display: flex;
    align-items: center;
    gap: 7px;
  }

  .diagram-card-body {
    font-size: 12px;
    color: #5a6478;
    line-height: 1.65;
    padding: 0;
    margin: 0;
  }

  .diagram-card-body li {
    list-style: none;
    padding-left: 12px;
    position: relative;
    margin: 0;
  }

  .diagram-card-body li::before {
    content: '–';
    position: absolute;
    left: 0;
    color: #a0aab8;
  }

  .diagram-relationships {
    grid-column: 1 / -1;
    background: #fafbfc;
    border: 1.5px solid #eaecf0;
    border-radius: 8px;
    padding: 18px 20px;
  }

  .diagram-relationships .diagram-group-label {
    color: #7a8599;
    margin-bottom: 12px;
  }

  .diagram-rel-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
  }

  .diagram-rel-item {
    background: #fff;
    border: 1.5px solid #eaecf0;
    border-radius: 6px;
    padding: 10px 12px;
    font-size: 11.5px;
    color: #3d4558;
    line-height: 1.5;
  }

  .diagram-rel-item strong {
    display: block;
    font-size: 11px;
    font-weight: 600;
    color: #1a1f2e;
    margin-bottom: 3px;
  }

  .diagram-rel-arrow {
    color: #a0aab8;
    font-size: 11px;
  }
</style>

<div class="diagram">
  <h2 class="diagram-title">WCAG Compliance Workflow — System Overview</h2>

  <div class="diagram-grid">

    <div class="diagram-group people">
      <div class="diagram-group-label">People</div>
      <div class="diagram-card">
        <div class="diagram-card-title"><span>👤</span> PM</div>
        <ul class="diagram-card-body">
          <li>Creates initiative &amp; epics</li>
          <li>Manages GitHub issues</li>
          <li>Tracks progress</li>
        </ul>
      </div>
      <div class="diagram-card">
        <div class="diagram-card-title"><span>👤</span> Developer</div>
        <ul class="diagram-card-body">
          <li>Runs WAVE audits</li>
          <li>Applies fixes</li>
          <li>Documents solutions</li>
        </ul>
      </div>
    </div>

    <div class="diagram-group tools">
      <div class="diagram-group-label">Tools</div>
      <div class="diagram-card">
        <div class="diagram-card-title"><span>🔍</span> WAVE Extension</div>
        <ul class="diagram-card-body">
          <li>Identifies errors &amp; alerts</li>
          <li>Flags contrast issues</li>
          <li>Run per page by developer</li>
        </ul>
      </div>
      <div class="diagram-card">
        <div class="diagram-card-title"><span>📁</span> Google Drive</div>
        <ul class="diagram-card-body">
          <li>Hosts Accessibility Project folder</li>
          <li>Stores both spreadsheets</li>
          <li>Shared across PM &amp; developers</li>
        </ul>
      </div>
    </div>

    <div class="diagram-group artifacts">
      <div class="diagram-group-label">Artifacts</div>
      <div class="diagram-card">
        <div class="diagram-card-title"><span>📖</span> Known Issues Index</div>
        <ul class="diagram-card-body">
          <li>Documents solutions</li>
          <li>Enables reuse across teams</li>
          <li>Updated by developers</li>
        </ul>
      </div>
      <div class="diagram-card">
        <div class="diagram-card-title"><span>🗂</span> GitHub Issues</div>
        <ul class="diagram-card-body">
          <li>Initiative → Epics 1–5</li>
          <li>Fix issues → PRs</li>
          <li>Created &amp; managed by PM</li>
        </ul>
      </div>
      <div class="diagram-card">
        <div class="diagram-card-title"><span>📋</span> Page Access by Role</div>
        <ul class="diagram-card-body">
          <li>Lists all pages &amp; global elements</li>
          <li>Maps user role permissions</li>
          <li>Created from template by PM</li>
        </ul>
      </div>
      <div class="diagram-card">
        <div class="diagram-card-title"><span>📊</span> Audit Spreadsheet</div>
        <ul class="diagram-card-body">
          <li>Created from template by PM</li>
          <li>Tracks pages, errors &amp; PRs</li>
          <li>Stored in Accessibility Project folder</li>
        </ul>
      </div>
    </div>

    <div class="diagram-relationships">
      <div class="diagram-group-label">How they connect</div>
      <div class="diagram-rel-grid" style="grid-template-columns: repeat(5, 1fr);">
        <div class="diagram-rel-item">
          <strong>PM <span class="diagram-rel-arrow">→</span> Google Drive</strong>
          Creates Accessibility Project folder &amp; spreadsheets from templates
        </div>
        <div class="diagram-rel-item">
          <strong>PM <span class="diagram-rel-arrow">→</span> GitHub Issues</strong>
          Creates Initiative, Epics 1–5, and all child issues
        </div>
        <div class="diagram-rel-item">
          <strong>Page Access by Role <span class="diagram-rel-arrow">→</span> Audit Spreadsheet</strong>
          Informs which pages &amp; roles to audit
        </div>
        <div class="diagram-rel-item">
          <strong>Developer <span class="diagram-rel-arrow">→</span> WAVE Extension</strong>
          Runs audits on each page
        </div>
        <div class="diagram-rel-item">
          <strong>WAVE <span class="diagram-rel-arrow">→</span> Audit Spreadsheet</strong>
          Findings logged per page by developer
        </div>
        <div class="diagram-rel-item">
          <strong>Audit Spreadsheet <span class="diagram-rel-arrow">→</span> GitHub Issues</strong>
          Informs which fix issues to create
        </div>
        <div class="diagram-rel-item">
          <strong>Developer <span class="diagram-rel-arrow">→</span> Known Issues Index</strong>
          Documents new solutions for reuse
        </div>
        <div class="diagram-rel-item">
          <strong>Known Issues Index <span class="diagram-rel-arrow">→</span> GitHub Issues</strong>
          Referenced in every fix issue
        </div>
        <div class="diagram-rel-item">
          <strong>Developer <span class="diagram-rel-arrow">→</span> Audit Spreadsheet</strong>
          Logs PR links on completion
        </div>
        <div class="diagram-rel-item">
          <strong>Developer <span class="diagram-rel-arrow">→</span> GitHub Issues</strong>
          Closes issues via PRs
        </div>
      </div>
    </div>

  </div>
</div>


<style>
  @import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@500&display=swap');

  * { box-sizing: border-box; margin: 0; padding: 0; }

  .flow-wrap {
    margin: 0;
  }

  .flow-title {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: #7a8599;
    margin-bottom: 32px;
    padding-bottom: 16px;
    border-bottom: 1.5px solid #dde2ea;
  }

  /* ── Connector line ── */
  .connector {
    width: 2px;
    height: 28px;
    background: #d0d5e0;
    margin: 0 auto;
  }

  .connector.branch {
    height: 16px;
  }

  /* ── Start / End pill ── */
  .node-pill {
    display: block;
    margin: 0 auto;
    width: fit-content;
    padding: 10px 32px;
    border-radius: 999px;
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 0.04em;
    text-align: center;
  }

  .node-pill.start { background: #ffffff; color: #1a1f2e; border: 2px solid #1a1f2e; }
  .node-pill.end   { background: #2a7a50; color: #fff; }

  /* ── Epic block ── */
  .epic {
    border-radius: 10px;
    overflow: hidden;
    border: 1.5px solid transparent;
  }

  .epic-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 14px 18px;
    cursor: pointer;
    user-select: none;
    gap: 12px;
  }

  .epic-header:hover { filter: brightness(0.97); }

  .epic-header-left {
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .epic-badge {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 10px;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    padding: 3px 8px;
    border-radius: 4px;
    white-space: nowrap;
  }

  .epic-title {
    font-size: 13.5px;
    font-weight: 600;
  }

  .epic-chevron {
    font-size: 12px;
    transition: transform 0.25s ease;
    flex-shrink: 0;
    color: inherit;
    opacity: 0.6;
  }

  .epic.open .epic-chevron { transform: rotate(180deg); }

  .epic-body {
    display: none;
    padding: 0 18px 18px;
    border-top: 1px solid rgba(0,0,0,0.06);
  }

  .epic.open .epic-body { display: block; }

  /* ── Step node ── */
  .step {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    padding: 10px 12px;
    border-radius: 6px;
    margin-top: 10px;
    font-size: 12.5px;
    line-height: 1.5;
    color: #2a2f3e;
  }

  .step-icon {
    font-size: 14px;
    flex-shrink: 0;
    margin-top: 1px;
  }

  /* ── Decision diamond ── */
  .decision-wrap {
    margin-top: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .decision {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 200px;
    height: 56px;
    background: #fff;
    border: 2px solid #d0d5e0;
    transform: rotate(0deg);
    position: relative;
    font-size: 12px;
    font-weight: 600;
    color: #2a2f3e;
    text-align: center;
    clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
    padding: 0 28px;
  }

  .decision-branches {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
    width: 100%;
    margin-top: 8px;
  }

  .branch {
    border-radius: 6px;
    padding: 10px 12px;
    font-size: 12px;
    line-height: 1.5;
    color: #2a2f3e;
  }

  .branch-label {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 10px;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 6px;
    display: block;
  }

  /* ── Loop indicator ── */
  .loop-badge {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    font-family: 'IBM Plex Mono', monospace;
    font-size: 10px;
    font-weight: 500;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    padding: 3px 9px;
    border-radius: 4px;
    margin-top: 10px;
    background: rgba(0,0,0,0.06);
    color: #5a6478;
  }

  /* ── Color themes per epic ── */
  /* epic color themes defined below */

  /* Initiative — Red */
  .epic.e0 { border-color: #f5b8b8; }
  .epic.e0 .epic-header { background: #fde8e8; color: #8a1a1a; }
  .epic.e0 .epic-badge  { background: #f5b8b8; color: #8a1a1a; }
  .epic.e0 .epic-body   { background: #fff5f5; }
  .epic.e0 .step        { background: #fde8e8; border: 1px solid #f5b8b8; }

  /* Epic 1 — Orange */
  .epic.e1 { border-color: #f5c89a; }
  .epic.e1 .epic-header { background: #fff0e0; color: #8a3d00; }
  .epic.e1 .epic-badge  { background: #f5c89a; color: #8a3d00; }
  .epic.e1 .epic-body   { background: #fff8f2; }
  .epic.e1 .step        { background: #fff0e0; border: 1px solid #f5c89a; }

  /* Epic 2 — Yellow */
  .epic.e2 { border-color: #e8d870; }
  .epic.e2 .epic-header { background: #fff8d6; color: #7a6000; }
  .epic.e2 .epic-badge  { background: #e8d870; color: #7a6000; }
  .epic.e2 .epic-body   { background: #fffde8; }
  .epic.e2 .step        { background: #fff8d6; border: 1px solid #e8d870; }

  /* Epic 3 — Cyan */
  .epic.e3 { border-color: #7ed4e0; }
  .epic.e3 .epic-header { background: #e0f7fa; color: #0e6b7a; }
  .epic.e3 .epic-badge  { background: #7ed4e0; color: #0e6b7a; }
  .epic.e3 .epic-body   { background: #f0fcff; }
  .epic.e3 .step        { background: #e0f7fa; border: 1px solid #7ed4e0; }

  /* Epic 4 — Blue */
  .epic.e4 { border-color: #94b8f0; }
  .epic.e4 .epic-header { background: #e8f0ff; color: #1a4a9a; }
  .epic.e4 .epic-badge  { background: #94b8f0; color: #1a4a9a; }
  .epic.e4 .epic-body   { background: #f4f8ff; }
  .epic.e4 .step        { background: #e8f0ff; border: 1px solid #94b8f0; }

  /* Epic 5 — Green */
  .epic.e5 { border-color: #7ed4a0; }
  .epic.e5 .epic-header { background: #e6f7ed; color: #1a6e3c; }
  .epic.e5 .epic-badge  { background: #7ed4a0; color: #1a6e3c; }
  .epic.e5 .epic-body   { background: #f2fdf6; }
  .epic.e5 .step        { background: #e6f7ed; border: 1px solid #7ed4a0; }

  /* decision & branch theming per epic */
  .epic.e0 .decision { border-color: #f5b8b8; }
  .epic.e0 .branch   { background: #fde8e8; border: 1px solid #f5b8b8; }
  .epic.e0 .branch-label { color: #8a1a1a; }

  .epic.e1 .decision { border-color: #f5c89a; }
  .epic.e1 .branch   { background: #fff0e0; border: 1px solid #f5c89a; }
  .epic.e1 .branch-label { color: #8a3d00; }

  .epic.e2 .decision { border-color: #e8d870; }
  .epic.e2 .branch   { background: #fff8d6; border: 1px solid #e8d870; }
  .epic.e2 .branch-label { color: #7a6000; }

  .epic.e3 .decision { border-color: #7ed4e0; }
  .epic.e3 .branch   { background: #e0f7fa; border: 1px solid #7ed4e0; }
  .epic.e3 .branch-label { color: #0e6b7a; }

  .epic.e4 .decision { border-color: #94b8f0; }
  .epic.e4 .branch   { background: #e8f0ff; border: 1px solid #94b8f0; }
  .epic.e4 .branch-label { color: #1a4a9a; }

  .epic.e5 .decision { border-color: #7ed4a0; }
  .epic.e5 .branch   { background: #e6f7ed; border: 1px solid #7ed4a0; }
  .epic.e5 .branch-label { color: #1a6e3c; }

  /* expand-all toggle */
  .toggle-all {
    display: flex;
    justify-content: flex-end;
    margin-bottom: 16px;
  }

  .toggle-all button {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    background: #fff;
    border: 1.5px solid #dde2ea;
    border-radius: 6px;
    padding: 6px 14px;
    cursor: pointer;
    color: #5a6478;
    transition: background 0.15s;
  }

  .toggle-all button:hover { background: #f0f2f6; }
</style>

<div class="flow-wrap">
  <div class="flow-title">WCAG Compliance Workflow — Process Flowchart</div>

  <div class="toggle-all">
    <button onclick="toggleAll()">Expand All</button>
  </div>

  <!-- START -->
  <span class="node-pill start">▶ Start: WCAG Compliance Initiative</span>
  <div class="connector"></div>

  <!-- INITIATIVE SETUP -->
  <div class="epic e0" id="epic0">
    <div class="epic-header" onclick="toggle('epic0')">
      <div class="epic-header-left">
        <span class="epic-badge">Initiative</span>
        <span class="epic-title">PM Setup</span>
      </div>
      <span class="epic-chevron">▼</span>
    </div>
    <div class="epic-body">
      <div class="step"><span class="step-icon">📁</span> Create "Accessibility Project" folder in team's Google Drive</div>
      <div class="step"><span class="step-icon">📊</span> Create <em>[PROJECT NAME] WAVE Accessibility Audit Spreadsheet</em> from template — save in Accessibility Project folder<br><small style="color:#7a8599;margin-top:4px;display:block;">Columns pre-named with data validation set up, no content</small></div>
      <div class="step"><span class="step-icon">📋</span> Create <em>Page Access by Role</em> spreadsheet from template — save in Accessibility Project folder<br><small style="color:#7a8599;margin-top:4px;display:block;">Lists all pages &amp; global features with user role permissions — team fills this out</small></div>
      <div class="step"><span class="step-icon">🗂</span> Create Epics 1–5 in GitHub and add each as a sub-issue to this Initiative</div>
    </div>
  </div>

  <div class="connector"></div>

  <!-- EPIC 1 -->
  <div class="epic e1" id="epic1">
    <div class="epic-header" onclick="toggle('epic1')">
      <div class="epic-header-left">
        <span class="epic-badge">Epic 1</span>
        <span class="epic-title">Initial Audit</span>
      </div>
      <span class="epic-chevron">▼</span>
    </div>
    <div class="epic-body">
      <div class="step"><span class="step-icon">📋</span> Inventory all pages &amp; recurring elements in spreadsheet</div>
      <div class="step"><span class="step-icon">🔍</span> Audit recurring elements (header, nav, footer) with WAVE</div>
      <div class="step"><span class="step-icon">📝</span> Document all errors &amp; alerts in spreadsheet</div>
      <div class="step"><span class="step-icon">✅</span> Epic 1 complete — hand off to PM</div>
    </div>
  </div>

  <div class="connector"></div>

  <!-- EPIC 2 -->
  <div class="epic e2" id="epic2">
    <div class="epic-header" onclick="toggle('epic2')">
      <div class="epic-header-left">
        <span class="epic-badge">Epic 2</span>
        <span class="epic-title">Recurring Element Remediation</span>
      </div>
      <span class="epic-chevron">▼</span>
    </div>
    <div class="epic-body">
      <div class="step"><span class="step-icon">🗂</span> PM creates one issue per recurring element with issues</div>
      <div class="step"><span class="step-icon">🔧</span> Dev reviews WAVE errors for element</div>
      <div class="step"><span class="step-icon">💡</span> Dev applies fix</div>
      <div class="decision-wrap">
        <div class="decision">More recurring elements?</div>
        <div class="decision-branches">
          <div class="branch">
            <span class="branch-label">↑ Yes</span>
            Return to top of Epic 2 loop
          </div>
          <div class="branch">
            <span class="branch-label">↓ No</span>
            Epic 2 complete
          </div>
        </div>
      </div>
      <span class="loop-badge">↻ Repeats per recurring element</span>
    </div>
  </div>

  <div class="connector"></div>

  <!-- EPIC 3 -->
  <div class="epic e3" id="epic3">
    <div class="epic-header" onclick="toggle('epic3')">
      <div class="epic-header-left">
        <span class="epic-badge">Epic 3</span>
        <span class="epic-title">Page Audits — Audit Only, No Fixes</span>
      </div>
      <span class="epic-chevron">▼</span>
    </div>
    <div class="epic-body">
      <div class="step"><span class="step-icon">🗂</span> PM creates one audit issue per page</div>
      <div class="step"><span class="step-icon">🔍</span> Dev runs WAVE extension on page</div>
      <div class="step"><span class="step-icon">📝</span> Dev documents errors &amp; alerts in spreadsheet</div>
      <div class="decision-wrap">
        <div class="decision">More pages?</div>
        <div class="decision-branches">
          <div class="branch">
            <span class="branch-label">↑ Yes</span>
            Return to top of Epic 3 loop
          </div>
          <div class="branch">
            <span class="branch-label">↓ No</span>
            Epic 3 complete
          </div>
        </div>
      </div>
      <span class="loop-badge">↻ Repeats per page</span>
    </div>
  </div>

  <div class="connector"></div>

  <!-- EPIC 4 -->
  <div class="epic e4" id="epic4">
    <div class="epic-header" onclick="toggle('epic4')">
      <div class="epic-header-left">
        <span class="epic-badge">Epic 4</span>
        <span class="epic-title">Error &amp; Alert Fixes — Epic of Epics</span>
      </div>
      <span class="epic-chevron">▼</span>
    </div>
    <div class="epic-body">
      <div class="step"><span class="step-icon">🗂</span> PM creates one fix epic per WAVE error/alert type</div>
      <div class="decision-wrap">
        <div class="decision">Solution exists in Known Issues index?</div>
        <div class="decision-branches">
          <div class="branch">
            <span class="branch-label">✓ Yes</span>
            PM creates fix issue per affected page → Dev reviews existing solution → Dev applies solution → PR submitted
          </div>
          <div class="branch">
            <span class="branch-label">✗ No</span>
            PM creates document+fix issue for first page → Dev researches &amp; develops solution → Dev applies to first page → Dev documents solution in Known Issues index → remaining pages follow the Yes branch
          </div>
        </div>
      </div>
      <div class="decision-wrap">
        <div class="decision">More pages for this error?</div>
        <div class="decision-branches">
          <div class="branch">
            <span class="branch-label">↑ Yes</span>
            Create fix issue for next page
          </div>
          <div class="branch">
            <span class="branch-label">↓ No</span>
            Check for more error types
          </div>
        </div>
      </div>
      <div class="decision-wrap">
        <div class="decision">More error types?</div>
        <div class="decision-branches">
          <div class="branch">
            <span class="branch-label">↑ Yes</span>
            Return to top of Epic 4 loop
          </div>
          <div class="branch">
            <span class="branch-label">↓ No</span>
            Epic 4 complete
          </div>
        </div>
      </div>
      <span class="loop-badge">↻ Repeats per error type and per page</span>
    </div>
  </div>

  <div class="connector"></div>

  <!-- EPIC 5 -->
  <div class="epic e5" id="epic5">
    <div class="epic-header" onclick="toggle('epic5')">
      <div class="epic-header-left">
        <span class="epic-badge">Epic 5</span>
        <span class="epic-title">Ongoing Audit Cycle — Validation &amp; Re-Audit</span>
      </div>
      <span class="epic-chevron">▼</span>
    </div>
    <div class="epic-body">
      <div class="step"><span class="step-icon">🔍</span> Dev re-audits all pages with WAVE</div>
      <div class="decision-wrap">
        <div class="decision">Errors found?</div>
        <div class="decision-branches">
          <div class="branch">
            <span class="branch-label">✗ No</span>
            Epic 5 becomes final audit &amp; sign-off → Initiative complete
          </div>
          <div class="branch">
            <span class="branch-label">✓ Yes</span>
            PM creates new issues for affected pages → Return to Epic 3 &amp; Epic 4 workflow
          </div>
        </div>
      </div>
      <span class="loop-badge">↻ Repeats until no errors remain</span>
    </div>
  </div>

  <div class="connector"></div>

  <!-- END -->
  <span class="node-pill end">✓ Initiative Complete — Final Sign-Off</span>

</div>

<script>
  function toggle(id) {
    const el = document.getElementById(id);
    el.classList.toggle('open');
    updateToggleBtn();
  }

  function toggleAll() {
    const epics = document.querySelectorAll('.epic');
    const allOpen = [...epics].every(e => e.classList.contains('open'));
    epics.forEach(e => allOpen ? e.classList.remove('open') : e.classList.add('open'));
    updateToggleBtn();
  }

  function updateToggleBtn() {
    const epics = document.querySelectorAll('.epic');
    const allOpen = [...epics].every(e => e.classList.contains('open'));
    document.querySelector('.toggle-all button').textContent = allOpen ? 'Collapse All' : 'Expand All';
  }
</script>

---

- Page Status: In Progress
- Current Authors: 
    - Bonnie Wolfe
