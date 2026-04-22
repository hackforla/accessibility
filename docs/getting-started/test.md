# Test

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
        <div class="diagram-card-title"><span>📊</span> Audit Spreadsheet</div>
        <ul class="diagram-card-body">
          <li>Tracks pages audited</li>
          <li>Logs errors found</li>
          <li>Records PR links</li>
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
          <li>Initiative → Epics</li>
          <li>Fix issues → PRs</li>
          <li>Created &amp; managed by PM</li>
        </ul>
      </div>
    </div>

    <div class="diagram-relationships">
      <div class="diagram-group-label">How they connect</div>
      <div class="diagram-rel-grid">
        <div class="diagram-rel-item">
          <strong>PM <span class="diagram-rel-arrow">→</span> GitHub Issues</strong>
          Creates and manages all issues and epics
        </div>
        <div class="diagram-rel-item">
          <strong>Developer <span class="diagram-rel-arrow">→</span> WAVE Extension</strong>
          Runs audits on each page
        </div>
        <div class="diagram-rel-item">
          <strong>WAVE <span class="diagram-rel-arrow">→</span> Audit Spreadsheet</strong>
          Findings are logged per page
        </div>
        <div class="diagram-rel-item">
          <strong>Developer <span class="diagram-rel-arrow">→</span> Known Issues Index</strong>
          Documents new solutions for reuse
        </div>
        <div class="diagram-rel-item">
          <strong>Audit Spreadsheet <span class="diagram-rel-arrow">→</span> GitHub Issues</strong>
          Informs which issues to create
        </div>
        <div class="diagram-rel-item">
          <strong>Known Issues Index <span class="diagram-rel-arrow">→</span> GitHub Issues</strong>
          Referenced in every fix issue
        </div>
        <div class="diagram-rel-item">
          <strong>Developer <span class="diagram-rel-arrow">→</span> Audit Spreadsheet</strong>
          Logs findings and PR links
        </div>
        <div class="diagram-rel-item">
          <strong>Developer <span class="diagram-rel-arrow">→</span> GitHub Issues</strong>
          Closes issues via PRs
        </div>
      </div>
    </div>

  </div>
</div>

---

- Page Status: In Progress
- Current Authors: 
    - Bonnie Wolfe
