### Hi there 👋

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Turag Server CLI</title>
    <style>
        body {
            background-color: #0d1117;
            color: #d4d4d4;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
            margin: 0;
            padding: 40px 20px;
            max-width: 900px;
            margin-left: auto;
            margin-right: auto;
            line-height: 1.6;
        }

        .description {
            font-size: 16px;
            margin-bottom: 25px;
            color: #d1d5db;
        }

        .terminal {
            background-color: #262626; 
            border-radius: 8px;
            padding: 25px;
            font-family: 'Consolas', 'Fira Code', 'Monaco', monospace;
            font-size: 14.5px;
            line-height: 1.5;
            color: #d4d4d4;
            box-shadow: 0 20px 50px rgba(0,0,0,0.8);
            border: 1px solid #333;
            min-height: 500px; /* Pre-fill height so it doesn't jump */
        }

        .prompt-bracket { color: #888; }
        .prompt-arrow { color: #a6e22e; } 
        .prompt-dir { color: #66d9ef; font-weight: bold;} 
        .prompt-git { color: #ae81ff; } 
        .prompt-cross { color: #f92672; font-weight: bold; } 
        .sys-success { color: #a6e22e; font-weight: bold; }
        .sys-info { color: #e6db74; } 
        .sys-muted { color: #888888; }
        .cmd-text { color: #f8f8f2; }

        .ascii-art {
            color: #5f8787; 
            font-weight: bold;
            line-height: 1.15;
            margin: 20px 0;
            white-space: pre;
        }

        a {
            color: #66d9ef;
            text-decoration: none;
        }
        a:hover {
            text-decoration: underline;
        }

        .animate-pulse {
            animation: blink 1s step-start infinite;
            display: inline-block;
            vertical-align: bottom;
            width: 8px;
            height: 16px;
            background-color: #d4d4d4;
            margin-left: 2px;
        }

        @keyframes blink {
            50% { opacity: 0; }
        }
    </style>
</head>
<body>
    <div class="description">
        Md. Abdullah Turag Sarkar is a Junior AI Automation Specialist focused on deploying intelligent AI solutions, automating workflows, and scaling business operations.
    </div>
    
    <div class="terminal" id="terminal-content">
        <!-- JS will dynamically type terminal content here -->
    </div>

    <!-- Social Links visually better outside terminal -->
    <div style="margin-top: 30px; display: flex; gap: 10px; flex-wrap: wrap; justify-content: center;">
        <a href="https://your-portfolio-site.com" target="_blank"><img src="https://img.shields.io/badge/🌐_Visit_My_Web_Profile-000000?style=flat-square&logo=googlechrome&logoColor=white" height="26"/></a>
        <a href="mailto:turagsarkar@gmail.com"><img src="https://img.shields.io/badge/Email-ea4335?style=flat-square&logo=gmail&logoColor=white" height="26"/></a>
        <a href="https://linkedin.com/in/turagsarkar" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" height="26"/></a>
        <a href="https://github.com/turagsarkar" target="_blank"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" height="26"/></a>
    </div>

    <script>
        const commands = [
            `<div><span class="prompt-bracket">[</span><span class="prompt-arrow">➜</span> <span class="prompt-dir">portfolio</span> <span class="prompt-git">git:(master)</span> <span class="prompt-cross">✗</span> <span class="sys-muted">cargo run --bin turag-cli -- --addr 127.0.0.1:8080</span></div>`,
            `<div><span class="sys-success">&nbsp;&nbsp;&nbsp;&nbsp;Finished</span> <span class="sys-info">\`dev\` profile [unoptimized + debuginfo] target(s) in 0.09s</span></div>`,
            `<div><span class="sys-success">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Running</span> <span class="sys-info">\`target/debug/turag-cli --addr '127.0.0.1:8080'\`</span></div>`,
            `<div style="margin-bottom: 20px;"><span class="cmd-text">➔ connected target: 127.0.0.1:8080</span></div>`,
            `<div class="ascii-art">
████████╗██╗   ██╗██████╗  █████╗  ██████╗
╚══██╔══╝██║   ██║██╔══██╗██╔══██╗██╔════╝
   ██║   ██║   ██║██████╔╝███████║██║  ███╗
   ██║   ██║   ██║██╔══██╗██╔══██║██║   ██║
   ██║   ╚██████╔╝██║  ██║██║  ██║╚██████╔╝
   ╚═╝    ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝ ╚═════╝ 
            </div>`,
            `<div style="margin-bottom: 15px;"><span class="sys-muted">type commands (ABOUT/SKILLS/EXPERIENCE/RESEARCH/PROJECTS/CONTACT). 'exit' or Ctrl+C to quit.</span></div>`,
            `[🤖 > ABOUT`,
            `OK\n<span class="cmd-text">Name: Md. Abdullah Turag Sarkar\nRole: Junior AI Automation Specialist @ SM Technology, Betopia Group\nLocation: Dhaka, Bangladesh</span>\n`,
            `[🤖 > SKILLS`,
            `OK\n<span class="cmd-text">Languages :\n<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" height="20" style="vertical-align:middle;"> <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" height="20" style="vertical-align:middle;"> <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white" height="20" style="vertical-align:middle;"> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" height="20" style="vertical-align:middle;"> <img src="https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white" height="20" style="vertical-align:middle;">\n\nFrameworks:\n<img src="https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white" height="20" style="vertical-align:middle;"> <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white" height="20" style="vertical-align:middle;"> <img src="https://img.shields.io/badge/Keras-D00000?style=flat-square&logo=keras&logoColor=white" height="20" style="vertical-align:middle;"> <img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" height="20" style="vertical-align:middle;"> <img src="https://img.shields.io/badge/n8n-FF6D5A?style=flat-square&logo=n8n&logoColor=white" height="20" style="vertical-align:middle;"> <img src="https://img.shields.io/badge/REST_API-005571?style=flat-square" height="20" style="vertical-align:middle;">\n\nDatabases :\n<img src="https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white" height="20" style="vertical-align:middle;"></span>\n`,
            `[🤖 > EXPERIENCE`,
            `OK\n<span class="cmd-text">2026 - Pres : Junior AI Automation Specialist @ SM Technology, Betopia Group\n2022 & 2024 : IT Supervisor (Contractual) @ Bangladesh Bureau of Statistics</span>\n`,
            `[🤖 > RESEARCH_INTERESTS`,
            `OK\n<span class="cmd-text">> Intelligent Automation & Generative AI Agents\n> Decentralized Smart Grid Control Systems\n> Medical Image Processing and Disease Detection</span>\n`,
            `[🤖 > PROJECTS`,
            `OK\n<span class="cmd-text">- Electrical-Grid-Stability-Simulated (Python, Scikit-learn)\n- Identification-of-Erythemato-Squamous-Disease (Python, Flask, Streamlit)\n- Image-Based-Plant-leaf-Disease-Detection (TensorFlow, Keras)</span>\n`,
            `[🤖 > CONTACT`,
            `OK\n<span class="cmd-text">Portfolio : <a href="#" target="_blank">https://your-portfolio-site.com</a>  <span class="sys-muted"><-- Visit my Web Profile!</span>\nEmail     : <a href="mailto:turagsarkar@gmail.com">turagsarkar@gmail.com</a>\nPhone     : +880-1957059432\nLinkedIn  : <a href="https://linkedin.com/in/turagsarkar" target="_blank">linkedin.com/in/turagsarkar</a>\nGitHub    : <a href="https://github.com/turagsarkar" target="_blank">github.com/turagsarkar</a></span>\n`,
            `[🤖 > `
        ];

        const terminal = document.getElementById('terminal-content');
        let cmdIndex = 0;

        function renderLines() {
            if (cmdIndex >= commands.length) {
                return; 
            }

            let lineStr = commands[cmdIndex];
            
            if (lineStr.startsWith('[🤖 >')) {
                // Simulate typing user input inside prompt
                let spanWrapper = document.createElement('div');
                spanWrapper.innerHTML = `<span class="prompt-bracket">[🤖 > </span><span class="cmd-text typing"></span><span class="animate-pulse typing-cursor"></span>`;
                terminal.appendChild(spanWrapper);
                let typingTarget = spanWrapper.querySelector('.typing');
                let cursorTarget = spanWrapper.querySelector('.typing-cursor');
                let textToType = lineStr.replace('[🤖 > ', '');
                
                // Keep the cursor blinking at the very end
                if(textToType.trim() === ""){
                    return;
                }

                let charIndex = 0;
                let typeInterval = setInterval(() => {
                    if (charIndex < textToType.length) {
                        typingTarget.textContent += textToType.charAt(charIndex);
                        charIndex++;
                    } else {
                        clearInterval(typeInterval);
                        cmdIndex++;
                        cursorTarget.remove(); // Drop cursor jumping to next line
                        setTimeout(renderLines, 400); // 400ms pause before output executes
                    }
                }, 60); // 60ms typing speed
                
            } else {
                // Output instant dump from terminal server
                let outputDiv = document.createElement('div');
                outputDiv.style.marginBottom = "15px";
                
                if (lineStr.startsWith('OK\n')) {
                    outputDiv.innerHTML = '<span class="sys-muted">OK</span><br>' + lineStr.replace('OK\n', '').replace(/\n/g, '<br>');
                } else {
                    outputDiv.innerHTML = lineStr;
                }

                terminal.appendChild(outputDiv);
                
                cmdIndex++;
                let delay = lineStr.includes("ascii-art") ? 800 : 100;
                setTimeout(renderLines, delay);
            }
        }

        // Delay 800ms to mimic page load before animation bootup
        setTimeout(renderLines, 800);
    </script>
</body>
</html>
