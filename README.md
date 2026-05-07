<svg xmlns="http://www.w3.org/2000/svg" width="860" height="440" viewBox="0 0 860 440">
<defs>
  <style>
    text { font-family: "JetBrains Mono", "Fira Mono", monospace; }
    .bg { fill: #0d1117; }
    .surface { fill: #161b22; }
    .border-col { stroke: #21262d; fill: none; }
    .muted { fill: #8b949e; }
    .faint { fill: #3d444d; }
    .txt { fill: #e6edf3; }
    .green { fill: #3fb950; }
    .blue { fill: #58a6ff; }
    .purple { fill: #bc8cff; }
    .orange { fill: #d29922; }
    .teal { fill: #39d5c3; }
    .red { fill: #f85149; }
    .s-green { stroke: #3fb950; fill: none; }
    .s-blue { stroke: #58a6ff; fill: none; }
    .s-border { stroke: #21262d; fill: #161b22; }

    .stage { opacity: 0; }

    .s0 { animation: stg0 45s linear infinite; }
    @keyframes stg0 {
      0%      { opacity: 1; }
      11.1%   { opacity: 1; }
      13.3%   { opacity: 0; }
      100%    { opacity: 0; }
    }

    .s1 { animation: stg1 45s linear infinite; }
    @keyframes stg1 {
      0%      { opacity: 0; }
      10%     { opacity: 0; }
      11.1%   { opacity: 1; }
      22.2%   { opacity: 1; }
      24.4%   { opacity: 0; }
      100%    { opacity: 0; }
    }

    .s2 { animation: stg2 45s linear infinite; }
    @keyframes stg2 {
      0%,22.2%  { opacity: 0; }
      22.3%     { opacity: 1; }
      33.3%     { opacity: 1; }
      35.5%     { opacity: 0; }
      100%      { opacity: 0; }
    }

    .s3 { animation: stg3 45s linear infinite; }
    @keyframes stg3 {
      0%,33.3%  { opacity: 0; }
      33.4%     { opacity: 1; }
      44.4%     { opacity: 1; }
      46.6%     { opacity: 0; }
      100%      { opacity: 0; }
    }

    .s4 { animation: stg4 45s linear infinite; }
    @keyframes stg4 {
      0%,44.4%  { opacity: 0; }
      44.5%     { opacity: 1; }
      55.5%     { opacity: 1; }
      57.7%     { opacity: 0; }
      100%      { opacity: 0; }
    }

    .s5 { animation: stg5 45s linear infinite; }
    @keyframes stg5 {
      0%,55.5%  { opacity: 0; }
      55.6%     { opacity: 1; }
      66.6%     { opacity: 1; }
      68.8%     { opacity: 0; }
      100%      { opacity: 0; }
    }

    .s6 { animation: stg6 45s linear infinite; }
    @keyframes stg6 {
      0%,66.6%  { opacity: 0; }
      66.7%     { opacity: 1; }
      77.7%     { opacity: 1; }
      79.9%     { opacity: 0; }
      100%      { opacity: 0; }
    }

    .s7 { animation: stg7 45s linear infinite; }
    @keyframes stg7 {
      0%,77.7%  { opacity: 0; }
      77.8%     { opacity: 1; }
      88.8%     { opacity: 1; }
      91%       { opacity: 0; }
      100%      { opacity: 0; }
    }

    .s8 { animation: stg8 45s linear infinite; }
    @keyframes stg8 {
      0%,88.8%  { opacity: 0; }
      88.9%     { opacity: 1; }
      100%      { opacity: 1; }
    }

    .bar-anim { stroke-linecap: round; }
    .blink { animation: blink 1s step-end infinite; }
    @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }
    .pulse { animation: pulse 2s ease-in-out infinite; }
    @keyframes pulse { 0%,100%{opacity:1} 50%{opacity:.3} }
    .pt { animation: ptfade 3s ease-out forwards; }
    @keyframes ptfade { from{opacity:0} to{opacity:0.7} }

    .regline {
      stroke: #3fb950; stroke-width: 2; fill: none;
      stroke-dasharray: 700; stroke-dashoffset: 700;
      animation: drawline 45s linear infinite;
    }
    @keyframes drawline {
      0%,8.8%  { stroke-dashoffset: 700; opacity: 0; }
      9%       { opacity: 1; }
      11.1%    { stroke-dashoffset: 0; opacity: 1; }
      13.3%    { stroke-dashoffset: 0; opacity: 0; }
      100%     { stroke-dashoffset: 0; opacity: 0; }
    }

    .qline { opacity: 0; }
    .ql0  { animation: qshow 45s linear infinite; }
    .ql1  { animation: qshow1 45s linear infinite; }
    .ql2  { animation: qshow2 45s linear infinite; }
    .ql3  { animation: qshow3 45s linear infinite; }
    .ql4  { animation: qshow4 45s linear infinite; }
    .ql5  { animation: qshow5 45s linear infinite; }
    .ql6  { animation: qshow6 45s linear infinite; }
    .ql7  { animation: qshow7 45s linear infinite; }
    .ql8  { animation: qshow8 45s linear infinite; }
    .ql9  { animation: qshow9 45s linear infinite; }
    .ql10 { animation: qshow10 45s linear infinite; }

    @keyframes qshow   { 0%,22.2%{opacity:0} 22.5%{opacity:1} 35.5%{opacity:1} 36%{opacity:0} 100%{opacity:0} }
    @keyframes qshow1  { 0%,22.8%{opacity:0} 23.1%{opacity:1} 35.5%{opacity:1} 36%{opacity:0} 100%{opacity:0} }
    @keyframes qshow2  { 0%,23.4%{opacity:0} 23.7%{opacity:1} 35.5%{opacity:1} 36%{opacity:0} 100%{opacity:0} }
    @keyframes qshow3  { 0%,24%  {opacity:0} 24.3%{opacity:1} 35.5%{opacity:1} 36%{opacity:0} 100%{opacity:0} }
    @keyframes qshow4  { 0%,24.6%{opacity:0} 24.9%{opacity:1} 35.5%{opacity:1} 36%{opacity:0} 100%{opacity:0} }
    @keyframes qshow5  { 0%,25.2%{opacity:0} 25.5%{opacity:1} 35.5%{opacity:1} 36%{opacity:0} 100%{opacity:0} }
    @keyframes qshow6  { 0%,25.8%{opacity:0} 26.1%{opacity:1} 35.5%{opacity:1} 36%{opacity:0} 100%{opacity:0} }
    @keyframes qshow7  { 0%,26.4%{opacity:0} 26.7%{opacity:1} 35.5%{opacity:1} 36%{opacity:0} 100%{opacity:0} }
    @keyframes qshow8  { 0%,27%  {opacity:0} 27.3%{opacity:1} 35.5%{opacity:1} 36%{opacity:0} 100%{opacity:0} }
    @keyframes qshow9  { 0%,27.6%{opacity:0} 27.9%{opacity:1} 35.5%{opacity:1} 36%{opacity:0} 100%{opacity:0} }
    @keyframes qshow10 { 0%,28.2%{opacity:0} 28.5%{opacity:1} 35.5%{opacity:1} 36%{opacity:0} 100%{opacity:0} }

    .tr0 { animation: tr0a 45s linear infinite; }
    .tr1 { animation: tr1a 45s linear infinite; }
    .tr2 { animation: tr2a 45s linear infinite; }
    .tr3 { animation: tr3a 45s linear infinite; }
    .tr4 { animation: tr4a 45s linear infinite; }
    @keyframes tr0a { 0%,33.4%{opacity:0;transform:translateY(4px)} 34.2%{opacity:1;transform:translateY(0)} 46.6%{opacity:1} 47%{opacity:0} 100%{opacity:0} }
    @keyframes tr1a { 0%,34.3%{opacity:0;transform:translateY(4px)} 35.1%{opacity:1;transform:translateY(0)} 46.6%{opacity:1} 47%{opacity:0} 100%{opacity:0} }
    @keyframes tr2a { 0%,35.2%{opacity:0;transform:translateY(4px)} 36.0%{opacity:1;transform:translateY(0)} 46.6%{opacity:1} 47%{opacity:0} 100%{opacity:0} }
    @keyframes tr3a { 0%,36.1%{opacity:0;transform:translateY(4px)} 36.9%{opacity:1;transform:translateY(0)} 46.6%{opacity:1} 47%{opacity:0} 100%{opacity:0} }
    @keyframes tr4a { 0%,37%  {opacity:0;transform:translateY(4px)} 37.8%{opacity:1;transform:translateY(0)} 46.6%{opacity:1} 47%{opacity:0} 100%{opacity:0} }

    .pn0 { animation: pna0 45s linear infinite; }
    .pn1 { animation: pna1 45s linear infinite; }
    .pn2 { animation: pna2 45s linear infinite; }
    .pn3 { animation: pna3 45s linear infinite; }
    .pn4 { animation: pna4 45s linear infinite; }
    .pn5 { animation: pna5 45s linear infinite; }
    .pn6 { animation: pna6 45s linear infinite; }
    @keyframes pna0 { 0%,44.5%{opacity:0} 45.2%{opacity:1} 57.7%{opacity:1} 58.5%{opacity:0} 100%{opacity:0} }
    @keyframes pna1 { 0%,45.3%{opacity:0} 46%  {opacity:1} 57.7%{opacity:1} 58.5%{opacity:0} 100%{opacity:0} }
    @keyframes pna2 { 0%,46.1%{opacity:0} 46.8%{opacity:1} 57.7%{opacity:1} 58.5%{opacity:0} 100%{opacity:0} }
    @keyframes pna3 { 0%,46.9%{opacity:0} 47.6%{opacity:1} 57.7%{opacity:1} 58.5%{opacity:0} 100%{opacity:0} }
    @keyframes pna4 { 0%,47.7%{opacity:0} 48.4%{opacity:1} 57.7%{opacity:1} 58.5%{opacity:0} 100%{opacity:0} }
    @keyframes pna5 { 0%,48.5%{opacity:0} 49.2%{opacity:1} 57.7%{opacity:1} 58.5%{opacity:0} 100%{opacity:0} }
    @keyframes pna6 { 0%,49.3%{opacity:0} 50%  {opacity:1} 57.7%{opacity:1} 58.5%{opacity:0} 100%{opacity:0} }

    .cb0 { animation: cba0 45s linear infinite; }
    .cb1 { animation: cba1 45s linear infinite; }
    .cb2 { animation: cba2 45s linear infinite; }
    .cb3 { animation: cba3 45s linear infinite; }
    .cb4 { animation: cba4 45s linear infinite; }
    .cb5 { animation: cba5 45s linear infinite; }
    @keyframes cba0 { 0%,55.6%{opacity:0;transform:scale(.9)} 56.3%{opacity:1;transform:scale(1)} 68.8%{opacity:1} 69.5%{opacity:0} 100%{opacity:0} }
    @keyframes cba1 { 0%,56.4%{opacity:0;transform:scale(.9)} 57.1%{opacity:1;transform:scale(1)} 68.8%{opacity:1} 69.5%{opacity:0} 100%{opacity:0} }
    @keyframes cba2 { 0%,57.2%{opacity:0;transform:scale(.9)} 57.9%{opacity:1;transform:scale(1)} 68.8%{opacity:1} 69.5%{opacity:0} 100%{opacity:0} }
    @keyframes cba3 { 0%,58%  {opacity:0;transform:scale(.9)} 58.7%{opacity:1;transform:scale(1)} 68.8%{opacity:1} 69.5%{opacity:0} 100%{opacity:0} }
    @keyframes cba4 { 0%,58.8%{opacity:0;transform:scale(.9)} 59.5%{opacity:1;transform:scale(1)} 68.8%{opacity:1} 69.5%{opacity:0} 100%{opacity:0} }
    @keyframes cba5 { 0%,59.6%{opacity:0;transform:scale(.9)} 60.3%{opacity:1;transform:scale(1)} 68.8%{opacity:1} 69.5%{opacity:0} 100%{opacity:0} }

    .qb0 { animation: qba0 45s linear infinite; }
    .qb1 { animation: qba1 45s linear infinite; }
    .qb2 { animation: qba2 45s linear infinite; }
    .qb3 { animation: qba3 45s linear infinite; }
    .qb4 { animation: qba4 45s linear infinite; }
    .qbfill0 { animation: qbf0 45s linear infinite; }
    .qbfill1 { animation: qbf1 45s linear infinite; }
    .qbfill2 { animation: qbf2 45s linear infinite; }
    .qbfill3 { animation: qbf3 45s linear infinite; }
    .qbfill4 { animation: qbf4 45s linear infinite; }
    @keyframes qba0 { 0%,66.7%{opacity:0} 67.4%{opacity:1} 79.9%{opacity:1} 80.5%{opacity:0} 100%{opacity:0} }
    @keyframes qba1 { 0%,67.5%{opacity:0} 68.2%{opacity:1} 79.9%{opacity:1} 80.5%{opacity:0} 100%{opacity:0} }
    @keyframes qba2 { 0%,68.3%{opacity:0} 69%  {opacity:1} 79.9%{opacity:1} 80.5%{opacity:0} 100%{opacity:0} }
    @keyframes qba3 { 0%,69.1%{opacity:0} 69.8%{opacity:1} 79.9%{opacity:1} 80.5%{opacity:0} 100%{opacity:0} }
    @keyframes qba4 { 0%,69.9%{opacity:0} 70.6%{opacity:1} 79.9%{opacity:1} 80.5%{opacity:0} 100%{opacity:0} }
    @keyframes qbf0 { 0%,66.7%{stroke-dashoffset:500} 67.4%{stroke-dashoffset:0} 79.9%{stroke-dashoffset:0} 80.5%{stroke-dashoffset:500} 100%{stroke-dashoffset:500} }
    @keyframes qbf1 { 0%,67.5%{stroke-dashoffset:400} 68.2%{stroke-dashoffset:0} 79.9%{stroke-dashoffset:0} 80.5%{stroke-dashoffset:400} 100%{stroke-dashoffset:400} }
    @keyframes qbf2 { 0%,68.3%{stroke-dashoffset:350} 69%{stroke-dashoffset:0} 79.9%{stroke-dashoffset:0} 80.5%{stroke-dashoffset:350} 100%{stroke-dashoffset:350} }
    @keyframes qbf3 { 0%,69.1%{stroke-dashoffset:450} 69.8%{stroke-dashoffset:0} 79.9%{stroke-dashoffset:0} 80.5%{stroke-dashoffset:450} 100%{stroke-dashoffset:450} }
    @keyframes qbf4 { 0%,69.9%{stroke-dashoffset:380} 70.6%{stroke-dashoffset:0} 79.9%{stroke-dashoffset:0} 80.5%{stroke-dashoffset:380} 100%{stroke-dashoffset:380} }
  </style>
</defs>

<rect class="bg" width="860" height="440"/>

<g class="s0">
  <rect class="surface" x="40" y="30" width="800" height="380" rx="8"/>
  <rect class="border-col" x="40" y="30" width="800" height="380" rx="8"/>
  <text class="muted" x="60" y="55" font-size="12">Data Analysis</text>
  <polyline class="regline" points="80,320 150,280 220,240 290,200 360,160 420,140 490,110 560,90 630,80 700,70 760,60"/>
</g>

<g class="s1">
  <rect class="surface" x="40" y="30" width="800" height="380" rx="8"/>
  <rect class="border-col" x="40" y="30" width="800" height="380" rx="8"/>
  <text class="muted" x="60" y="55" font-size="12">Query Editor</text>
  <text class="blue" x="60" y="90" font-size="11" font-family="monospace">
    <tspan class="ql0">S</tspan><tspan class="ql1">E</tspan><tspan class="ql2">L</tspan><tspan class="ql3">E</tspan><tspan class="ql4">C</tspan><tspan class="ql5">T</tspan><tspan class="ql6"> </tspan><tspan class="ql7">*</tspan><tspan class="ql8"> </tspan><tspan class="ql9">F</tspan><tspan class="ql10">ROM</tspan>
  </text>
</g>

<g class="s2">
  <rect class="surface" x="40" y="30" width="800" height="380" rx="8"/>
  <rect class="border-col" x="40" y="30" width="800" height="380" rx="8"/>
  <text class="muted" x="60" y="55" font-size="12">Results Table</text>
  <line class="border-col" x1="60" y1="70" x2="820" y2="70"/>
  <g class="tr0"><text class="txt" x="80" y="95" font-size="11">ID: 1001</text><text class="txt" x="250" y="95" font-size="11">Value: 95.3</text></g>
  <g class="tr1"><text class="txt" x="80" y="120" font-size="11">ID: 1002</text><text class="txt" x="250" y="120" font-size="11">Value: 87.2</text></g>
  <g class="tr2"><text class="txt" x="80" y="145" font-size="11">ID: 1003</text><text class="txt" x="250" y="145" font-size="11">Value: 92.1</text></g>
  <g class="tr3"><text class="txt" x="80" y="170" font-size="11">ID: 1004</text><text class="txt" x="250" y="170" font-size="11">Value: 88.7</text></g>
  <g class="tr4"><text class="txt" x="80" y="195" font-size="11">ID: 1005</text><text class="txt" x="250" y="195" font-size="11">Value: 91.4</text></g>
</g>

<g class="s3">
  <rect class="surface" x="40" y="30" width="800" height="380" rx="8"/>
  <rect class="border-col" x="40" y="30" width="800" height="380" rx="8"/>
  <text class="muted" x="60" y="55" font-size="12">Data Pipeline</text>
  <g class="pn0"><circle cx="100" cy="150" r="20" class="green"/></g>
  <g class="pn1"><circle cx="180" cy="150" r="20" class="green"/></g>
  <g class="pn2"><circle cx="260" cy="150" r="20" class="blue"/></g>
  <g class="pn3"><circle cx="340" cy="150" r="20" class="blue"/></g>
  <g class="pn4"><circle cx="420" cy="150" r="20" class="purple"/></g>
  <g class="pn5"><circle cx="500" cy="150" r="20" class="purple"/></g>
  <g class="pn6"><circle cx="580" cy="150" r="20" class="orange"/></g>
  <line class="s-border" x1="120" y1="150" x2="160" y2="150"/>
  <line class="s-border" x1="200" y1="150" x2="240" y2="150"/>
  <line class="s-border" x1="280" y1="150" x2="320" y2="150"/>
  <line class="s-border" x1="360" y1="150" x2="400" y2="150"/>
  <line class="s-border" x1="440" y1="150" x2="480" y2="150"/>
  <line class="s-border" x1="520" y1="150" x2="560" y2="150"/>
</g>

<g class="s4">
  <rect class="surface" x="40" y="30" width="800" height="380" rx="8"/>
  <rect class="border-col" x="40" y="30" width="800" height="380" rx="8"/>
  <text class="muted" x="60" y="55" font-size="12">Infrastructure</text>
  <g class="cb0"><rect class="s-border" x="80" y="100" width="100" height="80" rx="4"/><text class="txt" x="95" y="145" font-size="10">Service A</text></g>
  <g class="cb1"><rect class="s-border" x="200" y="100" width="100" height="80" rx="4"/><text class="txt" x="215" y="145" font-size="10">Service B</text></g>
  <g class="cb2"><rect class="s-border" x="320" y="100" width="100" height="80" rx="4"/><text class="txt" x="335" y="145" font-size="10">Service C</text></g>
  <g class="cb3"><rect class="s-border" x="440" y="100" width="100" height="80" rx="4"/><text class="txt" x="455" y="145" font-size="10">Service D</text></g>
  <g class="cb4"><rect class="s-border" x="560" y="100" width="100" height="80" rx="4"/><text class="txt" x="575" y="145" font-size="10">Service E</text></g>
  <g class="cb5"><rect class="s-border" x="680" y="100" width="100" height="80" rx="4"/><text class="txt" x="695" y="145" font-size="10">Service F</text></g>
</g>

<g class="s5">
  <rect class="surface" x="40" y="30" width="800" height="380" rx="8"/>
  <rect class="border-col" x="40" y="30" width="800" height="380" rx="8"/>
  <text class="muted" x="60" y="55" font-size="12">Quality Metrics</text>
  <g class="qb0"><rect class="border-col" x="80" y="110" width="200" height="20" rx="3"/><line class="qbfill0 bar-anim" x1="80" y1="120" x2="280" y2="120" stroke-dasharray="500"/></g>
  <g class="qb1"><rect class="border-col" x="80" y="150" width="200" height="20" rx="3"/><line class="qbfill1 bar-anim" x1="80" y1="160" x2="280" y2="160" stroke-dasharray="400"/></g>
  <g class="qb2"><rect class="border-col" x="80" y="190" width="200" height="20" rx="3"/><line class="qbfill2 bar-anim" x1="80" y1="200" x2="280" y2="200" stroke-dasharray="350"/></g>
  <g class="qb3"><rect class="border-col" x="80" y="230" width="200" height="20" rx="3"/><line class="qbfill3 bar-anim" x1="80" y1="240" x2="280" y2="240" stroke-dasharray="450"/></g>
  <g class="qb4"><rect class="border-col" x="80" y="270" width="200" height="20" rx="3"/><line class="qbfill4 bar-anim" x1="80" y1="280" x2="280" y2="280" stroke-dasharray="380"/></g>
</g>

<g class="s6">
  <rect class="surface" x="40" y="30" width="800" height="380" rx="8"/>
  <rect class="border-col" x="40" y="30" width="800" height="380" rx="8"/>
  <text class="muted" x="60" y="55" font-size="12">Performance</text>
  <circle cx="150" cy="150" r="50" class="border-col" stroke-width="2"/>
  <circle cx="150" cy="150" r="40" class="border-col" stroke-width="1"/>
  <text class="green" x="130" y="155" font-size="14" font-weight="bold">98%</text>
  <text class="muted" x="100" y="230" font-size="11">Success Rate</text>
  <circle class="blink" cx="350" cy="150" r="8" class="green"/>
  <text class="txt" x="380" y="155" font-size="11">Active</text>
</g>

<g class="s7">
  <rect class="surface" x="40" y="30" width="800" height="380" rx="8"/>
  <rect class="border-col" x="40" y="30" width="800" height="380" rx="8"/>
  <text class="muted" x="60" y="55" font-size="12">Real-time Monitoring</text>
  <circle cx="150" cy="150" r="8" class="pulse green"/>
  <circle cx="150" cy="150" r="15" class="pulse" fill="none" stroke="#3fb950" stroke-width="2"/>
  <circle cx="150" cy="150" r="25" class="pulse" fill="none" stroke="#3fb950" stroke-width="1" opacity="0.5"/>
  <text class="blue" x="200" y="155" font-size="11">Streaming data...</text>
</g>

<g class="s8">
  <rect class="surface" x="40" y="30" width="800" height="380" rx="8"/>
  <rect class="border-col" x="40" y="30" width="800" height="380" rx="8"/>
  <text class="green" x="60" y="90" font-size="18" font-weight="bold">Data Analysis Complete</text>
  <text class="txt" x="60" y="130" font-size="12">✓ Data processed</text>
  <text class="txt" x="60" y="155" font-size="12">✓ Quality validated</text>
  <text class="txt" x="60" y="180" font-size="12">✓ Performance optimized</text>
  <text class="muted" x="60" y="230" font-size="11">Ready for insights and decision-making</text>
</g>

</svg>
