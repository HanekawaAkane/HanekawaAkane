<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🌟 我的 GitHub 主页</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.8/dist/chart.umd.min.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Tailwind 配置 -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#6366F1', // 主色调：紫色
                        secondary: '#06B6D4', // 辅助色：青色
                        accent: '#EC4899', // 强调色：粉色
                        dark: '#1E293B', // 深色背景
                        light: '#F8FAFC', // 浅色背景
                    },
                    fontFamily: {
                        inter: ['Inter', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .text-shadow {
                text-shadow: 0 2px 4px rgba(0,0,0,0.1);
            }
            .text-gradient {
                background-clip: text;
                -webkit-background-clip: text;
                -webkit-text-fill-color: transparent;
            }
            .animate-float {
                animation: float 3s ease-in-out infinite;
            }
            .animate-pulse-slow {
                animation: pulse 4s cubic-bezier(0.4, 0, 0.6, 1) infinite;
            }
            .bg-grid {
                background-size: 20px 20px;
                background-image: 
                    linear-gradient(to right, rgba(255,255,255,0.05) 1px, transparent 1px),
                    linear-gradient(to bottom, rgba(255,255,255,0.05) 1px, transparent 1px);
            }
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
    </style>
</head>
<body class="font-inter bg-gradient-to-br from-dark to-gray-900 text-light min-h-screen">
    <!-- 导航栏 -->
    <nav class="fixed w-full top-0 z-50 bg-dark/80 backdrop-blur-md border-b border-gray-800 transition-all duration-300" id="navbar">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <a href="#" class="flex items-center gap-2">
                <span class="text-2xl text-primary font-bold">Dev<span class="text-accent">Pro</span></span>
            </a>
            
            <div class="hidden md:flex items-center gap-6">
                <a href="#about" class="text-gray-300 hover:text-primary transition-colors">关于我</a>
                <a href="#skills" class="text-gray-300 hover:text-primary transition-colors">技术栈</a>
                <a href="#projects" class="text-gray-300 hover:text-primary transition-colors">项目</a>
                <a href="#stats" class="text-gray-300 hover:text-primary transition-colors">统计</a>
                <a href="#contact" class="bg-primary hover:bg-primary/90 text-white px-4 py-2 rounded-lg transition-all transform hover:scale-105">联系我</a>
            </div>
            
            <button class="md:hidden text-2xl text-gray-300" id="menu-toggle">
                <i class="fa fa-bars"></i>
            </button>
        </div>
        
        <!-- 移动端菜单 -->
        <div class="md:hidden hidden bg-dark/95 backdrop-blur-lg absolute w-full border-b border-gray-800" id="mobile-menu">
            <div class="container mx-auto px-4 py-3 flex flex-col gap-4">
                <a href="#about" class="text-gray-300 hover:text-primary transition-colors py-2">关于我</a>
                <a href="#skills" class="text-gray-300 hover:text-primary transition-colors py-2">技术栈</a>
                <a href="#projects" class="text-gray-300 hover:text-primary transition-colors py-2">项目</a>
                <a href="#stats" class="text-gray-300 hover:text-primary transition-colors py-2">统计</a>
                <a href="#contact" class="bg-primary hover:bg-primary/90 text-white px-4 py-2 rounded-lg transition-all text-center">联系我</a>
            </div>
        </div>
    </nav>

    <!-- 英雄区域 -->
    <header class="pt-32 pb-20 px-4 relative overflow-hidden">
        <div class="absolute inset-0 bg-grid opacity-30"></div>
        <div class="absolute -right-10 -top-10 w-64 h-64 bg-primary/20 rounded-full blur-3xl animate-pulse-slow"></div>
        <div class="absolute -left-10 bottom-10 w-64 h-64 bg-accent/20 rounded-full blur-3xl animate-pulse-slow"></div>
        
        <div class="container mx-auto relative z-10">
            <div class="flex flex-col md:flex-row items-center gap-10">
                <div class="md:w-1/2 space-y-6">
                    <h1 class="text-[clamp(2.5rem,5vw,4rem)] font-bold leading-tight">
                        <span class="block text-gradient bg-gradient-to-r from-primary to-secondary">你好，我是开发者</span>
                        <span class="block text-white">专注于全栈开发与人工智能</span>
                    </h1>
                    <p class="text-lg text-gray-300 max-w-xl">
                        拥有丰富经验的全栈工程师，擅长Java、Python、PyTorch等多种技术栈，致力于构建高效、创新的软件解决方案。
                    </p>
                    <div class="flex flex-wrap gap-4 pt-4">
                        <a href="#projects" class="bg-primary hover:bg-primary/90 text-white px-6 py-3 rounded-lg transition-all transform hover:scale-105 flex items-center gap-2">
                            <i class="fa fa-code"></i> 查看项目
                        </a>
                        <a href="#contact" class="bg-transparent border-2 border-gray-700 hover:border-primary text-white px-6 py-3 rounded-lg transition-all transform hover:scale-105 flex items-center gap-2">
                            <i class="fa fa-envelope"></i> 联系我
                        </a>
                    </div>
                </div>
                
                <div class="md:w-1/2 flex justify-center">
                    <div class="relative w-64 h-64 md:w-80 md:h-80">
                        <div class="absolute inset-0 bg-gradient-to-tr from-primary to-accent rounded-full blur-xl opacity-60 animate-pulse-slow"></div>
                        <div class="absolute inset-1 bg-dark rounded-full overflow-hidden border-4 border-gray-800">
                            <img src="https://picsum.photos/seed/devprofile/400/400" alt="开发者照片" class="w-full h-full object-cover mix-blend-luminosity hover:mix-blend-normal transition-all duration-500">
                        </div>
                        <div class="absolute -bottom-5 -right-5 bg-dark/80 backdrop-blur-md border border-gray-800 rounded-lg p-4 shadow-lg animate-float">
                            <div class="flex items-center gap-3">
                                <div class="w-10 h-10 bg-green-500 rounded-full flex items-center justify-center text-white">
                                    <i class="fa fa-code"></i>
                                </div>
                                <div>
                                    <p class="text-xs text-gray-400">当前项目</p>
                                    <p class="text-sm font-medium">AI 图像识别系统</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- 关于我 -->
    <section id="about" class="py-20 px-4 bg-gray-900/50 relative">
        <div class="absolute inset-0 bg-grid opacity-20"></div>
        <div class="container mx-auto relative z-10">
            <div class="text-center mb-16">
                <h2 class="text-[clamp(1.8rem,4vw,3rem)] font-bold mb-4">
                    <span class="text-gradient bg-gradient-to-r from-primary to-secondary">关于我</span>
                </h2>
                <p class="text-gray-400 max-w-2xl mx-auto">探索我的技术旅程和专业背景</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
                <div class="space-y-6">
                    <p class="text-gray-300 text-lg">
                        你好！我是一名热衷于技术创新的全栈工程师，拥有超过5年的软件开发经验。我擅长将复杂的问题转化为优雅、高效的解决方案。
                    </p>
                    <p class="text-gray-300">
                        我的技术栈涵盖后端开发、机器学习和前端框架。我相信持续学习和技术创新是保持竞争力的关键，因此我不断探索新的技术领域并将其应用到实际项目中。
                    </p>
                    
                    <div class="grid grid-cols-2 gap-6 pt-4">
                        <div class="bg-dark/50 border border-gray-800 rounded-xl p-6 hover:border-primary/50 transition-all">
                            <div class="text-primary text-3xl mb-2">
                                <i class="fa fa-code"></i>
                            </div>
                            <h3 class="text-xl font-semibold mb-2">全栈开发</h3>
                            <p class="text-gray-400">从后端到前端，构建完整的应用解决方案</p>
                        </div>
                        
                        <div class="bg-dark/50 border border-gray-800 rounded-xl p-6 hover:border-primary/50 transition-all">
                            <div class="text-secondary text-3xl mb-2">
                                <i class="fa fa-rocket"></i>
                            </div>
                            <h3 class="text-xl font-semibold mb-2">AI 与机器学习</h3>
                            <p class="text-gray-400">使用 PyTorch 等框架构建智能应用</p>
                        </div>
                    </div>
                </div>
                
                <div class="bg-dark/50 border border-gray-800 rounded-2xl p-8 relative overflow-hidden">
                    <div class="absolute top-0 right-0 w-40 h-40 bg-primary/10 rounded-full blur-3xl"></div>
                    
                    <div class="space-y-6 relative z-10">
                        <div class="flex justify-between items-center">
                            <div class="flex items-center gap-3">
                                <div class="w-12 h-12 bg-primary/20 rounded-lg flex items-center justify-center text-primary">
                                    <i class="fa fa-graduation-cap text-xl"></i>
                                </div>
                                <div>
                                    <h3 class="font-semibold text-lg">计算机科学硕士</h3>
                                    <p class="text-gray-400">顶尖科技大学</p>
                                </div>
                            </div>
                            <span class="bg-primary/20 text-primary px-3 py-1 rounded-full text-sm">2018-2021</span>
                        </div>
                        
                        <div class="h-1 bg-gray-800 rounded-full overflow-hidden">
                            <div class="h-full bg-gradient-to-r from-primary to-secondary" style="width: 85%"></div>
                        </div>
                        
                        <div class="flex justify-between items-center">
                            <div class="flex items-center gap-3">
                                <div class="w-12 h-12 bg-secondary/20 rounded-lg flex items-center justify-center text-secondary">
                                    <i class="fa fa-briefcase text-xl"></i>
                                </div>
                                <div>
                                    <h3 class="font-semibold text-lg">高级软件工程师</h3>
                                    <p class="text-gray-400">科技巨头公司</p>
                                </div>
                            </div>
                            <span class="bg-secondary/20 text-secondary px-3 py-1 rounded-full text-sm">2021-至今</span>
                        </div>
                        
                        <div class="h-1 bg-gray-800 rounded-full overflow-hidden">
                            <div class="h-full bg-gradient-to-r from-secondary to-accent" style="width: 70%"></div>
                        </div>
                        
                        <div class="flex justify-between items-center">
                            <div class="flex items-center gap-3">
                                <div class="w-12 h-12 bg-accent/20 rounded-lg flex items-center justify-center text-accent">
                                    <i class="fa fa-users text-xl"></i>
                                </div>
                                <div>
                                    <h3 class="font-semibold text-lg">开源贡献者</h3>
                                    <p class="text-gray-400">多个热门项目</p>
                                </div>
                            </div>
                            <span class="bg-accent/20 text-accent px-3 py-1 rounded-full text-sm">2017-至今</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 技术栈 -->
    <section id="skills" class="py-20 px-4 relative">
        <div class="absolute -top-20 left-0 w-full h-20 bg-gradient-to-b from-gray-900/50 to-transparent"></div>
        <div class="container mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-[clamp(1.8rem,4vw,3rem)] font-bold mb-4">
                    <span class="text-gradient bg-gradient-to-r from-primary to-secondary">技术栈</span>
                </h2>
                <p class="text-gray-400 max-w-2xl mx-auto">我熟练掌握的编程语言和工具</p>
            </div>
            
            <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
                <!-- Java -->
                <div class="bg-dark/50 border border-gray-800 rounded-xl p-6 hover:border-primary/50 transition-all group">
                    <div class="w-16 h-16 bg-red-600/20 rounded-lg flex items-center justify-center text-red-500 text-3xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fa fa-coffee"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Java</h3>
                    <p class="text-gray-400 text-sm">企业级应用开发、Spring框架、微服务</p>
                    <div class="mt-4 h-1 bg-gray-800 rounded-full overflow-hidden">
                        <div class="h-full bg-red-500" style="width: 90%"></div>
                    </div>
                </div>
                
                <!-- Python -->
                <div class="bg-dark/50 border border-gray-800 rounded-xl p-6 hover:border-primary/50 transition-all group">
                    <div class="w-16 h-16 bg-yellow-500/20 rounded-lg flex items-center justify-center text-yellow-500 text-3xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fa fa-code"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Python</h3>
                    <p class="text-gray-400 text-sm">数据科学、机器学习、Web开发</p>
                    <div class="mt-4 h-1 bg-gray-800 rounded-full overflow-hidden">
                        <div class="h-full bg-yellow-500" style="width: 95%"></div>
                    </div>
                </div>
                
                <!-- PyTorch -->
                <div class="bg-dark/50 border border-gray-800 rounded-xl p-6 hover:border-primary/50 transition-all group">
                    <div class="w-16 h-16 bg-orange-500/20 rounded-lg flex items-center justify-center text-orange-500 text-3xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fa fa-brain"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">PyTorch</h3>
                    <p class="text-gray-400 text-sm">深度学习、神经网络、计算机视觉</p>
                    <div class="mt-4 h-1 bg-gray-800 rounded-full overflow-hidden">
                        <div class="h-full bg-orange-500" style="width: 85%"></div>
                    </div>
                </div>
                
                <!-- Perl -->
                <div class="bg-dark/50 border border-gray-800 rounded-xl p-6 hover:border-primary/50 transition-all group">
                    <div class="w-16 h-16 bg-blue-500/20 rounded-lg flex items-center justify-center text-blue-500 text-3xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fa fa-terminal"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Perl</h3>
                    <p class="text-gray-400 text-sm">脚本编程、系统管理、文本处理</p>
                    <div class="mt-4 h-1 bg-gray-800 rounded-full overflow-hidden">
                        <div class="h-full bg-blue-500" style="width: 75%"></div>
                    </div>
                </div>
                
                <!-- Go -->
                <div class="bg-dark/50 border border-gray-800 rounded-xl p-6 hover:border-primary/50 transition-all group">
                    <div class="w-16 h-16 bg-blue-400/20 rounded-lg flex items-center justify-center text-blue-400 text-3xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fa fa-bolt"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Go</h3>
                    <p class="text-gray-400 text-sm">高性能服务、云原生应用、微服务</p>
                    <div class="mt-4 h-1 bg-gray-800 rounded-full overflow-hidden">
                        <div class="h-full bg-blue-400" style="width: 80%"></div>
                    </div>
                </div>
                
                <!-- C++ -->
                <div class="bg-dark/50 border border-gray-800 rounded-xl p-6 hover:border-primary/50 transition-all group">
                    <div class="w-16 h-16 bg-blue-600/20 rounded-lg flex items-center justify-center text-blue-600 text-3xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fa fa-cogs"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">C++</h3>
                    <p class="text-gray-400 text-sm">系统编程、游戏开发、高性能计算</p>
                    <div class="mt-4 h-1 bg-gray-800 rounded-full overflow-hidden">
                        <div class="h-full bg-blue-600" style="width: 70%"></div>
                    </div>
                </div>
                
                <!-- Vue -->
                <div class="bg-dark/50 border border-gray-800 rounded-xl p-6 hover:border-primary/50 transition-all group">
                    <div class="w-16 h-16 bg-green-500/20 rounded-lg flex items-center justify-center text-green-500 text-3xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fa fa-th-large"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Vue.js</h3>
                    <p class="text-gray-400 text-sm">前端框架、SPA开发、组件化设计</p>
                    <div class="mt-4 h-1 bg-gray-800 rounded-full overflow-hidden">
                        <div class="h-full bg-green-500" style="width: 85%"></div>
                    </div>
                </div>
                
                <!-- 更多技能 -->
                <div class="bg-dark/50 border border-gray-800 rounded-xl p-6 hover:border-primary/50 transition-all group flex flex-col items-center justify-center">
                    <div class="w-16 h-16 bg-gray-700/20 rounded-lg flex items-center justify-center text-gray-400 text-3xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fa fa-ellipsis-h"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">更多技能</h3>
                    <div class="grid grid-cols-2 gap-2 mt-4 w-full">
                        <span class="bg-gray-800 text-gray-300 text-xs px-2 py-1 rounded-full text-center">Docker</span>
                        <span class="bg-gray-800 text-gray-300 text-xs px-2 py-1 rounded-full text-center">Kubernetes</span>
                        <span class="bg-gray-800 text-gray-300 text-xs px-2 py-1 rounded-full text-center">PostgreSQL</span>
                        <span class="bg-gray-800 text-gray-300 text-xs px-2 py-1 rounded-full text-center">MongoDB</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 项目展示 -->
    <section id="projects" class="py-20 px-4 bg-gray-900/50 relative">
        <div class="absolute inset-0 bg-grid opacity-20"></div>
        <div class="container mx-auto relative z-10">
            <div class="text-center mb-16">
                <h2 class="text-[clamp(1.8rem,4vw,3rem)] font-bold mb-4">
                    <span class="text-gradient bg-gradient-to-r from-primary to-secondary">项目展示</span>
                </h2>
                <p class="text-gray-400 max-w-2xl mx-auto">探索我的开源和商业项目</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- 项目1 -->
                <div class="bg-dark/50 border border-gray-800 rounded-xl overflow-hidden group hover:border-primary/50 transition-all transform hover:-translate-y-2 duration-300">
                    <div class="relative h-48 overflow-hidden">
                        <img src="https://picsum.photos/seed/project1/600/400" alt="AI 图像识别系统" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-dark to-transparent"></div>
                        <div class="absolute bottom-4 left-4">
                            <span class="bg-primary/80 text-white text-xs px-2 py-1 rounded-full">PyTorch</span>
                            <span class="bg-secondary/80 text-white text-xs px-2 py-1 rounded-full ml-2">Python</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-2 group-hover:text-primary transition-colors">AI 图像识别系统</h3>
                        <p class="text-gray-400 text-sm mb-4">基于深度学习的图像识别系统，能够准确识别和分类各种图像内容，应用于安防监控和智能相册等场景。</p>
                        <div class="flex justify-between items-center">
                            <div class="flex items-center gap-2">
                                <span class="text-gray-400 text-sm"><i class="fa fa-star text-yellow-500"></i> 245</span>
                                <span class="text-gray-400 text-sm"><i class="fa fa-code-fork"></i> 89</span>
                            </div>
                            <a href="#" class="text-primary hover:text-primary/80 text-sm flex items-center gap-1">
                                查看详情 <i class="fa fa-arrow-right"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- 项目2 -->
                <div class="bg-dark/50 border border-gray-800 rounded-xl overflow-hidden group hover:border-primary/50 transition-all transform hover:-translate-y-2 duration-300">
                    <div class="relative h-48 overflow-hidden">
                        <img src="https://picsum.photos/seed/project2/600/400" alt="微服务电商平台" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-dark to-transparent"></div>
                        <div class="absolute bottom-4 left-4">
                            <span class="bg-blue-500/80 text-white text-xs px-2 py-1 rounded-full">Java</span>
                            <span class="bg-green-500/80 text-white text-xs px-2 py-1 rounded-full ml-2">Spring</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-2 group-hover:text-primary transition-colors">微服务电商平台</h3>
                        <p class="text-gray-400 text-sm mb-4">基于Spring Cloud的微服务架构电商平台，支持高并发交易和分布式系统，具有良好的扩展性和容错性。</p>
                        <div class="flex justify-between items-center">
                            <div class="flex items-center gap-2">
                                <span class="text-gray-400 text-sm"><i class="fa fa-star text-yellow-500"></i> 187</span>
                                <span class="text-gray-400 text-sm"><i class="fa fa-code-fork"></i> 64</span>
                            </div>
                            <a href="#" class="text-primary hover:text-primary/80 text-sm flex items-center gap-1">
                                查看详情 <i class="fa fa-arrow-right"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- 项目3 -->
                <div class="bg-dark/50 border border-gray-800 rounded-xl overflow-hidden group hover:border-primary/50 transition-all transform hover:-translate-y-2 duration-300">
                    <div class="relative h-48 overflow-hidden">
                        <img src="https://picsum.photos/seed/project3/600/400" alt="实时数据可视化平台" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-dark to-transparent"></div>
                        <div class="absolute bottom-4 left-4">
                            <span class="bg-green-500/80 text-white text-xs px-2 py-1 rounded-full">Vue.js</span>
                            <span class="bg-orange-500/80 text-white text-xs px-2 py-1 rounded-full ml-2">Node.js</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-2 group-hover:text-primary transition-colors">实时数据可视化平台</h3>
                        <p class="text-gray-400 text-sm mb-4">使用Vue.js和D3.js构建的实时数据可视化平台，支持多种图表类型和交互式数据展示，适用于监控和分析系统。</p>
                        <div class="flex justify-between items-center">
                            <div class="flex items-center gap-2">
                                <span class="text-gray-400 text-sm"><i class="fa fa-star text-yellow-500"></i> 156</span>
                                <span class="text-gray-400 text-sm"><i class="fa fa-code-fork"></i> 42</span>
                            </div>
                            <a href="#" class="text-primary hover:text-primary/80 text-sm flex items-center gap-1">
                                查看详情 <i class="fa fa-arrow-right"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- 项目4 -->
                <div class="bg-dark/50 border border-gray-800 rounded-xl overflow-hidden group hover:border-primary/50 transition-all transform hover:-translate-y-2 duration-300">
                    <div class="relative h-48 overflow-hidden">
                        <img src="https://picsum.photos/seed/project4/600/400" alt="高性能API网关" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-dark to-transparent"></div>
                        <div class="absolute bottom-4 left-4">
                            <span class="bg-blue-400/80 text-white text-xs px-2 py-1 rounded-full">Go</span>
                            <span class="bg-purple-500/80 text-white text-xs px-2 py-1 rounded-full ml-2">gRPC</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-2 group-hover:text-primary transition-colors">高性能API网关</h3>
                        <p class="text-gray-400 text-sm mb-4">基于Go语言开发的高性能API网关，支持负载均衡、限流、认证等功能，为微服务架构提供统一的入口。</p>
                        <div class="flex justify-between items-center">
                            <div class="flex items-center gap-2">
                                <span class="text-gray-400 text-sm"><i class="fa fa-star text-yellow-500"></i> 112</span>
                                <span class="text-gray-400 text-sm"><i class="fa fa-code-fork"></i> 37</span>
                            </div>
                            <a href="#" class="text-primary hover:text-primary/80 text-sm flex items-center gap-1">
                                查看详情 <i class="fa fa-arrow-right"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- 项目5 -->
                <div class="bg-dark/50 border border-gray-800 rounded-xl overflow-hidden group hover:border-primary/50 transition-all transform hover:-translate-y-2 duration-300">
                    <div class="relative h-48 overflow-hidden">
                        <img src="https://picsum.photos/seed/project5/600/400" alt="生物信息分析工具" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-dark to-transparent"></div>
                        <div class="absolute bottom-4 left-4">
                            <span class="bg-yellow-500/80 text-white text-xs px-2 py-1 rounded-full">Python</span>
                            <span class="bg-red-500/80 text-white text-xs px-2 py-1 rounded-full ml-2">Perl</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-2 group-hover:text-primary transition-colors">生物信息分析工具</h3>
                        <p class="text-gray-400 text-sm mb-4">用于基因组序列分析和蛋白质结构预测的生物信息学工具集，结合了Python和Perl的优势，提供高效的生物数据分析能力。</p>
                        <div class="flex justify-between items-center">
                            <div class="flex items-center gap-2">
                                <span class="text-gray-400 text-sm"><i class="fa fa-star text-yellow-500"></i> 89</span>
                                <span class="text-gray-400 text-sm"><i class="fa fa-code-fork"></i> 28</span>
                            </div>
                            <a href="#" class="text-primary hover:text-primary/80 text-sm flex items-center gap-1">
                                查看详情 <i class="fa fa-arrow-right"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- 项目6 -->
                <div class="bg-dark/50 border border-gray-800 rounded-xl overflow-hidden group hover:border-primary/50 transition-all transform hover:-translate-y-2 duration-300">
                    <div class="relative h-48 overflow-hidden">
                        <img src="https://picsum.photos/seed/project6/600/400" alt="分布式计算框架" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-dark to-transparent"></div>
                        <div class="absolute bottom-4 left-4">
                            <span class="bg-blue-600/80 text-white text-xs px-2 py-1 rounded-full">C++</span>
                            <span class="bg-indigo-500/80 text-white text-xs px-2 py-1 rounded-full ml-2">MPI</span>
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-semibold mb-2 group-hover:text-primary transition-colors">分布式计算框架</h3>
                        <p class="text-gray-400 text-sm mb-4">基于C++和MPI的高性能分布式计算框架，用于解决大规模科学计算问题，支持并行处理和任务调度。</p>
                        <div class="flex justify-between items-center">
                            <div class="flex items-center gap-2">
                                <span class="text-gray-400 text-sm"><i class="fa fa-star text-yellow-500"></i> 73</span>
                                <span class="text-gray-400 text-sm"><i class="fa fa-code-fork"></i> 21</span>
                            </div>
                            <a href="#" class="text-primary hover:text-primary/80 text-sm flex items-center gap-1">
                                查看详情 <i class="fa fa-arrow-right"></i>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-12">
                <a href="#" class="inline-flex items-center gap-2 bg-primary hover:bg-primary/90 text-white px-6 py-3 rounded-lg transition-all transform hover:scale-105">
                    查看更多项目 <i class="fa fa-github"></i>
                </a>
            </div>
        </div>
    </section>

    <!-- 统计数据 -->
    <section id="stats" class="py-20 px-4 relative">
        <div class="absolute -top-20 left-0 w-full h-20 bg-gradient-to-b from-gray-900/50 to-transparent"></div>
        <div class="container mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-[clamp(1.8rem,4vw,3rem)] font-bold mb-4">
                    <span class="text-gradient bg-gradient-to-r from-primary to-secondary">开发统计</span>
                </h2>
                <p class="text-gray-400 max-w-2xl mx-auto">我的代码贡献和项目活跃度</p>
            </div>
            
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                <div class="bg-dark/50 border border-gray-800 rounded-xl p-6">
                    <h3 class="text-xl font-semibold mb-6">语言使用分布</h3>
                    <div class="h-80">
                        <canvas id="languageChart"></canvas>
                    </div>
                </div>
                
                <div class="bg-dark/50 border border-gray-800 rounded-xl p-6">
                    <h3 class="text-xl font-semibold mb-6">代码提交活跃度</h3>
                    <div class="h-80">
                        <canvas id="activityChart"></canvas>
                    </div>
                </div>
                
                <div class="bg-dark/50 border border-gray-800 rounded-xl p-6 lg:col-span-2">
                    <h3 class="text-xl font-semibold mb-6">GitHub 统计卡片</h3>
                    <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
                        <div class="bg-gray-900/50 border border-gray-800 rounded-lg p-6 text-center">
                            <div class="text-4xl font-bold text-primary mb-2" id="repoCount">0</div>
                            <p class="text-gray-400">公开仓库</p>
                        </div>
                        <div class="bg-gray-900/50 border border-gray-800 rounded-lg p-6 text-center">
                            <div class="text-4xl font-bold text-secondary mb-2" id="starCount">0</div>
                            <p class="text-gray-400">获得星标</p>
                        </div>
                        <div class="bg-gray-900/50 border border-gray-800 rounded-lg p-6 text-center">
                            <div class="text-4xl font-bold text-accent mb-2" id="forkCount">0</div>
                            <p class="text-gray-400">被复刻次数</p>
                        </div>
                        <div class="bg-gray-900/50 border border-gray-800 rounded-lg p-6 text-center">
                            <div class="text-4xl font-bold text-green-500 mb-2" id="contribCount">0</div>
                            <p class="text-gray-400">贡献天数</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 联系我 -->
    <section id="contact" class="py-20 px-4 bg-gray-900/50 relative">
        <div class="absolute inset-0 bg-grid opacity-20"></div>
        <div class="absolute -right-10 -bottom-10 w-64 h-64 bg-primary/20 rounded-full blur-3xl"></div>
        <div class="absolute -left-10 top-10 w-64 h-64 bg-accent/20 rounded-full blur-3xl"></div>
        
        <div class="container mx-auto relative z-10">
            <div class="text-center mb-16">
                <h2 class="text-[clamp(1.8rem,4vw,3rem)] font-bold mb-4">
                    <span class="text-gradient bg-gradient-to-r from-primary to-secondary">联系我</span>
                </h2>
                <p class="text-gray-400 max-w-2xl mx-auto">欢迎随时与我交流和合作</p>
            </div>
            
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                <div class="bg-dark/50 border border-gray-800 rounded-xl p-8">
                    <h3 class="text-xl font-semibold mb-6">发送消息</h3>
                    <form class="space-y-6">
                        <div>
                            <label for="name" class="block text-sm font-medium text-gray-300 mb-1">姓名</label>
                            <input type="text" id="name" class="w-full bg-gray-800 border border-gray-700 rounded-lg px-4 py-3 text-white focus:outline-none focus:ring-2 focus:ring-primary/50 focus:border-primary transition-all" placeholder="请输入您的姓名">
                        </div>
                        <div>
                            <label for="email" class="block text-sm font-medium text-gray-300 mb-1">邮箱</label>
                            <input type="email" id="email" class="w-full bg-gray-800 border border-gray-700 rounded-lg px-4 py-3 text-white focus:outline-none focus:ring-2 focus:ring-primary/50 focus:border-primary transition-all" placeholder="请输入您的邮箱">
                        </div>
                        <div>
                            <label for="subject" class="block text-sm font-medium text-gray-300 mb-1">主题</label>
                            <input type="text" id="subject" class="w-full bg-gray-800 border border-gray-700 rounded-lg px-4 py-3 text-white focus:outline-none focus:ring-2 focus:ring-primary/50 focus:border-primary transition-all" placeholder="请输入消息主题">
                        </div>
                        <div>
                            <label for="message" class="block text-sm font-medium text-gray-300 mb-1">消息内容</label>
                            <textarea id="message" rows="4" class="w-full bg-gray-800 border border-gray-700 rounded-lg px-4 py-3 text-white focus:outline-none focus:ring-2 focus:ring-primary/50 focus:border-primary transition-all" placeholder="请输入您的消息内容"></textarea>
                        </div>
                        <button type="submit" class="w-full bg-primary hover:bg-primary/90 text-white px-6 py-3 rounded-lg transition-all transform hover:scale-[1.02] flex items-center justify-center gap-2">
                            <i class="fa fa-paper-plane"></i> 发送消息
                        </button>
                    </form>
                </div>
                
                <div class="flex flex-col justify-between">
                    <div class="bg-dark/50 border border-gray-800 rounded-xl p-8 mb-6">
                        <h3 class="text-xl font-semibold mb-6">联系方式</h3>
                        <div class="space-y-6">
                            <div class="flex items-start gap-4">
                                <div class="w-12 h-12 bg-primary/20 rounded-lg flex items-center justify-center text-primary flex-shrink-0">
                                    <i class="fa fa-envelope"></i>
                                </div>
                                <div>
                                    <h4 class="text-gray-300 font-medium">邮箱</h4>
                                    <p class="text-gray-400">developer@example.com</p>
                                </div>
                            </div>
                            <div class="flex items-start gap-4">
                                <div class="w-12 h-12 bg-secondary/20 rounded-lg flex items-center justify-center text-secondary flex-shrink-0">
                                    <i class="fa fa-github"></i>
                                </div>
                                <div>
                                    <h4 class="text-gray-300 font-medium">GitHub</h4>
                                    <p class="text-gray-400">github.com/devprofile</p>
                                </div>
                            </div>
                            <div class="flex items-start gap-4">
                                <div class="w-12 h-12 bg-accent/20 rounded-lg flex items-center justify-center text-accent flex-shrink-0">
                                    <i class="fa fa-linkedin"></i>
                                </div>
                                <div>
                                    <h4 class="text-gray-300 font-medium">LinkedIn</h4>
                                    <p class="text-gray-400">linkedin.com/in/devprofile</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="bg-dark/50 border border-gray-800 rounded-xl p-8">
                        <h3 class="text-xl font-semibold mb-6">技术咨询</h3>
                        <p class="text-gray-300 mb-6">
                            我提供技术咨询、项目开发和代码审查服务。无论您是需要构建新应用，还是优化现有系统，我都能为您提供专业的技术支持。
                        </p>
                        <div class="flex flex-wrap gap-4">
                            <span class="bg-gray-800 text-gray-300 px-3 py-1 rounded-full text-sm">后端开发</span>
                            <span class="bg-gray-800 text-gray-300 px-3 py-1 rounded-full text-sm">AI与机器学习</span>
                            <span class="bg-gray-800 text-gray-300 px-3 py-1 rounded-full text-sm">微服务架构</span>
                            <span class="bg-gray-800 text-gray-300 px-3 py-1 rounded-full text-sm">性能优化</span>
                            <span class="bg-gray-800 text-gray-300 px-3 py-1 rounded-full text-sm">云原生</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer class="py-12 px-4 bg-dark border-t border-gray-800">
        <div class="container mx-auto">
            <div class="flex flex-col md:flex-row justify-between items-center gap-8">
                <div class="text-center md:text-left">
                    <div class="flex items-center justify-center md:justify-start gap-2 mb-4">
                        <span class="text-2xl text-primary font-bold">Dev<span class="text-accent">Pro</span></span>
                    </div>
                    <p class="text-gray-400 max-w-md">
                        全栈开发者，致力于构建高效、创新的软件解决方案，连接技术与业务价值。
                    </p>
                </div>
                
                <div class="flex gap-4">
                    <a href="#" class="w-10 h-10 bg-gray-800 hover:bg-primary/20 text-gray-400 hover:text-primary rounded-full flex items-center justify-center transition-all">
                        <i class="fa fa-github"></i>
                    </a>
                    <a href="#" class="w-10 h-10 bg-gray-800 hover:bg-primary/20 text-gray-400 hover:text-primary rounded-full flex items-center justify-center transition-all">
                        <i class="fa fa-twitter"></i>
                    </a>
                    <a href="#" class="w-10 h-10 bg-gray-800 hover:bg-primary/20 text-gray-400 hover:text-primary rounded-full flex items-center justify-center transition-all">
                        <i class="fa fa-linkedin"></i>
                    </a>
                    <a href="#" class="w-10 h-10 bg-gray-800 hover:bg-primary/20 text-gray-400 hover:text-primary rounded-full flex items-center justify-center transition-all">
                        <i class="fa fa-stack-overflow"></i>
                    </a>
                </div>
            </div>
            
            <div class="mt-12 pt-8 border-t border-gray-800 text-center text-gray-500 text-sm">
                <p>&copy; 2025 DevPro. 保留所有权利。</p>
            </div>
        </div>
    </footer>

    <!-- 返回顶部按钮 -->
    <button id="back-to-top" class="fixed bottom-8 right-8 bg-primary hover:bg-primary/90 text-white w-12 h-12 rounded-full flex items-center justify-center shadow-lg opacity-0 invisible transition-all z-50">
        <i class="fa fa-arrow-up"></i>
    </button>

    <!-- JavaScript -->
    <script>
        // 导航栏滚动效果
        const navbar = document.getElementById('navbar');
        const backToTop = document.getElementById('back-to-top');
        
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                navbar.classList.add('py-2');
                navbar.classList.remove('py-3');
                navbar.classList.add('shadow-lg');
                
                backToTop.classList.remove('opacity-0');
                backToTop.classList.remove('invisible');
                backToTop.classList.add('opacity-100');
            } else {
                navbar.classList.remove('py-2');
                navbar.classList.add('py-3');
                navbar.classList.remove('shadow-lg');
                
                backToTop.classList.add('opacity-0');
                backToTop.classList.add('invisible');
                backToTop.classList.remove('opacity-100');
            }
        });
        
        // 移动端菜单
        const menuToggle = document.getElementById('menu-toggle');
        const mobileMenu = document.getElementById('mobile-menu');
        
        menuToggle.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });
        
        // 平滑滚动
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // 关闭移动菜单
                    if (!mobileMenu.classList.contains('hidden')) {
                        mobileMenu.classList.add('hidden');
                    }
                }
            });
        });
        
        // 返回顶部按钮
        backToTop.addEventListener('click', () => {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });
        
        // 图表初始化
        window.addEventListener('load', () => {
            // 语言分布图表
            const languageCtx = document.getElementById('languageChart').getContext('2d');
            const languageChart = new Chart(languageCtx, {
                type: 'doughnut',
                data: {
                    labels: ['Python', 'Java', 'Go', 'C++', 'Vue.js', 'Perl', '其他'],
                    datasets: [{
                        data: [35, 25, 15, 10, 8, 5, 2],
                        backgroundColor: [
                            '#FFD700', // Python
                            '#5B82A4', // Java
                            '#00ADD8', // Go
                            '#00599C', // C++
                            '#41B883', // Vue.js
                            '#39457E', // Perl
                            '#6B7280'  // 其他
                        ],
                        borderWidth: 0,
                        hoverOffset: 15
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            position: 'right',
                            labels: {
                                color: '#F8FAFC',
                                font: {
                                    family: 'Inter',
                                    size: 12
                                },
                                padding: 20
                            }
                        }
                    },
                    cutout: '65%'
                }
            });
            
            // 活跃度图表
            const activityCtx = document.getElementById('activityChart').getContext('2d');
            const activityChart = new Chart(activityCtx, {
                type: 'line',
                data: {
                    labels: ['一月', '二月', '三月', '四月', '五月', '六月', '七月', '八月', '九月', '十月', '十一月', '十二月'],
                    datasets: [{
                        label: '代码提交',
                        data: [42, 58, 65, 45, 78, 92, 85, 105, 90, 110, 125, 140],
                        backgroundColor: 'rgba(99, 102, 241, 0.2)',
                        borderColor: '#6366F1',
                        borderWidth: 2,
                        tension: 0.3,
                        fill: true
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    scales: {
                        y: {
                            beginAtZero: true,
                            grid: {
                                color: 'rgba(255, 255, 255, 0.05)'
                            },
                            ticks: {
                                color: '#94A3B8'
                            }
                        },
                        x: {
                            grid: {
                                display: false
                            },
                            ticks: {
                                color: '#94A3B8'
                            }
                        }
                    },
                    plugins: {
                        legend: {
                            display: false
                        }
                    }
                }
            });
            
            // 统计数据动画
            function animateValue(id, start, end, duration) {
                const obj = document.getElementById(id);
                let startTimestamp = null;
                const step = (timestamp) => {
                    if (!startTimestamp) startTimestamp = timestamp;
                    const progress = Math.min((timestamp - startTimestamp) / duration, 1);
                    obj.innerHTML = Math.floor(progress * (end - start) + start);
                    if (progress < 1) {
                        window.requestAnimationFrame(step);
                    }
                };
                window.requestAnimationFrame(step);
            }
            
            // 当元素进入视口时执行动画
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        animateValue('repoCount', 0, 42, 2000);
                        animateValue('starCount', 0, 1245, 2000);
                        animateValue('forkCount', 0, 538, 2000);
                        animateValue('contribCount', 0, 189, 2000);
                        observer.unobserve(entry.target);
                    }
                });
            }, { threshold: 0.5 });
            
            const statsSection = document.getElementById('stats');
            if (statsSection) {
                observer.observe(statsSection);
            }
        });
    </script>
</body>
</html>
    
