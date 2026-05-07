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

    /* Each stage lasts 5s, total 45s */
    /* Stage visibility: each block visible for 5s window */

    .stage { opacity: 0; }

    /* s0: 0-5s */
    .s0 { animation: stg0 45s linear infinite; }
    @keyframes stg0 {
      0%      { opacity: 1; }
      11.1%   { opacity: 1; }
      13.3%   { opacity: 0; }
      100%    { opacity: 0; }
    }

    /* s1: 5-10s */
    .s1 { animation: stg1 45s linear infinite; }
    @keyframes stg1 {
      0%      { opacity: 0; }
      10%     { opacity: 0; }
      11.1%   { opacity: 1; }
      22.2%   { opacity: 1; }
      24.4%   { opacity: 0; }
      100%    { opacity: 0; }
    }

    /* s2: 10-15s */
    .s2 { animation: stg2 45s linear infinite; }
    @keyframes stg2 {
      0%,22.2%  { opacity: 0; }
      22.3%     { opacity: 1; }
      33.3%     { opacity: 1; }
      35.5%     { opacity: 0; }
      100%      { opacity: 0; }
    }

    /* s3: 15-20s */
    .s3 { animation: stg3 45s linear infinite; }
    @keyframes stg3 {
      0%,33.3%  { opacity: 0; }
      33.4%     { opacity: 1; }
      44.4%     { opacity: 1; }
      46.6%     { opacity: 0; }
      100%      { opacity: 0; }
    }

    /* s4: 20-25s */
    .s4 { animation: stg4 45s linear infinite; }
    @keyframes stg4 {
      0%,44.4%  { opacity: 0; }
      44.5%     { opacity: 1; }
      55.5%     { opacity: 1; }
      57.7%     { opacity: 0; }
      100%      { opacity: 0; }
    }

    /* s5: 25-30s */
    .s5 { animation: stg5 45s linear infinite; }
    @keyframes stg5 {
      0%,55.5%  { opacity: 0; }
      55.6%     { opacity: 1; }
      66.6%     { opacity: 1; }
      68.8%     { opacity: 0; }
      100%      { opacity: 0; }
    }

    /* s6: 30-35s */
    .s6 { animation: stg6 45s linear infinite; }
    @keyframes stg6 {
      0%,66.6%  { opacity: 0; }
      66.7%     { opacity: 1; }
      77.7%     { opacity: 1; }
      79.9%     { opacity: 0; }
      100%      { opacity: 0; }
    }

    /* s7: 35-40s */
    .s7 { animation: stg7 45s linear infinite; }
    @keyframes stg7 {
      0%,77.7%  { opacity: 0; }
      77.8%     { opacity: 1; }
      88.8%     { opacity: 1; }
      91%       { opacity: 0; }
      100%      { opacity: 0; }
    }

    /* s8: 40-45s */
    .s8 { animation: stg8 45s linear infinite; }
    @keyframes stg8 {
      0%,88.8%  { opacity: 0; }
      88.9%     { opacity: 1; }
      100%      { opacity: 1; }
    }

    /* bar fills - animate width via stroke-dashoffset trick */
    .bar-anim { stroke-linecap: round; }

    /* dot blink */
    .blink { animation: blink 1s step-end infinite; }
    @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

    /* pulse dot */
    .pulse { animation: pulse 2s ease-in-out infinite; }
    @keyframes pulse { 0%,100%{opacity:1} 50%{opacity:.3} }

    /* scatter points appear */
    .pt { animation: ptfade 3s ease-out forwards; }
    @keyframes ptfade { from{opacity:0} to{opacity:0.7} }

    /* regression line draw */
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

    /* text typing for query */
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

    /* table rows */
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

    /* pipeline nodes */
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

    /* container boxes */
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

    /* quality bars */
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
  </style>
</defs>

<rect class="bg" width="860" height="440"/>
</svg>
