<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1180 610" width="100%" height="100%">
  <defs>
    <!-- Dark Mode Gradients & Filters -->
    <linearGradient id="bg-grad-dark" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#030712"/>
      <stop offset="50%" stop-color="#0b0f19"/>
      <stop offset="100%" stop-color="#030712"/>
    </linearGradient>
    <linearGradient id="accent-grad-dark" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#7C3AED"/>
      <stop offset="50%" stop-color="#22D3EE"/>
      <stop offset="100%" stop-color="#10B981"/>
    </linearGradient>
    <linearGradient id="ascii-grad-dark" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" stop-color="#22D3EE">
        <animate attributeName="stop-color" values="#22D3EE;#7C3AED;#10B981;#22D3EE" dur="8s" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" stop-color="#7C3AED">
        <animate attributeName="stop-color" values="#7C3AED;#10B981;#22D3EE;#7C3AED" dur="8s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>
    <radialGradient id="glow-1" cx="20%" cy="20%" r="50%">
      <stop offset="0%" stop-color="#7C3AED" stop-opacity="0.15"/>
      <stop offset="100%" stop-color="#030712" stop-opacity="0"/>
    </radialGradient>
    <radialGradient id="glow-2" cx="80%" cy="80%" r="50%">
      <stop offset="0%" stop-color="#22D3EE" stop-opacity="0.12"/>
      <stop offset="100%" stop-color="#030712" stop-opacity="0"/>
    </radialGradient>
    <filter id="glass-blur" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="20"/>
      <feColorMatrix type="matrix" values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 18 -7"/>
    </filter>
    
    <!-- Noise Pattern Simulation -->
    <pattern id="noise" width="100" height="100" patternUnits="userSpaceOnUse">
      <path d="M0 0h100v100H0z" fill="none"/>
      <circle cx="10" cy="10" r="0.5" fill="#ffffff" fill-opacity="0.05"/>
      <circle cx="50" cy="30" r="0.5" fill="#ffffff" fill-opacity="0.03"/>
      <circle cx="80" cy="70" r="0.5" fill="#ffffff" fill-opacity="0.06"/>
      <circle cx="30" cy="90" r="0.5" fill="#ffffff" fill-opacity="0.04"/>
    </pattern>
  </defs>

  <style>
    .base-text { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; }
    .mono-text { font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace; }
    
    /* Animations */
    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-8px); }
    }
    @keyframes pulse-glow {
      0%, 100% { opacity: 0.6; }
      50% { opacity: 1; }
    }
    @keyframes blink {
      0%, 100% { opacity: 1; }
      50% { opacity: 0; }
    }

    .floating { animation: float 6s ease-in-out infinite; }
    .pulsing { animation: pulse-glow 3s ease-in-out infinite; }
    .cursor { animation: blink 1s step-end infinite; }
    
    .panel {
      fill: #0F172A;
      stroke: rgba(255, 255, 255, 0.08);
      stroke-width: 1;
      rx: 16px;
    }
    
    .pill {
      fill: #1E293B;
      stroke: rgba(255, 255, 255, 0.06);
      transition: all 0.3s ease;
    }
    .pill:hover {
      fill: #334155;
      stroke: #22D3EE;
    }
  </style>

  <!-- Background Layer -->
  <rect width="1180" height="610" rx="20" fill="url(#bg-grad-dark)"/>
  <rect width="1180" height="610" rx="20" fill="url(#noise)"/>

  <!-- Ambient Background Glows -->
  <circle cx="200" cy="150" r="300" fill="url(#glow-1)" class="pulsing"/>
  <circle cx="950" cy="450" r="350" fill="url(#glow-2)" class="pulsing" style="animation-delay: 1.5s;"/>

  <!-- ======================================== -->
  <!-- LEFT SIDE: ASCII Portrait & Terminal UI  -->
  <!-- ======================================== -->
  <g transform="translate(30, 30)" class="floating">
    <!-- Left Panel Background -->
    <rect width="418" height="550" class="panel"/>
    
    <!-- Window Controls / Header -->
    <circle cx="25" cy="25" r="6" fill="#EF4444" opacity="0.8"/>
    <circle cx="45" cy="25" r="6" fill="#F59E0B" opacity="0.8"/>
    <circle cx="65" cy="25" r="6" fill="#10B981" opacity="0.8"/>
    <text x="90" y="29" class="mono-text" fill="#64748B" font-size="11" letter-spacing="1">root@sec-ops:~</text>
    <line x1="15" y1="45" x2="403" y2="45" stroke="rgba(255,255,255,0.06)" stroke-width="1"/>

    <!-- User Generated ASCII Portrait -->
    <g transform="translate(0, 60)">
      <!-- x="209" with text-anchor="middle" centers the ASCII lines perfectly in the 418px panel -->
      <text x="209" text-anchor="middle" class="mono-text" font-size="8" font-weight="700" fill="url(#ascii-grad-dark)" xml:space="preserve" letter-spacing="1">
        <tspan x="209" dy="9">./#%&amp;%%%%%%&amp;%(,.</tspan>
        <tspan x="209" dy="9">,#&amp;&amp;&amp;&amp;&amp;&amp;%%&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;%%%(.</tspan>
        <tspan x="209" dy="9">,%%&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;%%*.</tspan>
        <tspan x="209" dy="9">,%&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;@&amp;&amp;&amp;&amp;&amp;&amp;&amp;@&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;%</tspan>
        <tspan x="209" dy="9">.(%&amp;&amp;@&amp;@@@@@@&amp;@@@&amp;@@@@@@&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;%*</tspan>
        <tspan x="209" dy="9">.%&amp;&amp;&amp;@@&amp;&amp;@@@@@@@@@@@@@@@@@@@@@@@@@@@@&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;#</tspan>
        <tspan x="209" dy="9">.%&amp;&amp;&amp;@&amp;&amp;&amp;&amp;&amp;@&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;@&amp;@@@@@&amp;&amp;@@@&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;&amp;.</tspan>
        <tspan x="209" dy="9">%&amp;&amp;&amp;%#(((#%%#/*****/(###(//////((((((#%&amp;&amp;&amp;&amp;&amp;*</tspan>
        <tspan x="209" dy="9">#&amp;&amp;%#///////**************************/%&amp;&amp;&amp;&amp;</tspan>
        <tspan x="209" dy="9">&amp;&amp;%##(/////**************************/(%%&amp;%</tspan>
        <tspan x="209" dy="9">*%##((/////*****************,,********/(#%,</tspan>
        <tspan x="209" dy="9">((((/(###(#((/************(%%&amp;%%%%%#/*//(</tspan>
        <tspan x="209" dy="9">.((/#%##((((#%%%#(/**//###%%%&amp;%#(////**/*</tspan>
        <tspan x="209" dy="9">/(/////(#%#/%&amp;%*/#(#/***//((/*(%(*(((/***///*/</tspan>
        <tspan x="209" dy="9">.#((//////((((((//((/*******/////////********//</tspan>
        <tspan x="209" dy="9">((((//////*******/(/**********************(//,</tspan>
        <tspan x="209" dy="9">/(//////*******////**,***/*************/**/,</tspan>
        <tspan x="209" dy="9">/(///////*****//(%(//(%(/*************//**</tspan>
        <tspan x="209" dy="9">(((/(//////****//(///*//************////*,</tspan>
        <tspan x="209" dy="9">//(////////////**/**/////*****/*//*,</tspan>
        <tspan x="209" dy="9">,(((((////((((#####((((#(//***/////</tspan>
        <tspan x="209" dy="9">*(((((//////////((//***//////////</tspan>
        <tspan x="209" dy="9">*((((((////////////////////////</tspan>
        <tspan x="209" dy="9">(((((/////////////******//((//</tspan>
        <tspan x="209" dy="9">/(((###(//(///(////////((////*</tspan>
        <tspan x="209" dy="9">./(((((((#############(((///////.</tspan>
        <tspan x="209" dy="9">,#&amp;#(((//(((((((((((((/////////////&amp;(,</tspan>
        <tspan x="209" dy="9">,*/#((/((//////(((((//////////////////%(**,</tspan>
        <tspan x="209" dy="9">.***/*//((///(///////////(((/////****//*///(**********.</tspan>
        <tspan x="209" dy="9">.****************/(////////***//////////****/***//(******************.</tspan>
        <tspan x="209" dy="9">*************************//((////****//////*****/**/(/***********************</tspan>
        <tspan x="209" dy="9">***********************//*/////////////**//*******************,*,**,,,,******</tspan>
        <tspan x="209" dy="9">**************************///////////////*************,*******,,**,,*********</tspan>
        <tspan x="209" dy="9">************************,**////////////******************,**,***********,****</tspan>
      </text>
    </g>

    <!-- Terminal Status Box inside Left Panel -->
    <g transform="translate(20, 385)">
      <rect width="378" height="145" rx="8" fill="#030712" stroke="rgba(255,255,255,0.05)"/>
      <text x="15" y="22" class="mono-text" fill="#10B981" font-size="11">➜  ~ systemctl status net-sec.service</text>
      <text x="15" y="42" class="mono-text" fill="#94A3B8" font-size="10">● net-sec.service - Network &amp; Security Ops</text>
      <text x="25" y="58" class="mono-text" fill="#64748B" font-size="9.5">Loaded: loaded (/etc/systemd/system)</text>
      <text x="25" y="74" class="mono-text" fill="#64748B" font-size="9.5">Active: active (running) since Mar 2023</text>
      <text x="25" y="90" class="mono-text" fill="#22D3EE" font-size="9.5">Status: "Securing TÜBİTAK BİLGEM &amp; Kamu SM"</text>
      
      <line x1="15" y1="102" x2="363" y2="102" stroke="rgba(255,255,255,0.05)" stroke-width="1"/>
      
      <text x="15" y="122" class="mono-text" fill="#F8FAFC" font-size="10">⚡ Core Stack:</text>
      <text x="95" y="122" class="mono-text" fill="#94A3B8" font-size="9.5">Palo Alto • Fortinet • NetScaler • CyberArk</text>
    </g>
  </g>

  <!-- ======================================== -->
  <!-- RIGHT SIDE: Profile Details & Skills     -->
  <!-- ======================================== -->
  <g transform="translate(478, 30)">
    <!-- Right Panel Background -->
    <rect width="672" height="550" class="panel"/>

    <!-- Header Greeting & Rotating Title -->
    <g transform="translate(35, 45)">
      <text class="base-text" fill="#94A3B8" font-size="16" font-weight="500">Hi 👋 I'm</text>
      <text class="base-text" fill="#F8FAFC" font-size="32" font-weight="800" y="38">Emre Can Tüzer</text>
      
      <!-- Animated Role / Subtitle -->
      <g transform="translate(0, 68)">
        <rect width="340" height="28" rx="6" fill="#1E293B" stroke="rgba(34,211,238,0.2)"/>
        <text x="12" y="19" class="mono-text" fill="#22D3EE" font-size="12" font-weight="600">
          Senior Network &amp; Security Engineer[cite: 1]
          <animate attributeName="opacity" values="1;0.9;1" dur="2s" repeatCount="indefinite"/>
        </text>
        <rect x="325" y="8" width="6" height="12" fill="#22D3EE" class="cursor"/>
      </g>
    </g>

    <!-- Meta Info Grid (Location, Education, Focus, Email) -->
    <g transform="translate(35, 160)">
      <!-- Location -->
      <g transform="translate(0, 0)">
        <circle cx="12" cy="12" r="12" fill="#1E293B" stroke="rgba(255,255,255,0.05)"/>
        <path d="M12 6C9.79 6 8 7.79 8 10c0 2.25 4 8 4 8s4-5.75 4-8c0-2.21-1.79-4-4-4zm0 5.5c-.83 0-1.5-.67-1.5-1.5s.67-1.5 1.5-1.5 1.5.67 1.5 1.5-.67 1.5-1.5 1.5z" fill="#22D3EE" transform="scale(0.8) translate(3,3)"/>
        <text x="35" y="16" class="base-text" fill="#94A3B8" font-size="13">Location:</text>
        <text x="105" y="16" class="base-text" fill="#F8FAFC" font-size="13" font-weight="600">Gebze, Kocaeli, Türkiye</text>
      </g>

      <!-- Education -->
      <g transform="translate(310, 0)">
        <circle cx="12" cy="12" r="12" fill="#1E293B" stroke="rgba(255,255,255,0.05)"/>
        <path d="M12 3L1 9l11 6 9-4.91V17h2V9L12 3z" fill="#7C3AED" transform="scale(0.7) translate(5,5)"/>
        <text x="35" y="16" class="base-text" fill="#94A3B8" font-size="13">Education:</text>
        <text x="110" y="16" class="base-text" fill="#F8FAFC" font-size="13" font-weight="600">İTÜ MSc. / İYTE BSc.[cite: 1]</text>
      </g>

      <!-- Current Focus -->
      <g transform="translate(0, 38)">
        <circle cx="12" cy="12" r="12" fill="#1E293B" stroke="rgba(255,255,255,0.05)"/>
        <circle cx="12" cy="12" r="4" fill="#10B981"/>
        <text x="35" y="16" class="base-text" fill="#94A3B8" font-size="13">Current Focus:</text>
        <text x="135" y="16" class="base-text" fill="#F8FAFC" font-size="13" font-weight="600">Cybersecurity, Cryptography &amp; PAM[cite: 1]</text>
      </g>

      <!-- Email -->
      <g transform="translate(310, 38)">
        <circle cx="12" cy="12" r="12" fill="#1E293B" stroke="rgba(255,255,255,0.05)"/>
        <path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z" fill="#22D3EE" transform="scale(0.6) translate(6,6)"/>
        <text x="35" y="16" class="base-text" fill="#94A3B8" font-size="13">Email:</text>
        <text x="80" y="16" class="base-text" fill="#22D3EE" font-size="13" font-weight="600">emrecantuzer@gmail.com[cite: 1]</text>
      </g>
    </g>

    <!-- Divider -->
    <line x1="35" y1="260" x2="637" y2="260" stroke="rgba(255,255,255,0.06)" stroke-width="1"/>

    <!-- Skills Section: Glowing Pills -->
    <g transform="translate(35, 280)">
      <text class="base-text" fill="#F8FAFC" font-size="14" font-weight="700" letter-spacing="0.5">TECHNICAL EXPERTISE &amp; SKILLS</text>
      
      <!-- Row 1 Pills -->
      <g transform="translate(0, 20)">
        <g class="pill" transform="translate(0, 0)">
          <rect width="90" height="28" rx="14" class="pill" />
          <text x="45" y="18" text-anchor="middle" class="mono-text" fill="#E2E8F0" font-size="11">Palo Alto[cite: 1]</text>
        </g>
        <g class="pill" transform="translate(100, 0)">
          <rect width="80" height="28" rx="14" class="pill"/>
          <text x="40" y="18" text-anchor="middle" class="mono-text" fill="#E2E8F0" font-size="11">Fortinet[cite: 1]</text>
        </g>
        <g class="pill" transform="translate(190, 0)">
          <rect width="90" height="28" rx="14" class="pill"/>
          <text x="45" y="18" text-anchor="middle" class="mono-text" fill="#E2E8F0" font-size="11">NetScaler[cite: 1]</text>
        </g>
        <g class="pill" transform="translate(290, 0)">
          <rect width="90" height="28" rx="14" class="pill"/>
          <text x="45" y="18" text-anchor="middle" class="mono-text" fill="#E2E8F0" font-size="11">CyberArk[cite: 1]</text>
        </g>
        <g class="pill" transform="translate(390, 0)">
          <rect width="75" height="28" rx="14" class="pill"/>
          <text x="37" y="18" text-anchor="middle" class="mono-text" fill="#E2E8F0" font-size="11">Python[cite: 1]</text>
        </g>
        <g class="pill" transform="translate(475, 0)">
          <rect width="75" height="28" rx="14" class="pill"/>
          <text x="37" y="18" text-anchor="middle" class="mono-text" fill="#E2E8F0" font-size="11">Docker</text>
        </g>
      </g>

      <!-- Row 2 Pills -->
      <g transform="translate(0, 58)">
        <g class="pill" transform="translate(0, 0)">
          <rect width="95" height="28" rx="14" class="pill"/>
          <text x="47" y="18" text-anchor="middle" class="mono-text" fill="#E2E8F0" font-size="11">PostgreSQL</text>
        </g>
        <g class="pill" transform="translate(105, 0)">
          <rect width="95" height="28" rx="14" class="pill"/>
          <text x="47" y="18" text-anchor="middle" class="mono-text" fill="#E2E8F0" font-size="11">Linux / OEL[cite: 1]</text>
        </g>
        <g class="pill" transform="translate(210, 0)">
          <rect width="75" height="28" rx="14" class="pill"/>
          <text x="37" y="18" text-anchor="middle" class="mono-text" fill="#E2E8F0" font-size="11">Zabbix[cite: 1]</text>
        </g>
        <g class="pill" transform="translate(295, 0)">
          <rect width="115" height="28" rx="14" class="pill"/>
          <text x="57" y="18" text-anchor="middle" class="mono-text" fill="#E2E8F0" font-size="11">Cryptography[cite: 1]</text>
        </g>
        <g class="pill" transform="translate(420, 0)">
          <rect width="60" height="28" rx="14" class="pill"/>
          <text x="30" y="18" text-anchor="middle" class="mono-text" fill="#E2E8F0" font-size="11">Git</text>
        </g>
      </g>
    </g>

    <!-- Divider -->
    <line x1="35" y1="410" x2="637" y2="410" stroke="rgba(255,255,255,0.06)" stroke-width="1"/>

    <!-- Bottom Section: Current Organization & Social / Action Links -->
    <g transform="translate(35, 435)">
      <!-- Current Status Badge -->
      <rect width="280" height="65" rx="8" fill="#030712" stroke="rgba(255,255,255,0.05)"/>
      <circle cx="20" cy="22" r="4" fill="#10B981">
        <animate attributeName="opacity" values="1;0.3;1" dur="2s" repeatCount="indefinite"/>
      </circle>
      <text x="35" y="26" class="base-text" fill="#94A3B8" font-size="11">CURRENTLY EMPLOYED AT</text>
      <text x="15" y="48" class="base-text" fill="#F8FAFC" font-size="13" font-weight="600">TÜBİTAK BİLGEM Kamu SM[cite: 1]</text>

      <!-- Social / Quick Links -->
      <g transform="translate(315, 0)">
        <g transform="translate(0, 0)" class="pill" cursor="pointer">
          <rect width="70" height="65" rx="8" class="pill"/>
          <path d="M12 2A10 10 0 0 0 2 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.1-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0 0 12 2z" fill="#F8FAFC" transform="scale(1.2) translate(11,8)"/>
          <text x="35" y="55" text-anchor="middle" class="mono-text" fill="#94A3B8" font-size="10">GitHub</text>
        </g>

        <g transform="translate(85, 0)" class="pill" cursor="pointer">
          <rect width="70" height="65" rx="8" class="pill"/>
          <path d="M19 3a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h14m-.5 15.5v-5.3a3.26 3.26 0 0 0-3.26-3.26c-.85 0-1.84.52-2.28 1.3v-1.11h-2.79v8.37h2.79v-4.93c0-.77.62-1.4 1.39-1.4a1.4 1.4 0 0 1 1.4 1.4v4.93h2.75M6.88 8.56a1.68 1.68 0 0 0 1.68-1.68c0-.93-.75-1.69-1.68-1.69a1.69 1.69 0 0 0-1.69 1.69c0 .93.76 1.68 1.69 1.68m1.39 9.94v-8.37H5.5v8.37h2.77z" fill="#22D3EE" transform="scale(1.1) translate(9,10)"/>
          <text x="35" y="55" text-anchor="middle" class="mono-text" fill="#94A3B8" font-size="10">LinkedIn</text>
        </g>

        <g transform="translate(170, 0)" class="pill" cursor="pointer">
          <rect width="132" height="65" rx="8" class="pill"/>
          <path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z" fill="#10B981" transform="scale(1.1) translate(14,11)"/>
          <text x="66" y="55" text-anchor="middle" class="mono-text" fill="#F8FAFC" font-size="10">Contact Me</text>
        </g>
      </g>
    </g>
  </g>

  <!-- Dynamic Scanline Sweep Effect Overlay -->
  <rect x="0" y="0" width="1180" height="15" fill="url(#accent-grad-dark)" opacity="0.04" pointer-events="none">
    <animate attributeName="y" values="-20;610" dur="6s" repeatCount="indefinite"/>
  </rect>
</svg>
