<script>
    import Navbar from '$lib/components/Navbar.svelte';
    import Footer from '$lib/components/Footer.svelte';
    import FeatureRow from '$lib/components/FeatureRow.svelte';
</script>

<div class="bg-[var(--color-bluecargo-dark)] min-h-screen flex flex-col">
    <Navbar />

    <main class="flex-grow">
        <!-- Hero Section -->
        <section class="relative pt-32 pb-20 overflow-hidden">
            <div class="container mx-auto px-6 relative z-10">
                <div class="max-w-4xl mx-auto text-center">
                    <!-- Search/Notification Pill -->
                    <div class="inline-flex items-center gap-2 bg-white/10 backdrop-blur-sm border border-white/10 rounded-full px-4 py-1.5 mb-8">
                        <span class="w-2 h-2 rounded-full bg-[var(--color-bluecargo-primary)]"></span>
                        <span class="text-white text-sm font-medium">AI-Powered Auditing</span>
                        <span class="text-gray-400 text-sm">Save millions on freight costs</span>
                        <svg class="w-4 h-4 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg>
                    </div>

                    <h1 class="text-5xl md:text-7xl font-bold text-white tracking-tight mb-6 text-balance">
                        Stop overpaying on freight invoices.
                    </h1>
                    
                    <p class="text-lg md:text-xl text-gray-400 mb-10 max-w-2xl mx-auto leading-relaxed text-balance">
                        AI-powered freight invoice auditing validated against real-time port and terminal data. Automatically catch unverified accessorial charges and recover millions in wrongful detention and demurrage fees.
                    </p>
                    
                    <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
                        <button class="bg-white hover:bg-gray-100 text-black px-6 py-3 rounded-full font-medium transition-colors flex items-center gap-2">
                            Start Free Trial
                            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                                <path d="M5 12h14M12 5l7 7-7 7"/>
                            </svg>
                        </button>
                        <button class="bg-transparent border border-white/20 hover:bg-white/10 text-white px-6 py-3 rounded-full font-medium transition-colors flex items-center gap-2">
                            See How It Works
                            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                                <path d="M5 12h14M12 5l7 7-7 7"/>
                            </svg>
                        </button>
                    </div>
                </div>
            </div>

            <!-- Hero Images/Cards -->
            <div class="mt-20 relative">
                <div class="flex justify-center gap-6 overflow-hidden px-6">
                    <!-- Card 1 - Invoice Audit -->
                    <div class="w-[350px] md:w-[450px] flex-shrink-0 rounded-xl overflow-hidden shadow-2xl border border-white/10 transform -rotate-2 mt-8">
                        <div class="bg-white p-4">
                            <div class="flex items-center justify-between mb-4">
                                <div class="text-xs font-semibold text-gray-500">INVOICE #DET-2847</div>
                                <div class="h-8 px-3 bg-red-50 rounded text-red-600 text-xs flex items-center justify-center font-bold">DISPUTED</div>
                            </div>
                            <div class="space-y-3">
                                <div class="p-3 bg-gray-50 rounded-lg">
                                    <div class="text-xs text-gray-500 mb-1">Detention Charge</div>
                                    <div class="text-lg font-bold text-gray-900">$2,850.00</div>
                                </div>
                                <div class="flex justify-between text-xs">
                                    <span class="text-gray-500">Container: MSCU8234567</span>
                                    <span class="text-red-600 font-semibold">Invalid charge</span>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Card 2 (Center) - Container Tracking -->
                    <div class="w-[350px] md:w-[450px] flex-shrink-0 rounded-xl overflow-hidden shadow-2xl border border-white/10 z-10">
                        <div class="bg-white h-full flex flex-col">
                            <div class="bg-[var(--color-bluecargo-primary)] p-6">
                                <div class="flex justify-between items-center">
                                    <div class="text-white font-semibold">Container Tracking</div>
                                    <div class="h-8 w-8 bg-white/20 rounded-full flex items-center justify-center">
                                        <svg class="w-4 h-4 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg>
                                    </div>
                                </div>
                            </div>
                            <div class="p-6 flex-grow">
                                <div class="space-y-4">
                                    <div class="flex items-center gap-3">
                                        <div class="w-8 h-8 rounded-full bg-green-100 flex items-center justify-center">
                                            <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path></svg>
                                        </div>
                                        <div class="flex-grow">
                                            <div class="text-sm font-medium text-gray-900">Available for pickup</div>
                                            <div class="text-xs text-gray-500">LA/LB Port - Terminal 2</div>
                                        </div>
                                    </div>
                                    <div class="text-xs text-gray-400 space-y-1">
                                        <div class="flex justify-between"><span>Last Free Day:</span><span class="font-medium text-gray-600">Dec 18, 2024</span></div>
                                        <div class="flex justify-between"><span>Per Diem Rate:</span><span class="font-medium text-gray-600">$150/day</span></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Card 3 - Savings Report -->
                    <div class="w-[350px] md:w-[450px] flex-shrink-0 rounded-xl overflow-hidden shadow-2xl border border-white/10 transform rotate-2 mt-8">
                        <div class="bg-white p-4">
                            <div class="flex items-center justify-between mb-4">
                                <div class="text-xs font-semibold text-gray-500">MONTHLY SAVINGS</div>
                                <div class="h-8 px-3 bg-green-50 rounded text-green-600 text-xs flex items-center justify-center font-bold">+$142K</div>
                            </div>
                            <div class="space-y-3">
                                <div class="p-3 bg-gray-50 rounded-lg">
                                    <div class="text-xs text-gray-500 mb-2">Recovered Charges</div>
                                    <div class="flex items-end gap-1 h-16">
                                        <div class="w-full bg-green-200 rounded-t" style="height: 45%"></div>
                                        <div class="w-full bg-green-300 rounded-t" style="height: 60%"></div>
                                        <div class="w-full bg-green-400 rounded-t" style="height: 75%"></div>
                                        <div class="w-full bg-green-500 rounded-t" style="height: 90%"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Logos Section -->
        <section class="py-12 border-y border-white/5 bg-black/20">
            <div class="container mx-auto px-6">
                <p class="text-center text-gray-500 text-sm mb-8">Trusted by leading supply chain teams</p>
                <div class="flex flex-wrap justify-center items-center gap-12 md:gap-20 opacity-60">
                    <div class="text-white font-bold text-xl tracking-tight">GE Appliances</div>
                    <div class="text-white font-bold text-xl tracking-tight">IMC</div>
                    <div class="text-white font-bold text-xl tracking-tight">Forrest Logistics</div>
                    <div class="text-white font-bold text-xl tracking-tight">STG Logistics</div>
                </div>
            </div>
        </section>

        <!-- BlueCargo Core Section -->
        <section class="py-32 relative overflow-hidden">
            <div class="container mx-auto px-6 relative z-10">
                <div class="text-center mb-24">
                    <h2 class="text-[var(--color-bluecargo-primary)] font-mono text-xs tracking-[0.2em] uppercase mb-6">Real-Time Port Data</h2>
                    <h3 class="text-4xl md:text-6xl font-bold text-white mb-2 tracking-tight">AI-powered freight auditing.</h3>
                    <h3 class="text-4xl md:text-6xl font-bold text-gray-600 tracking-tight">Backed by terminal data.</h3>
                </div>

                <div class="grid md:grid-cols-2 gap-16 items-center max-w-6xl mx-auto">
                    <!-- Data Visualization Card -->
                    <div class="bg-gradient-to-br from-[#7C3AED] to-[#4C1D95] rounded-3xl p-12 aspect-[4/3] relative overflow-hidden flex items-center justify-center shadow-2xl">
                        <!-- Abstract UI Elements -->
                        <div class="relative z-10 w-full max-w-[320px]">
                            <!-- Container Status Card -->
                            <div class="bg-white/10 backdrop-blur-xl border border-white/20 rounded-2xl p-6 mb-8 shadow-xl relative overflow-hidden group hover:scale-105 transition-transform duration-500">
                                <div class="space-y-4 relative z-10">
                                    <div class="flex items-center justify-between">
                                        <div class="text-white/60 text-xs uppercase tracking-wider font-medium">Container Status</div>
                                        <div class="px-2 py-1 bg-green-500/20 rounded text-green-300 text-xs font-semibold">Available</div>
                                    </div>
                                    <div class="text-white font-mono text-xl tracking-wider">MSCU8234567</div>
                                    <div class="pt-3 border-t border-white/10 space-y-2">
                                        <div class="flex justify-between text-xs">
                                            <span class="text-white/60">Terminal:</span>
                                            <span class="text-white font-medium">LA/LB Port</span>
                                        </div>
                                        <div class="flex justify-between text-xs">
                                            <span class="text-white/60">Last Free Day:</span>
                                            <span class="text-white font-medium">Dec 18</span>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            
                            <!-- Floating Pills -->
                            <div class="relative">
                                <div class="absolute -left-4 top-0 bg-white text-black px-5 py-2.5 rounded-full text-sm font-semibold shadow-lg flex items-center gap-2 transform -rotate-2">
                                    <div class="w-5 h-5 rounded-full bg-blue-100 flex items-center justify-center text-blue-600">
                                        <svg class="w-3 h-3" fill="currentColor" viewBox="0 0 20 20"><path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"/><path fill-rule="evenodd" d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd"/></svg>
                                    </div>
                                    Invoice Auditing
                                </div>
                                <div class="absolute -right-4 top-12 bg-white/10 backdrop-blur-md text-white px-5 py-2.5 rounded-full text-sm font-semibold border border-white/20 flex items-center gap-2 transform rotate-2">
                                    <div class="w-5 h-5 rounded-full bg-purple-500/30 flex items-center justify-center text-purple-200">
                                        <svg class="w-3 h-3" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M6 2a1 1 0 00-1 1v1H4a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V6a2 2 0 00-2-2h-1V3a1 1 0 10-2 0v1H7V3a1 1 0 00-1-1zm0 5a1 1 0 000 2h8a1 1 0 100-2H6z" clip-rule="evenodd"/></svg>
                                    </div>
                                    D&D Tracking
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Text Content -->
                    <div class="space-y-8">
                        <h3 class="text-4xl md:text-5xl font-bold text-white tracking-tight">Stop the port data black box.</h3>
                        <p class="text-gray-400 text-lg leading-relaxed max-w-lg">
                            90% of traded goods flow through ports, yet they remain the biggest bottleneck in supply chains. BlueCargo connects to 230+ terminals and validates every charge with timestamped documentation.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- White Section -->
        <div class="bg-[#F9FAFB] text-black rounded-t-[4rem] relative z-20 mt-[-2rem] pt-32 pb-32">
            <div class="container mx-auto px-6">
                <!-- Header -->
                <div class="max-w-4xl mb-24">
                    <div class="flex items-center gap-4 mb-6">
                        <div class="h-px w-12 bg-gray-300"></div>
                        <span class="text-gray-500 font-mono text-xs tracking-[0.2em] uppercase">Platform Features</span>
                    </div>
                    <h2 class="text-4xl md:text-6xl font-bold text-gray-900 mb-2 tracking-tight">Everything you need to control freight costs.</h2>
                    <h2 class="text-4xl md:text-6xl font-bold text-gray-400 tracking-tight mb-8">From audit to recovery.</h2>
                    
                    <a href="#" class="inline-flex items-center gap-2 text-sm font-semibold border-b border-black pb-0.5 hover:text-gray-600 transition-colors">
                        Explore our platform
                        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M5 12h14M12 5l7 7-7 7"/>
                        </svg>
                    </a>
                </div>

                <!-- Features Grid -->
                <div class="flex flex-col lg:flex-row gap-12">
                    <!-- Sidebar Navigation (Sticky) -->
                    <div class="hidden lg:block w-64 flex-shrink-0">
                        <div class="sticky top-32 space-y-4">
                            <div class="flex items-center gap-2 text-sm font-semibold text-black border-l-2 border-black pl-4 py-1">
                                <span class="w-1.5 h-1.5 rounded-full bg-[var(--color-bluecargo-primary)]"></span>
                                AI Invoice Auditing
                            </div>
                            <a href="#" class="block text-sm text-gray-500 pl-4 py-1 hover:text-black border-l-2 border-transparent hover:border-gray-200 transition-colors">Container Tracking</a>
                            <a href="#" class="block text-sm text-gray-500 pl-4 py-1 hover:text-black border-l-2 border-transparent hover:border-gray-200 transition-colors">Terminal Data</a>
                            <a href="#" class="block text-sm text-gray-500 pl-4 py-1 hover:text-black border-l-2 border-transparent hover:border-gray-200 transition-colors">Dispute Management</a>
                            <a href="#" class="block text-sm text-gray-500 pl-4 py-1 hover:text-black border-l-2 border-transparent hover:border-gray-200 transition-colors">Cost Analytics</a>
                            <a href="#" class="block text-sm text-gray-500 pl-4 py-1 hover:text-black border-l-2 border-transparent hover:border-gray-200 transition-colors">Port Coverage</a>
                        </div>
                    </div>

                    <!-- Feature Cards -->
                    <div class="flex-grow space-y-8">
                        <FeatureRow 
                            title="AI Invoice Auditing" 
                            description="Automate freight invoice validation. BlueCargo's AI validates every charge against real-time port and terminal data, catching unverified accessorial fees before you pay."
                            icon="lock"
                            image="collateral"
                        />
                         <FeatureRow 
                            title="Container Tracking" 
                            description="Monitor every container in real-time. Track 15M+ container events across 230+ terminals with live updates on availability, appointments, and last free days."
                            icon="connect"
                            image="connect"
                        />
                         <FeatureRow 
                            title="Terminal Data Integration" 
                            description="Access the industry's most reliable port data. Our proprietary algorithms showcase only the most accurate data points from 67 port terminals and 23 steamship lines."
                            icon="data"
                            image="data"
                        />
                         <FeatureRow 
                            title="Dispute Management" 
                            description="Recover wrongful charges automatically. 95% dispute success rate with timestamped documentation and 2 years of backup data for evidence-backed claims."
                            icon="lab"
                            image="lab"
                        />
                         <FeatureRow 
                            title="Cost Analytics" 
                            description="Predict and prevent detention fees. Predictive analytics forecast cost trends and identify patterns, helping you avoid $175M+ in per diem fees annually."
                            icon="preview"
                            image="preview"
                        />
                         <FeatureRow 
                            title="Port Coverage" 
                            description="Complete visibility across all major US ports. Operations in LA/LB, NY/NJ, and all major US ports with connections to 230+ terminals and rail ramps."
                            icon="guard"
                            image="guard"
                        />
                    </div>
                </div>

                <!-- Value Prop Section -->
                <div class="mt-32 text-center max-w-4xl mx-auto mb-24">
                    <div class="w-24 h-24 mx-auto bg-gradient-to-br from-blue-100 to-purple-100 rounded-full flex items-center justify-center mb-8 relative">
                        <div class="absolute inset-0 bg-white/50 blur-xl rounded-full"></div>
                        <svg class="w-10 h-10 text-blue-600 relative z-10" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path></svg>
                    </div>
                    <h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8 leading-tight">
                        Built for supply chain managers at importers who need freight cost control but lose millions to unverified charges.
                    </h2>
                    <button class="bg-white border border-gray-200 hover:border-gray-400 text-black px-6 py-3 rounded-full font-medium transition-colors flex items-center gap-2 mx-auto">
                        See customer stories
                        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M5 12h14M12 5l7 7-7 7"/>
                        </svg>
                    </button>
                </div>

                <!-- Trusted By Section -->
                <div class="mb-32">
                    <p class="text-xl text-gray-500 mb-12">Trusted by leading supply chain teams. See how they save millions.</p>
                    
                    <div class="grid md:grid-cols-3 gap-6">
                        <!-- GE Appliances Card (Large) -->
                        <div class="md:col-span-2 bg-[#0A0A0A] rounded-3xl p-10 relative overflow-hidden group min-h-[400px] flex flex-col justify-end">
                            <div class="absolute inset-0 bg-gradient-to-t from-black via-black/50 to-transparent"></div>
                            
                            <div class="relative z-10">
                                <div class="flex items-center gap-4 mb-6">
                                    <div class="text-white font-bold text-2xl tracking-tight">GE Appliances</div>
                                    <div class="w-8 h-8 rounded-full bg-[var(--color-bluecargo-primary)] flex items-center justify-center text-white font-bold">✓</div>
                                </div>
                                <h3 class="text-3xl font-bold text-white mb-4 max-w-md">
                                    "BlueCargo saved us <span class="text-[var(--color-bluecargo-primary)]">$1.6M annually</span> in unverified accessorial fees"
                                </h3>
                                <p class="text-gray-400 text-sm mb-4">— Jordan Glastein, Senior Manager, Ocean Logistics and Strategy</p>
                                <div class="w-10 h-10 rounded-full bg-white/10 backdrop-blur-md border border-white/20 flex items-center justify-center text-white group-hover:bg-white group-hover:text-black transition-colors">
                                    <svg class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg>
                                </div>
                            </div>
                        </div>

                        <!-- Smaller Cards -->
                        <div class="space-y-6">
                            <!-- Card 2 - Forrest Logistics -->
                            <div class="bg-[#0A0A0A] rounded-3xl p-8 relative overflow-hidden group h-[240px] flex flex-col justify-between">
                                <div class="absolute inset-0 bg-gradient-to-br from-blue-900/40 to-black"></div>
                                <div class="relative z-10">
                                    <div class="text-white font-bold text-lg mb-2">Forrest Logistics</div>
                                    <p class="text-gray-400 text-sm">"Recovered $5.2M in wrongful detention and demurrage charges"</p>
                                </div>
                                <div class="relative z-10 flex justify-end">
                                    <div class="w-10 h-10 rounded-full bg-white/10 backdrop-blur-md border border-white/20 flex items-center justify-center text-white group-hover:bg-white group-hover:text-black transition-colors">
                                        <svg class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg>
                                    </div>
                                </div>
                            </div>
                            <!-- Card 3 - STG Logistics -->
                            <div class="bg-[#0A0A0A] rounded-3xl p-8 relative overflow-hidden group h-[240px] flex flex-col justify-between">
                                <div class="absolute inset-0 bg-gradient-to-br from-green-900/40 to-black"></div>
                                <div class="relative z-10">
                                    <div class="text-white font-bold text-lg mb-2">STG Logistics</div>
                                    <p class="text-gray-400 text-sm">"A game changer for our drayage business"</p>
                                    <p class="text-gray-500 text-xs mt-2">— Mark Darling, SVP</p>
                                </div>
                                <div class="relative z-10 flex justify-end">
                                    <div class="w-10 h-10 rounded-full bg-white/10 backdrop-blur-md border border-white/20 flex items-center justify-center text-white group-hover:bg-white group-hover:text-black transition-colors">
                                        <svg class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Banner -->
                <div class="bg-[#0A0A0A] rounded-3xl p-12 md:p-20 relative overflow-hidden mb-32 text-center">
                    <div class="absolute inset-0 bg-[url('/grid-pattern.svg')] opacity-10"></div>
                    <div class="absolute left-0 top-0 w-64 h-64 bg-purple-500/10 blur-[100px] rounded-full"></div>
                    <div class="absolute right-0 bottom-0 w-64 h-64 bg-blue-500/10 blur-[100px] rounded-full"></div>
                    
                    <div class="relative z-10 max-w-3xl mx-auto">
                        <h2 class="text-4xl md:text-6xl font-bold text-white mb-6 tracking-tight">
                            Automate freight auditing. <span class="text-[var(--color-bluecargo-primary)]">Save millions.</span>
                        </h2>
                        <p class="text-gray-400 mb-10">
                            Connect to 230+ terminals and 23 steamship lines. Our API integrates seamlessly with your AP systems for 99% invoice automation.
                        </p>
                        <div class="inline-flex items-center gap-2 bg-white/10 backdrop-blur-md border border-white/10 rounded-full px-4 py-2 text-white text-sm hover:bg-white/20 transition-colors cursor-pointer">
                            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"></path></svg>
                            API Documentation
                            <kbd class="bg-black/30 px-1.5 py-0.5 rounded text-xs text-gray-400 font-mono">→</kbd>
                        </div>
                    </div>
                </div>

                <!-- Integrations -->
                <div class="text-center mb-32">
                    <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">
                        Terminals. Steamship lines. Rail ramps.<br>
                        <span class="text-gray-400">All major US ports.<br>BlueCargo connects to them all.</span>
                    </h2>
                    <button class="bg-gray-100 hover:bg-gray-200 text-black px-6 py-2 rounded-full text-sm font-medium transition-colors flex items-center gap-2 mx-auto mb-16 mt-8">
                        View all port coverage
                        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M5 12h14M12 5l7 7-7 7"/>
                        </svg>
                    </button>

                    <div class="grid grid-cols-2 md:grid-cols-4 gap-px bg-gray-200 border border-gray-200 rounded-2xl overflow-hidden">
                        {#each ['LA/LB Port', 'NY/NJ Port', 'Maersk', 'MSC', 'CMA CGM', 'Hapag-Lloyd', 'ONE', 'Evergreen'] as logo}
                        <div class="bg-[#F9FAFB] p-12 flex items-center justify-center grayscale opacity-60 hover:grayscale-0 hover:opacity-100 transition-all duration-300">
                            <span class="font-bold text-lg uppercase tracking-wider">{logo}</span>
                        </div>
                        {/each}
                    </div>
                </div>

                <!-- Blog Section -->
                <div class="mb-12">
                    <h2 class="text-4xl font-bold text-gray-900 mb-12">Learn more about freight cost optimization.</h2>
                    <div class="grid md:grid-cols-2 gap-8">
                        <!-- Post 1 -->
                        <div class="group cursor-pointer">
                            <div class="bg-gradient-to-br from-gray-200 to-gray-300 rounded-3xl aspect-[16/9] mb-6 relative overflow-hidden">
                                <div class="absolute inset-0 flex items-center justify-center">
                                    <div class="grid grid-cols-6 gap-4 opacity-50">
                                        {#each Array(24) as _}
                                            <svg class="w-6 h-6 text-blue-600 transform -rotate-45" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20 7l-8-4-8 4m16 0l-8 4m8-4v10l-8 4m0-10L4 7m8 4v10M4 7v10l8 4"></path></svg>
                                        {/each}
                                    </div>
                                </div>
                            </div>
                            <div class="text-xs font-bold text-gray-500 uppercase tracking-wider mb-2">Supply Chain Insights</div>
                            <h3 class="text-2xl font-bold text-gray-900 group-hover:text-blue-600 transition-colors">How ports became the biggest black box in supply chains</h3>
                        </div>
                        <!-- Post 2 -->
                        <div class="group cursor-pointer">
                            <div class="bg-gray-100 rounded-3xl aspect-[16/9] mb-6 relative overflow-hidden flex items-center justify-center">
                                <div class="flex gap-4">
                                    <div class="w-16 h-16 rounded-full bg-green-400 blur-xl opacity-80"></div>
                                    <div class="w-20 h-20 rounded-full bg-blue-400 blur-xl opacity-80"></div>
                                    <div class="w-12 h-12 rounded-full bg-purple-400 blur-xl opacity-80"></div>
                                </div>
                            </div>
                            <div class="text-xs font-bold text-gray-500 uppercase tracking-wider mb-2">Best Practices</div>
                            <h3 class="text-2xl font-bold text-gray-900 group-hover:text-blue-600 transition-colors">Understanding detention and demurrage: A complete guide</h3>
                        </div>
                    </div>
                </div>


    </main>

    <Footer />
</div>

