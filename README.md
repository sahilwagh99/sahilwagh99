<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sahil Wagh | AI & Automation Engineer</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        :root {
            /* Industrial / Technical Theme - No Synthwave/Neon Purple */
            --bg-base: #09090b;       /* Zinc 950 */
            --bg-surface: #18181b;    /* Zinc 900 */
            --bg-surface-hover: #27272a; /* Zinc 800 */
            --border: #3f3f46;        /* Zinc 700 */
            --border-light: #52525b;  /* Zinc 600 */
            
            --text-main: #f4f4f5;     /* Zinc 50 */
            --text-muted: #a1a1aa;    /* Zinc 400 */
            
            --accent-primary: #f97316;   /* Orange 500 - Mechanical/Rust vibe */
            --accent-secondary: #eab308; /* Yellow 500 */
            --accent-tertiary: #14b8a6;  /* Teal 500 - Data vibe */
            
            --code-bg: #111113;
            --font-sans: 'Inter', -apple-system, sans-serif;
            --font-mono: 'JetBrains Mono', monospace;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background-color: var(--bg-base);
            color: var(--text-main);
            font-family: var(--font-sans);
            line-height: 1.6;
            overflow-x: hidden;
            background-image: 
                linear-gradient(rgba(255, 255, 255, 0.02) 1px, transparent 1px),
                linear-gradient(90deg, rgba(255, 255, 255, 0.02) 1px, transparent 1px);
            background-size: 32px 32px;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 2rem;
        }

        /* Typography */
        h1, h2, h3, h4 {
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 1rem;
            letter-spacing: -0.02em;
        }

        h1 { font-size: 3.5rem; text-transform: uppercase; }
        h2 { font-size: 2rem; color: var(--text-main); display: flex; align-items: center; gap: 0.75rem; border-bottom: 1px solid var(--border); padding-bottom: 0.5rem; margin-top: 3rem; }
        h3 { font-size: 1.25rem; color: var(--accent-primary); }

        p { color: var(--text-muted); margin-bottom: 1rem; }
        a { color: var(--accent-primary); text-decoration: none; transition: 0.2s; }
        a:hover { color: var(--text-main); }

        /* Utility */
        .text-center { text-align: center; }
        .mt-2 { margin-top: 2rem; }
        .mb-2 { margin-bottom: 2rem; }
        .flex { display: flex; }
        .flex-wrap { flex-wrap: wrap; }
        .gap-2 { gap: 1rem; }
        .items-center { align-items: center; }
        .justify-center { justify-content: center; }
        
        /* Hero Section */
        .hero {
            padding: 6rem 0 4rem;
            text-align: center;
            border-bottom: 1px solid var(--border);
            position: relative;
        }
        
        .hero::after {
            content: '';
            position: absolute;
            bottom: -1px;
            left: 20%;
            right: 20%;
            height: 1px;
            background: linear-gradient(90deg, transparent, var(--accent-primary), transparent);
        }

        .hero h1 {
            background: linear-gradient(to right, var(--text-main), var(--text-muted));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 0.5rem;
        }

        .hero .subtitle {
            font-family: var(--font-mono);
            color: var(--accent-primary);
            font-size: 1.1rem;
            letter-spacing: 0.05em;
            margin-bottom: 2rem;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
            margin-top: 2rem;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            padding: 0.5rem 1rem;
            background: var(--bg-surface);
            border: 1px solid var(--border);
            border-radius: 4px;
            color: var(--text-main);
            font-family: var(--font-mono);
            font-size: 0.875rem;
            text-transform: uppercase;
            transition: all 0.2s;
        }

        .btn:hover {
            background: var(--bg-surface-hover);
            border-color: var(--accent-primary);
            transform: translateY(-2px);
        }

        /* Terminal Window */
        .terminal {
            background: var(--code-bg);
            border: 1px solid var(--border);
            border-radius: 8px;
            overflow: hidden;
            margin: 2rem 0;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }

        .terminal-header {
            background: var(--bg-surface);
            padding: 0.75rem 1rem;
            border-bottom: 1px solid var(--border);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }
        .dot.r { background: #ef4444; }
        .dot.y { background: #eab308; }
        .dot.g { background: #22c55e; }

        .terminal-body {
            padding: 1.5rem;
            font-family: var(--font-mono);
            font-size: 0.95rem;
            line-height: 1.6;
            overflow-x: auto;
        }

        /* Syntax Highlighting */
        .sy-keyword { color: var(--accent-primary); font-weight: bold; }
        .sy-class { color: var(--accent-secondary); font-weight: bold; }
        .sy-string { color: var(--accent-tertiary); }
        .sy-operator { color: var(--text-muted); }
        .sy-variable { color: var(--text-main); }

        /* Grid Cards */
        .grid-2x2 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .card {
            background: var(--bg-surface);
            border: 1px solid var(--border);
            padding: 1.5rem;
            border-radius: 6px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .card::before {
            content: '';
            position: absolute;
            top: 0; left: 0; width: 4px; height: 100%;
            background: var(--border);
            transition: 0.3s ease;
        }

        .card:hover::before {
            background: var(--accent-primary);
        }

        .card:hover {
            border-color: var(--border-light);
            transform: translateY(-3px);
        }

        .card h3 {
            margin-bottom: 0.75rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .card-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1rem;
        }

        .tag {
            background: var(--bg-base);
            border: 1px solid var(--border);
            padding: 0.25rem 0.5rem;
            border-radius: 4px;
            font-family: var(--font-mono);
            font-size: 0.75rem;
            color: var(--text-muted);
        }

        /* Pipeline Visuals (Replacing ASCII) */
        .pipeline-container {
            background: var(--bg-surface);
            border: 1px dashed var(--border-light);
            padding: 2rem;
            border-radius: 6px;
            margin: 1.5rem 0;
            overflow-x: auto;
        }

        .pipeline {
            display: flex;
            align-items: center;
            justify-content: flex-start;
            gap: 0.5rem;
            min-width: max-content;
        }

        .node {
            background: var(--bg-base);
            border: 1px solid var(--border);
            padding: 0.75rem 1.25rem;
            border-radius: 4px;
            font-family: var(--font-mono);
            font-size: 0.85rem;
            color: var(--text-main);
            position: relative;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            box-shadow: 0 4px 6px rgba(0,0,0,0.2);
        }

        .node.highlight {
            border-color: var(--accent-primary);
            color: var(--accent-primary);
        }

        .arrow {
            color: var(--border-light);
            font-size: 1.2rem;
            font-weight: bold;
        }

        /* Tech Stack Icons container */
        .tech-icons {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin: 1rem 0;
            background: var(--bg-surface);
            padding: 1.5rem;
            border: 1px solid var(--border);
            border-radius: 6px;
        }

        /* GitHub Stats */
        .stats-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 1rem;
            margin-top: 1.5rem;
        }
        @media (min-width: 768px) {
            .stats-grid { grid-template-columns: 1fr 1fr; }
        }
        .stats-grid img, .full-img img {
            width: 100%;
            border-radius: 6px;
            border: 1px solid var(--border);
        }

        .quote-block {
            text-align: center;
            padding: 4rem 0;
            font-family: var(--font-mono);
        }
        
        .quote-block blockquote {
            font-size: 1.5rem;
            color: var(--text-main);
            margin-bottom: 1.5rem;
            font-style: italic;
        }
        
        .quote-block span {
            color: var(--accent-primary);
            font-size: 0.9rem;
            letter-spacing: 0.1em;
        }

    </style>
</head>
<body>

    <div class="container">
        
        <!-- HEADER / HERO -->
        <header class="hero">
            <h1>Sahil Wagh</h1>
            <div class="subtitle">>_ AI & AUTOMATION ENGINEER</div>
            <p>Building AI-powered automation systems &bull; Engineering RAG & Agentic AI pipelines &bull; Turning unstructured data into intelligence</p>
            
            <div class="social-links">
                <a href="mailto:sahilwagh.dev@gmail.com" class="btn">
                    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg>
                    Email
                </a>
                <a href="https://kaggle.com/sahilwagh" target="_blank" class="btn">
                    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"></path><polyline points="3.27 6.96 12 12.01 20.73 6.96"></polyline><line x1="12" y1="22.08" x2="12" y2="12"></line></svg>
                    Kaggle
                </a>
                <a href="https://www.leetcode.com/sai_wagh" target="_blank" class="btn">
                    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="16 18 22 12 16 6"></polyline><polyline points="8 6 2 12 8 18"></polyline></svg>
                    LeetCode
                </a>
                <a href="https://github.com/sahilwagh99" target="_blank" class="btn">
                    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path></svg>
                    GitHub
                </a>
            </div>
        </header>

        <!-- WHOAMI -->
        <h2 id="whoami">⚡ whoami</h2>
        <div class="terminal">
            <div class="terminal-header">
                <div class="dot r"></div>
                <div class="dot y"></div>
                <div class="dot g"></div>
            </div>
            <div class="terminal-body">
<pre><code><span class="sy-keyword">class</span> <span class="sy-class">SahilWagh</span>:
    
    <span class="sy-variable">role</span> <span class="sy-operator">=</span> <span class="sy-string">"AI & Automation Engineer"</span>

    <span class="sy-variable">focus</span> <span class="sy-operator">=</span> [
        <span class="sy-string">"Generative AI"</span>,
        <span class="sy-string">"RAG Systems"</span>,
        <span class="sy-string">"Agentic AI"</span>,
        <span class="sy-string">"Intelligent Automation"</span>,
        <span class="sy-string">"Computer Vision"</span>,
        <span class="sy-string">"Cloud & DevOps"</span>
    ]

    <span class="sy-variable">philosophy</span> <span class="sy-operator">=</span> <span class="sy-string">"Automate what should not be manual."</span></code></pre>
            </div>
        </div>

        <!-- TECH STACK -->
        <h2>🛠️ Engineering Stack</h2>
        
        <div class="grid-2x2">
            <!-- AI & GENAI -->
            <div class="card">
                <h3>🧠 AI & GenAI</h3>
                <p>Building production-ready language and retrieval models.</p>
                <div class="card-tags">
                    <span class="tag">LangChain</span>
                    <span class="tag">LangGraph</span>
                    <span class="tag">LlamaIndex</span>
                    <span class="tag">HuggingFace</span>
                    <span class="tag">RAG</span>
                    <span class="tag">FAISS</span>
                    <span class="tag">ChromaDB</span>
                    <span class="tag">Pinecone</span>
                    <span class="tag">PyTorch</span>
                </div>
            </div>

            <!-- BACKEND & DATA -->
            <div class="card">
                <h3>🐍 Backend & Data</h3>
                <p>Architecting scalable data pipelines and APIs.</p>
                <div class="card-tags">
                    <span class="tag">Python</span>
                    <span class="tag">FastAPI</span>
                    <span class="tag">PostgreSQL</span>
                    <span class="tag">MongoDB</span>
                    <span class="tag">MySQL</span>
                </div>
            </div>

            <!-- COMPUTER VISION -->
            <div class="card">
                <h3>👁️ Vision & Document AI</h3>
                <p>Extracting structured intelligence from unstructured data.</p>
                <div class="card-tags">
                    <span class="tag">YOLO</span>
                    <span class="tag">OpenCV</span>
                    <span class="tag">EasyOCR</span>
                    <span class="tag">PyMuPDF</span>
                    <span class="tag">Docling</span>
                    <span class="tag">AWS Textract</span>
                </div>
            </div>

            <!-- CLOUD & DEVOPS -->
            <div class="card">
                <h3>☁️ Cloud & Automation</h3>
                <p>Deploying resilient systems and RPA workflows.</p>
                <div class="card-tags">
                    <span class="tag">AWS</span>
                    <span class="tag">Docker</span>
                    <span class="tag">Jenkins</span>
                    <span class="tag">CI/CD</span>
                    <span class="tag">UiPath</span>
                    <span class="tag">Power Automate</span>
                </div>
            </div>
        </div>

        <!-- FEATURED ENGINEERING PIPELINES -->
        <h2>🚀 Featured Engineering</h2>
        
        <h3>RAG & Agentic AI Architecture</h3>
        <div class="pipeline-container">
            <div class="pipeline">
                <div class="node">Documents / APIs</div>
                <div class="arrow">→</div>
                <div class="node">Chunking</div>
                <div class="arrow">→</div>
                <div class="node">Embeddings</div>
                <div class="arrow">→</div>
                <div class="node">Vector Store</div>
                <div class="arrow">→</div>
                <div class="node">Retriever</div>
                <div class="arrow">→</div>
                <div class="node highlight">LangGraph Agent</div>
                <div class="arrow">→</div>
                <div class="node highlight">LLM</div>
            </div>
        </div>

        <h3>Intelligent Document Processing</h3>
        <div class="pipeline-container">
            <div class="pipeline">
                <div class="node">PDF / Image</div>
                <div class="arrow">→</div>
                <div class="node">AWS Textract / OCR</div>
                <div class="arrow">→</div>
                <div class="node highlight">LLM Extraction</div>
                <div class="arrow">→</div>
                <div class="node">Validation Engine</div>
                <div class="arrow">→</div>
                <div class="node highlight">Structured Data</div>
            </div>
        </div>

        <h3>Computer Vision Pipeline</h3>
        <div class="pipeline-container">
            <div class="pipeline">
                <div class="node">Video Stream</div>
                <div class="arrow">→</div>
                <div class="node">YOLO Detection</div>
                <div class="arrow">→</div>
                <div class="node">Vehicle Class.</div>
                <div class="arrow">→</div>
                <div class="node">Plate Detection</div>
                <div class="arrow">→</div>
                <div class="node highlight">OCR</div>
                <div class="arrow">→</div>
                <div class="node highlight">Insights DB</div>
            </div>
        </div>

        <!-- ENGINEERING MINDSET -->
        <h2>🧩 Engineering Mindset</h2>
        <div class="pipeline-container" style="border-color: var(--border);">
            <div class="pipeline justify-center">
                <div class="node" style="border-color: var(--border-light);">01 UNDERSTAND</div>
                <div class="arrow">→</div>
                <div class="node" style="border-color: var(--border-light);">02 AUTOMATE</div>
                <div class="arrow">→</div>
                <div class="node highlight">03 INTELLIGENT</div>
                <div class="arrow">→</div>
                <div class="node highlight">04 SCALE</div>
            </div>
            <p class="text-center mt-2" style="font-family: var(--font-mono); font-size: 0.9rem;">Find the bottleneck → Build the system → Automate the workflow → Scale the solution</p>
        </div>

        <!-- GITHUB ANALYTICS -->
        <h2>📊 GitHub Analytics</h2>
        <div class="stats-grid">
            <!-- Using github_dark theme to match our industrial aesthetic instead of tokyonight -->
            <img src="https://github-readme-stats.vercel.app/api?username=sahilwagh99&show_icons=true&theme=github_dark&hide_border=true&rank_icon=github&bg_color=18181b&title_color=f4f4f5&text_color=a1a1aa&icon_color=f97316" alt="GitHub Stats">
            <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=sahilwagh99&layout=compact&theme=github_dark&hide_border=true&bg_color=18181b&title_color=f4f4f5&text_color=a1a1aa" alt="Top Languages">
        </div>
        
        <div class="full-img mt-2">
            <img src="https://github-readme-activity-graph.vercel.app/graph?username=sahilwagh99&theme=github-dark&hide_border=true&area=true&bg_color=18181b&color=f97316&line=f97316&point=f4f4f5" alt="Activity Graph">
        </div>

        <!-- FOOTER QUOTE -->
        <div class="quote-block">
            <blockquote>"Engineering intelligent systems out of digital chaos."</blockquote>
            <span>BUILD → AUTOMATE → INTELLIGENT → SCALE</span>
            
            <div class="social-links mt-2">
                <a href="https://drive.google.com/file/d/1lpU4DsrjAuA8hxiXneTlSdRclogX9dpT/view?usp=sharing" target="_blank" class="btn" style="border-color: var(--accent-primary); color: var(--accent-primary);">
                    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path><polyline points="14 2 14 8 20 8"></polyline><line x1="16" y1="13" x2="8" y2="13"></line><line x1="16" y1="17" x2="8" y2="17"></line><polyline points="10 9 9 9 8 9"></polyline></svg>
                    View Resume
                </a>
            </div>
        </div>

    </div>

</body>
</html>
