<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Portfólio - Desenvolvedor Web</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            scroll-behavior: smooth;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }
        
        .glass-effect {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .gradient-text {
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .skill-bar {
            transition: width 2s ease-in-out;
        }
        
        .project-card {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        
        .typewriter {
            overflow: hidden;
            border-right: .15em solid #4ecdc4;
            white-space: nowrap;
            animation: typing 3.5s steps(40, end), blink-caret .75s step-end infinite;
        }
        
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: #4ecdc4 }
        }
        
        .floating {
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0px); }
        }
    </style>
</head>
<body class="text-white">
    <!-- Header/Navigation -->
    <header class="fixed w-full z-50 glass-effect">
        <nav class="container mx-auto px-6 py-4">
            <div class="flex justify-between items-center">
                <div class="text-2xl font-bold gradient-text">
                    <a href="#" class="hover:text-white transition-colors">Portfólio</a>
                </div>
                
                <div class="hidden md:flex space-x-8">
                    <a href="#home" class="hover:text-[#4ecdc4] transition-colors">Início</a>
                    <a href="#about" class="hover:text-[#4ecdc4] transition-colors">Sobre</a>
                    <a href="#skills" class="hover:text-[#4ecdc4] transition-colors">Habilidades</a>
                    <a href="#projects" class="hover:text-[#4ecdc4] transition-colors">Projetos</a>
                    <a href="#contact" class="hover:text-[#4ecdc4] transition-colors">Contato</a>
                </div>
                
                <div class="md:hidden">
                    <button id="menu-btn" class="text-white focus:outline-none">
                        <i class="fas fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
            
            <!-- Mobile Menu -->
            <div id="mobile-menu" class="hidden md:hidden mt-4 space-y-4 pb-4">
                <a href="#home" class="block hover:text-[#4ecdc4] transition-colors">Início</a>
                <a href="#about" class="block hover:text-[#4ecdc4] transition-colors">Sobre</a>
                <a href="#skills" class="block hover:text-[#4ecdc4] transition-colors">Habilidades</a>
                <a href="#projects" class="block hover:text-[#4ecdc4] transition-colors">Projetos</a>
                <a href="#contact" class="block hover:text-[#4ecdc4] transition-colors">Contato</a>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="min-h-screen flex items-center justify-center pt-20">
        <div class="container mx-auto px-6 text-center">
            <div class="floating mb-8">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/feea5279-cc22-4ed2-8367-a1295ad2b1c4.png" alt="Foto de perfil profissional de desenvolvedor web com fundo moderno" class="w-64 h-64 rounded-full mx-auto border-4 border-white/20 shadow-2xl">
            </div>
            
            <h1 class="text-5xl md:text-7xl font-bold mb-6 typewriter">
                Olá, eu sou <span class="gradient-text">Desenvolvedor</span>
            </h1>
            
            <p class="text-xl md:text-2xl mb-8 text-white/90 max-w-3xl mx-auto">
                Criando experiências digitais incríveis com foco em performance, design e usabilidade.
            </p>
            
            <div class="flex flex-col sm:flex-row gap-4 justify-center">
                <a href="#projects" class="bg-[#4ecdc4] hover:bg-[#45b7d1] text-white font-semibold py-3 px-8 rounded-full transition-colors transform hover:scale-105">
                    Ver Projetos
                </a>
                <a href="#contact" class="border-2 border-white/30 hover:border-[#4ecdc4] text-white font-semibold py-3 px-8 rounded-full transition-all transform hover:scale-105">
                    Entrar em Contato
                </a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 bg-white/5">
        <div class="container mx-auto px-6">
            <h2 class="text-4xl font-bold text-center mb-16 gradient-text">Sobre Mim</h2>
            
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div>
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/eea70eb3-44cd-4dd0-ba78-3a8c3e91e633.png" alt="Desenvolvedor trabalhando em ambiente moderno com laptop e café" class="rounded-2xl shadow-2xl w-full">
                </div>
                
                <div>
                    <h3 class="text-2xl font-semibold mb-6">Paixão por criar soluções digitais</h3>
                    <p class="text-lg mb-6 text-white/90">
                        Sou um desenvolvedor web apaixonado por transformar ideias em realidade digital. 
                        Com experiência em diversas tecnologias modernas, busco sempre entregar 
                        produtos que não apenas funcionem perfeitamente, mas que também proporcionem 
                        uma experiência excepcional ao usuário.
                    </p>
                    
                    <p class="text-lg mb-8 text-white/90">
                        Meu foco está em criar aplicações web responsivas, acessíveis e de alto 
                        desempenho, sempre seguindo as melhores práticas de desenvolvimento.
                    </p>
                    
                    <div class="grid grid-cols-2 gap-4">
                        <div class="text-center p-4 glass-effect rounded-lg">
                            <div class="text-3xl font-bold gradient-text">50+</div>
                            <div class="text-white/80">Projetos Concluídos</div>
                        </div>
                        <div class="text-center p-4 glass-effect rounded-lg">
                            <div class="text-3xl font-bold gradient-text">3+</div>
                            <div class="text-white/80">Anos de Experiência</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-20">
        <div class="container mx-auto px-6">
            <h2 class="text-4xl font-bold text-center mb-16 gradient-text">Minhas Habilidades</h2>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Frontend Skills -->
                <div class="glass-effect p-6 rounded-2xl">
                    <div class="text-center mb-6">
                        <i class="fas fa-paint-brush text-4xl gradient-text mb-4"></i>
                        <h3 class="text-xl font-semibold">Frontend</h3>
                    </div>
                    <div class="space-y-4">
                        <div>
                            <div class="flex justify-between mb-2">
                                <span>HTML/CSS</span>
                                <span>95%</span>
                            </div>
                            <div class="w-full bg-white/20 rounded-full h-2">
                                <div class="skill-bar bg-[#4ecdc4] h-2 rounded-full" style="width: 95%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span>JavaScript</span>
                                <span>90%</span>
                            </div>
                            <div class="w-full bg-white/20 rounded-full h-2">
                                <div class="skill-bar bg-[#4ecdc4] h-2 rounded-full" style="width: 90%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span>React</span>
                                <span>85%</span>
                            </div>
                            <div class="w-full bg-white/20 rounded-full h-2">
                                <div class="skill-bar bg-[#4ecdc4] h-2 rounded-full" style="width: 85%"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Backend Skills -->
                <div class="glass-effect p-6 rounded-2xl">
                    <div class="text-center mb-6">
                        <i class="fas fa-server text-4xl gradient-text mb-4"></i>
                        <h3 class="text-xl font-semibold">Backend</h3>
                    </div>
                    <div class="space-y-4">
                        <div>
                            <div class="flex justify-between mb-2">
                                <span>Node.js</span>
                                <span>88%</span>
                            </div>
                            <div class="w-full bg-white/20 rounded-full h-2">
                                <div class="skill-bar bg-[#4ecdc4] h-2 rounded-full" style="width: 88%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span>Python</span>
                                <span>82%</span>
                            </div>
                            <div class="w-full bg-white/20 rounded-full h-2">
                                <div class="skill-bar bg-[#4ecdc4] h-2 rounded-full" style="width: 82%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span>MySQL</span>
                                <span>85%</span>
                            </div>
                            <div class="w-full bg-white/20 rounded-full h-2">
                                <div class="skill-bar bg-[#4ecdc4] h-2 rounded-full" style="width: 85%"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Tools -->
                <div class="glass-effect p-6 rounded-2xl">
                    <div class="text-center mb-6">
                        <i class="fas fa-tools text-4xl gradient-text mb-4"></i>
                        <h3 class="text-xl font-semibold">Ferramentas</h3>
                    </div>
                    <div class="space-y-4">
                        <div>
                            <div class="flex justify-between mb-2">
                                <span>Git</span>
                                <span>90%</span>
                            </div>
                            <div class="w-full bg-white/20 rounded-full h-2">
                                <div class="skill-bar bg-[#4ecdc4] h-2 rounded-full" style="width: 90%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span>Figma</span>
                                <span>80%</span>
                            </div>
                            <div class="w-full bg-white/20 rounded-full h-2">
                                <div class="skill-bar bg-[#4ecdc4] h-2 rounded-full" style="width: 80%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span>Docker</span>
                                <span>75%</span>
                            </div>
                            <div class="w-full bg-white/20 rounded-full h-2">
                                <div class="skill-bar bg-[#4ecdc4] h-2 rounded-full" style="width: 75%"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-20 bg-white/5">
        <div class="container mx-auto px-6">
            <h2 class="text-4xl font-bold text-center mb-16 gradient-text">Projetos Recentes</h2>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Project 1 -->
                <div class="project-card glass-effect rounded-2xl overflow-hidden">
                    <div class="h-48 overflow-hidden">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/27e5c019-e0fa-46a1-97fe-60800495b939.png" alt="Dashboard moderno de analytics com gráficos e métricas em tempo real" class="w-full h-full object-cover transition-transform duration-300 hover:scale-110">
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-2">Dashboard Analytics</h3>
                        <p class="text-white/80 mb-4">Plataforma de analytics em tempo real com visualizações interativas e relatórios personalizados.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-[#4ecdc4]/20 text-[#4ecdc4] px-3 py-1 rounded-full text-sm">React</span>
                            <span class="bg-[#4ecdc4]/20 text-[#4ecdc4] px-3 py-1 rounded-full text-sm">Node.js</span>
                            <span class="bg-[#4ecdc4]/20 text-[#4ecdc4] px-3 py-1 rounded-full text-sm">MongoDB</span>
                        </div>
                        <a href="#" class="text-[#4ecdc4] hover:text-white transition-colors font-semibold">
                            Ver Projeto →
                        </a>
                    </div>
                </div>

                <!-- Project 2 -->
                <div class="project-card glass-effect rounded-2xl overflow-hidden">
                    <div class="h-48 overflow-hidden">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/85d71314-0edd-4a81-984e-7c1c3339abb5.png" alt="Aplicativo móvel de e-commerce com interface limpa e moderna" class="w-full h-full object-cover transition-transform duration-300 hover:scale-110">
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-2">E-commerce Mobile</h3>
                        <p class="text-white/80 mb-4">Aplicativo de comércio eletrônico com carrinho, pagamentos e sistema de recomendação.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-[#4ecdc4]/20 text-[#4ecdc4] px-3 py-1 rounded-full text-sm">React Native</span>
                            <span class="bg-[#4ecdc4]/20 text-[#4ecdc4] px-3 py-1 rounded-full text-sm">Firebase</span>
                            <span class="bg-[#4ecdc4]/20 text-[#4ecdc4] px-3 py-1 rounded-full text-sm">Stripe</span>
                        </div>
                        <a href="#" class="text-[#4ecdc4] hover:text-white transition-colors font-semibold">
                            Ver Projeto →
                        </a>
                    </div>
                </div>

                <!-- Project 3 -->
                <div class="project-card glass-effect rounded-2xl overflow-hidden">
                    <div class="h-48 overflow-hidden">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/75eb5612-fc56-43a5-8ce2-2d1796b9e86b.png" alt="Interface de blog moderno com layout limpo e tipografia elegante" class="w-full h-full object-cover transition-transform duration-300 hover:scale-110">
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-2">Plataforma de Blog</h3>
                        <p class="text-white/80 mb-4">Sistema de gerenciamento de conteúdo com editor markdown e sistema de comentários.</p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-[#4ecdc4]/20 text-[#4ecdc4] px-3 py-1 rounded-full text-sm">Next.js</span>
                            <span class="bg-[#4ecdc4]/20 text-[#4ecdc4] px-3 py-1 rounded-full text-sm">Sanity</span>
                            <span class="bg-[#4ecdc4]/20 text-[#4ecdc4] px-3 py-1 rounded-full text-sm">Tailwind</span>
                        </div>
                        <a href="#" class="text-[#4ecdc4] hover:text-white transition-colors font-semibold">
                            Ver Projeto →
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20">
        <div class="container mx-auto px-6">
            <h2 class="text-4xl font-bold text-center mb-16 gradient-text">Vamos Trabalhar Juntos</h2>
            
            <div class="grid md:grid-cols-2 gap-12">
                <div>
                    <h3 class="text-2xl font-semibold mb-6">Entre em Contato</h3>
                    <p class="text-lg mb-8 text-white/90">
                        Estou sempre aberto a discutir novos projetos, oportunidades criativas ou 
                        fazer parte de sua visão. Vamos conversar!
                    </p>
                    
                    <div class="space-y-4">
                        <div class="flex items-center">
                            <i class="fas fa-envelope text-[#4ecdc4] text-xl mr-4"></i>
                            <span>email@exemplo.com</span>
                        </div>
                        <div class="flex items-center">
                            <i class="fas fa-phone text-[#4ecdc4] text-xl mr-4"></i>
                            <span>+
                            # Fael
Mande suas ideia e eu a transformarei em um sucesso 
