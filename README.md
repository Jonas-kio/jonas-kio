<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Código README + Vista Previa</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: #24292e;
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px;
            background: #f6f8fa;
        }
        
        .container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            height: 100vh;
        }
        
        .code-section {
            background: #1a1a1a;
            border-radius: 8px;
            overflow: hidden;
        }
        
        .code-header {
            background: #2d2d2d;
            color: white;
            padding: 15px 20px;
            font-weight: bold;
            border-bottom: 1px solid #444;
        }
        
        .code-content {
            height: calc(100vh - 100px);
            overflow-y: auto;
            padding: 0;
        }
        
        .code-content pre {
            margin: 0;
            padding: 20px;
            color: #f8f8f2;
            font-family: 'Consolas', 'Monaco', monospace;
            font-size: 12px;
            line-height: 1.4;
            white-space: pre-wrap;
            background: #1a1a1a;
        }
        
        .preview-section {
            background: white;
            border: 1px solid #e1e4e8;
            border-radius: 8px;
            overflow: hidden;
        }
        
        .preview-header {
            background: #f6f8fa;
            color: #24292e;
            padding: 15px 20px;
            font-weight: bold;
            border-bottom: 1px solid #e1e4e8;
        }
        
        .preview-content {
            height: calc(100vh - 100px);
            overflow-y: auto;
            padding: 20px;
        }
        
        /* Estilos para simular GitHub */
        .typing-text {
            background: linear-gradient(45deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: bold;
            font-size: 1.1em;
            text-align: center;
            padding: 15px;
            border: 2px solid #667eea;
            border-radius: 8px;
            margin: 15px 0;
        }
        
        .badge {
            display: inline-block;
            padding: 6px 12px;
            margin: 3px;
            border-radius: 4px;
            font-size: 11px;
            font-weight: bold;
            text-decoration: none;
            color: white;
        }
        
        .html-badge { background: #e34f26; }
        .css-badge { background: #1572b6; }
        .react-badge { background: #61dafb; color: #333; }
        .python-badge { background: #3776ab; }
        .java-badge { background: #ed8b00; color: #333; }
        .php-badge { background: #777bb4; }
        .laravel-badge { background: #ff2d20; }
        .figma-badge { background: #f24e1e; }
        .trello-badge { background: #0052cc; }
        .linkedin-badge { background: #0077b5; }
        .github-badge { background: #333; }
        .email-badge { background: #d14836; }
        .portfolio-badge { background: #ff5722; }
        
        .stats-placeholder {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 20px;
            border-radius: 8px;
            text-align: center;
            margin: 15px 0;
            font-size: 14px;
        }
        
        .code-block {
            background: #f6f8fa;
            border: 1px solid #e1e4e8;
            border-radius: 6px;
            padding: 16px;
            margin: 15px 0;
            font-family: 'Consolas', 'Monaco', monospace;
            font-size: 13px;
            overflow-x: auto;
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin: 15px 0;
        }
        
        .skill-item {
            background: #f8f9fa;
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid #0366d6;
        }
        
        .social-links {
            display: flex;
            gap: 10px;
            justify-content: center;
            margin: 20px 0;
            flex-wrap: wrap;
        }
        
        .wave {
            animation: wave 2s infinite;
            display: inline-block;
        }
        
        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(20deg); }
            75% { transform: rotate(-20deg); }
        }
        
        h1 { color: #2d3436; margin-bottom: 10px; }
        h2 { color: #0366d6; border-bottom: 2px solid #e1e4e8; padding-bottom: 5px; margin-top: 30px; }
        h3 { color: #586069; margin-top: 20px; }
        
        .copy-button {
            position: absolute;
            top: 15px;
            right: 15px;
            background: #0366d6;
            color: white;
            border: none;
            padding: 8px 12px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 12px;
        }
        
        .copy-button:hover {
            background: #0256cc;
        }
        
        .highlight {
            background: #fff3cd;
            padding: 2px 4px;
            border-radius: 3px;
            font-weight: bold;
        }
        
        blockquote {
            border-left: 4px solid #dfe2e5;
            padding: 0 16px;
            color: #6a737d;
            margin: 20px 0;
        }
        
        .center { text-align: center; }
        
        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
                height: auto;
            }
            
            .code-content, .preview-content {
                height: 400px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Sección del Código -->
        <div class="code-section">
            <div class="code-header">
                📝 Código Completo del README.md
                <button class="copy-button" onclick="copyCode()">Copiar Todo</button>
            </div>
            <div class="code-content">
                <pre id="readme-code"># 👨‍💻 Jonas Vidal Zenzano

&lt;div align="center"&gt;
  &lt;img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=1000&width=435&lines=Estudiante+de+Ingenier%C3%ADa+Inform%C3%A1tica;Desarrollador+Full-Stack;Construyendo+el+futuro+con+c%C3%B3digo;Siempre+aprendiendo+algo+nuevo" alt="Typing SVG" /&gt;
&lt;/div&gt;

---

## 🚀 Sobre mí

¡Hola! Soy un estudiante de Ingeniería Informática apasionado por transformar ideas en soluciones digitales. Me especializo en desarrollo full-stack y disfruto creando experiencias web que realmente importen.

- 🎓 **Estudiando:** Ingeniería Informática
- 💻 **Enfoque:** Desarrollo Full-Stack & Diseño UI/UX
- 🌱 **Aprendiendo:** Nuevas tecnologías y mejores prácticas
- 🎯 **Objetivo:** Crear tecnología que genere impacto positivo

---

## 🛠️ Stack Tecnológico

&lt;div align="center"&gt;

### **Frontend**
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)

### **Backend**
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)

### **Herramientas de Diseño & Gestión**
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)
![Trello](https://img.shields.io/badge/Trello-0052CC?style=for-the-badge&logo=trello&logoColor=white)

&lt;/div&gt;

---

## 📊 Estadísticas GitHub

&lt;div align="center"&gt;
  &lt;img height="180em" src="https://github-readme-stats.vercel.app/api?username=<span class="highlight">tuusername</span>&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true"/&gt;
  &lt;img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=<span class="highlight">tuusername</span>&layout=compact&langs_count=7&theme=tokyonight"/&gt;
&lt;/div&gt;

&lt;div align="center"&gt;
  &lt;img src="https://github-readme-streak-stats.herokuapp.com/?user=<span class="highlight">tuusername</span>&theme=tokyonight" alt="GitHub Streak"/&gt;
&lt;/div&gt;

---

## 🌟 Proyectos Destacados

&lt;div align="center"&gt;

[![Proyecto Web](https://github-readme-stats.vercel.app/api/pin/?username=<span class="highlight">tuusername</span>&repo=<span class="highlight">proyecto-web</span>&theme=tokyonight)](https://github.com/<span class="highlight">tuusername</span>/<span class="highlight">proyecto-web</span>)
[![API Laravel](https://github-readme-stats.vercel.app/api/pin/?username=<span class="highlight">tuusername</span>&repo=<span class="highlight">api-laravel</span>&theme=tokyonight)](https://github.com/<span class="highlight">tuusername</span>/<span class="highlight">api-laravel</span>)

&lt;/div&gt;

### 🎯 En lo que estoy trabajando:
- 🌐 **E-commerce Platform** - Tienda online con React + Laravel
- 🤖 **Chatbot Inteligente** - Asistente virtual con Python
- 📱 **App de Gestión** - Sistema de tareas con React + PHP
- 🎨 **Portfolio Personal** - Showcase de proyectos con animaciones

---

## 💼 Experiencia

```python
class Jonas:
    def __init__(self):
        self.name = "Jonas Vidal Zenzano"
        self.role = "Estudiante de Ingeniería Informática"
        self.languages = ["Python", "Java", "PHP", "JavaScript"]
        self.frameworks = ["React", "Laravel"]
        self.tools = ["Figma", "Trello", "Git", "VS Code"]
        self.current_focus = "Full-Stack Development"
    
    def say_hi(self):
        print("¡Construyamos algo increíble juntos!")

jonas = Jonas()
jonas.say_hi()
```

---

## 🎯 Habilidades

&lt;div align="center"&gt;

**Desarrollo Frontend**  
🔹 Interfaces reactivas con React  
🔹 Diseño responsive con CSS3  
🔹 Experiencia de usuario optimizada  

**Desarrollo Backend**  
🔹 APIs RESTful con Laravel  
🔹 Lógica de negocio con Python/Java  
🔹 Gestión de bases de datos  

**Diseño & Gestión**  
🔹 Prototipado en Figma  
🔹 Gestión de proyectos con Trello  
🔹 Metodologías ágiles  

&lt;/div&gt;



---

&lt;div align="center"&gt;
  
### ✨ "El código limpio no es solo funcionalidad, es arte en forma de lógica"

&lt;img src="https://komarev.com/ghpvc/?username=<span class="highlight">tuusername</span>&color=blueviolet&style=flat-square&label=Visitas+al+perfil" alt="Profile views" /&gt;

&lt;/div&gt;

---

&lt;div align="center"&gt;
  &lt;img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer"/&gt;
&lt;/div&gt;</pre>
            </div>
        </div>

        <!-- Sección de Vista Previa -->
        <div class="preview-section">
            <div class="preview-header">
                👀 Cómo se vería en GitHub
            </div>
            <div class="preview-content">
                <h1>👨‍💻 Jonas Vidal Zenzano <span class="wave">👋</span></h1>
                
                <div class="typing-text">
                    Estudiante de Ingeniería Informática • Desarrollador Full-Stack
                </div>

                <hr>

                <h2>🚀 Sobre mí</h2>
                <p>¡Hola! Soy un estudiante de Ingeniería Informática apasionado por transformar ideas en soluciones digitales. Me especializo en desarrollo full-stack y disfruto creando experiencias web que realmente importen.</p>
                
                <ul>
                    <li>🎓 <strong>Estudiando:</strong> Ingeniería Informática</li>
                    <li>💻 <strong>Enfoque:</strong> Desarrollo Full-Stack & Diseño UI/UX</li>
                    <li>🌱 <strong>Aprendiendo:</strong> Nuevas tecnologías y mejores prácticas</li>
                    <li>🎯 <strong>Objetivo:</strong> Crear tecnología que genere impacto positivo</li>
                </ul>

                <hr>

                <h2>🛠️ Stack Tecnológico</h2>
                
                <div class="center">
                    <h3><strong>Frontend</strong></h3>
                    <span class="badge html-badge">HTML5</span>
                    <span class="badge css-badge">CSS3</span>
                    <span class="badge react-badge">React</span>
                    
                    <h3><strong>Backend</strong></h3>
                    <span class="badge python-badge">Python</span>
                    <span class="badge java-badge">Java</span>
                    <span class="badge php-badge">PHP</span>
                    <span class="badge laravel-badge">Laravel</span>
                    
                    <h3><strong>Herramientas de Diseño & Gestión</strong></h3>
                    <span class="badge figma-badge">Figma</span>
                    <span class="badge trello-badge">Trello</span>
                </div>

                <hr>

                <h2>📊 Estadísticas GitHub</h2>
                <div class="stats-placeholder">
                    <strong>📈 GitHub Stats</strong><br>
                    Commits: 284 | Stars: 23 | PRs: 45<br>
                    <em>Aquí aparecerán tus estadísticas reales de GitHub</em>
                </div>
                
                <div class="stats-placeholder">
                    <strong>🔥 GitHub Streak</strong><br>
                    Current Streak: 25 días | Longest: 45 días<br>
                    <em>Tu racha de commits aparecerá aquí</em>
                </div>

                <hr>

                <h2>💼 Experiencia</h2>
                <div class="code-block">
<pre>class Jonas:
    def __init__(self):
        self.name = "Jonas Vidal Zenzano"
        self.role = "Estudiante de Ingeniería Informática"
        self.languages = ["Python", "Java", "PHP", "JavaScript"]
        self.frameworks = ["React", "Laravel"]
        self.tools = ["Figma", "Trello", "Git", "VS Code"]
        self.current_focus = "Full-Stack Development"
    
    def say_hi(self):
        print("¡Construyamos algo increíble juntos!")

jonas = Jonas()
jonas.say_hi()</pre>
                </div>

                <hr>

                <h2>🎯 Habilidades</h2>
                <div class="skills-grid">
                    <div class="skill-item">
                        <strong>Desarrollo Frontend</strong><br>
                        🔹 Interfaces reactivas con React<br>
                        🔹 Diseño responsive con CSS3<br>
                        🔹 Experiencia de usuario optimizada
                    </div>
                    <div class="skill-item">
                        <strong>Desarrollo Backend</strong><br>
                        🔹 APIs RESTful con Laravel<br>
                        🔹 Lógica de negocio con Python/Java<br>
                        🔹 Gestión de bases de datos
                    </div>
                    <div class="skill-item">
                        <strong>Diseño & Gestión</strong><br>
                        🔹 Prototipado en Figma<br>
                        🔹 Gestión de proyectos con Trello<br>
                        🔹 Metodologías ágiles
                    </div>
                </div>

                <hr>

                <h2>📫 Conecta conmigo</h2>
                <div class="social-links">
                    <a href="#" class="badge linkedin-badge">LinkedIn</a>
                    <a href="#" class="badge github-badge">GitHub</a>
                    <a href="#" class="badge email-badge">Gmail</a>
                    <a href="#" class="badge portfolio-badge">Portfolio</a>
                </div>

                <div class="center">
                    <h3>✨ "El código limpio no es solo funcionalidad, es arte en forma de lógica"</h3>
                    <p><span style="background: #8b5cf6; color: white; padding: 4px 12px; border-radius: 12px; font-size: 0.9em;">Visitas al perfil: 1,234</span></p>
                </div>
            </div>
        </div>
    </div>

    <script>
        function copyCode() {
            const codeElement = document.getElementById('readme-code');
            const text = codeElement.textContent;
            
            navigator.clipboard.writeText(text).then(function() {
                const button = document.querySelector('.copy-button');
                const originalText = button.textContent;
                button.textContent = '¡Copiado!';
                button.style.background = '#28a745';
                
                setTimeout(() => {
                    button.textContent = originalText;
                    button.style.background = '#0366d6';
                }, 2000);
            });
        }
    </script>
</body>
</html>
