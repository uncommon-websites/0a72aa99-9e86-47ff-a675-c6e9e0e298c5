<script lang="ts">
    export let title: string;
    export let description: string;
    export let image: string;
    export let icon: string;

    // Extract the bold part of the description (first sentence)
    $: splitDesc = description.split('. ');
    $: boldDesc = splitDesc[0] + '.';
    $: restDesc = splitDesc.slice(1).join('. ');
</script>

<div class="bg-[#F3F4F6] rounded-3xl p-8 md:p-12 transition-all hover:bg-gray-200 group">
    <!-- Header -->
    <div class="flex items-center gap-3 mb-8">
        <div class="text-blue-600">
            {#if icon === 'lock'}
                <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="11" width="18" height="11" rx="2" ry="2"></rect><path d="M7 11V7a5 5 0 0 1 10 0v4"></path></svg>
            {:else if icon === 'connect'}
                <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"></path><circle cx="9" cy="7" r="4"></circle><path d="M23 21v-2a4 4 0 0 0-3-3.87"></path><path d="M16 3.13a4 4 0 0 1 0 7.75"></path></svg>
            {:else if icon === 'data'}
                <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"></path><polyline points="3.27 6.96 12 12.01 20.73 6.96"></polyline><line x1="12" y1="22.08" x2="12" y2="12"></line></svg>
            {:else if icon === 'lab'}
                <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M6 14h12l-3.9-6.8a2 2 0 0 0-3.5 0L6 14z"></path><path d="M2 22h20"></path><path d="M10 14v4"></path><path d="M14 14v4"></path></svg>
            {:else if icon === 'preview'}
                <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"></circle><line x1="21" y1="21" x2="16.65" y2="16.65"></line></svg>
            {:else if icon === 'guard'}
                <svg class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"></path></svg>
            {/if}
        </div>
        <h3 class="text-xl font-semibold text-gray-900">{title}</h3>
    </div>

    <!-- Image Placeholder / Abstract UI -->
    <div class="bg-white rounded-xl shadow-sm border border-gray-200 overflow-hidden mb-8 aspect-[16/9] relative group-hover:shadow-md transition-shadow">
        {#if image === 'collateral'}
            <!-- Invoice Audit UI -->
            <div class="p-6 h-full flex flex-col">
                <div class="flex justify-between items-center mb-6 border-b border-gray-100 pb-4">
                    <div class="font-bold text-gray-800">Invoice Audit</div>
                    <div class="flex gap-2">
                        <div class="px-3 py-1 bg-red-50 text-red-600 text-xs font-semibold rounded">3 Disputed</div>
                    </div>
                </div>
                <div class="space-y-3">
                    <div class="flex justify-between text-xs text-gray-400 uppercase tracking-wider">
                        <span>Charge Type</span>
                        <span>Amount</span>
                        <span>Status</span>
                    </div>
                    <div class="flex justify-between items-center py-2 border-b border-gray-50">
                        <div class="text-xs text-gray-600">Detention Fee</div>
                        <div class="text-xs font-semibold text-gray-900">$2,850</div>
                        <div class="px-2 py-1 bg-red-100 text-red-600 rounded-full text-[10px] font-semibold">Invalid</div>
                    </div>
                    <div class="flex justify-between items-center py-2 border-b border-gray-50">
                        <div class="text-xs text-gray-600">Demurrage</div>
                        <div class="text-xs font-semibold text-gray-900">$1,200</div>
                        <div class="px-2 py-1 bg-green-100 text-green-600 rounded-full text-[10px] font-semibold">Valid</div>
                    </div>
                    <div class="flex justify-between items-center py-2 border-b border-gray-50">
                        <div class="text-xs text-gray-600">Per Diem</div>
                        <div class="text-xs font-semibold text-gray-900">$450</div>
                        <div class="px-2 py-1 bg-red-100 text-red-600 rounded-full text-[10px] font-semibold">Disputed</div>
                    </div>
                </div>
            </div>
        {:else if image === 'connect'}
            <!-- Container Tracking UI -->
            <div class="p-6 h-full flex flex-col bg-gray-50">
                <div class="bg-white p-4 rounded-lg shadow-sm border border-gray-200 mb-3">
                    <div class="flex items-center gap-3 mb-3">
                        <div class="w-8 h-8 rounded-full bg-blue-100 flex items-center justify-center text-blue-600">
                            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20 7l-8-4-8 4m16 0l-8 4m8-4v10l-8 4m0-10L4 7m8 4v10M4 7v10l8 4"></path></svg>
                        </div>
                        <div>
                            <div class="text-xs font-semibold text-gray-900">MSCU8234567</div>
                            <div class="text-[10px] text-gray-500">LA/LB Port Terminal 2</div>
                        </div>
                    </div>
                    <div class="flex gap-2 text-[10px]">
                        <div class="px-2 py-1 bg-green-50 text-green-600 rounded font-semibold">Available</div>
                        <div class="px-2 py-1 bg-gray-100 text-gray-600 rounded">Last Free: Dec 18</div>
                    </div>
                </div>
                <div class="bg-white p-4 rounded-lg shadow-sm border border-gray-200">
                    <div class="flex items-center gap-3">
                        <div class="w-8 h-8 rounded-full bg-purple-100 flex items-center justify-center text-purple-600">
                            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20 7l-8-4-8 4m16 0l-8 4m8-4v10l-8 4m0-10L4 7m8 4v10M4 7v10l8 4"></path></svg>
                        </div>
                        <div>
                            <div class="text-xs font-semibold text-gray-900">TEMU9876543</div>
                            <div class="text-[10px] text-gray-500">NY/NJ Port Terminal 5</div>
                        </div>
                    </div>
                </div>
            </div>
        {:else if image === 'data'}
            <!-- Terminal Data UI -->
            <div class="p-6 h-full flex flex-col">
                <div class="flex gap-4 mb-6">
                    <div class="w-1/2 p-4 bg-gray-50 rounded-lg border border-gray-100">
                        <div class="text-xs text-gray-400 mb-1">Terminals Connected</div>
                        <div class="text-xl font-bold text-gray-900">230+</div>
                        <div class="mt-4 h-16 flex items-end gap-1">
                            {#each [40, 60, 30, 70, 50, 80] as h}
                                <div class="w-full bg-blue-200 rounded-t" style="height: {h}%"></div>
                            {/each}
                        </div>
                    </div>
                    <div class="w-1/2 p-4 bg-gray-50 rounded-lg border border-gray-100">
                        <div class="text-xs text-gray-400 mb-1">Container Events Tracked</div>
                        <div class="text-xl font-bold text-gray-900">15M+</div>
                         <div class="mt-4 h-2 bg-gray-200 rounded-full overflow-hidden">
                            <div class="h-full bg-blue-500 w-2/3"></div>
                        </div>
                    </div>
                </div>
            </div>
        {:else if image === 'lab'}
            <!-- Dispute Management UI -->
            <div class="p-6 h-full bg-white">
                <div class="font-mono text-xs text-gray-400 mb-4">Dispute Timeline</div>
                <div class="space-y-4 relative pl-4 border-l border-gray-200">
                    <div class="relative">
                        <div class="absolute -left-[21px] top-1 w-3 h-3 rounded-full bg-green-500 border-2 border-white"></div>
                        <div class="text-xs font-medium text-gray-900">Invoice #DET-2847 Disputed</div>
                        <div class="mt-1 text-xs text-gray-500 pl-2 border-l border-gray-100 ml-1">AI detected invalid detention charge</div>
                    </div>
                     <div class="relative">
                        <div class="absolute -left-[21px] top-1 w-3 h-3 rounded-full bg-green-500 border-2 border-white"></div>
                        <div class="text-xs font-medium text-gray-900">Evidence Compiled</div>
                         <div class="mt-1 text-xs text-gray-500 pl-2 border-l border-gray-100 ml-1">Timestamped terminal data attached</div>
                    </div>
                     <div class="relative">
                        <div class="absolute -left-[21px] top-1 w-3 h-3 rounded-full bg-blue-400 border-2 border-white"></div>
                        <div class="text-xs font-medium text-gray-900">Dispute Submitted</div>
                         <div class="mt-1 text-xs text-gray-500 pl-2 border-l border-gray-100 ml-1">Awaiting carrier response</div>
                    </div>
                </div>
            </div>
        {:else if image === 'preview'}
            <!-- Cost Analytics UI -->
            <div class="p-6 h-full">
                <table class="w-full text-xs">
                    <thead>
                        <tr class="text-gray-400 border-b border-gray-100">
                            <th class="text-left pb-2 font-normal">Metric</th>
                            <th class="text-right pb-2 font-normal">This Month</th>
                            <th class="text-right pb-2 font-normal">Forecast</th>
                        </tr>
                    </thead>
                    <tbody class="text-gray-600">
                        <tr class="border-b border-gray-50">
                            <td class="py-2">Per Diem Fees</td>
                            <td class="py-2 text-right text-red-500">$45,200</td>
                            <td class="py-2 text-right text-green-500">$12,800</td>
                        </tr>
                         <tr class="border-b border-gray-50">
                            <td class="py-2">Disputed Charges</td>
                            <td class="py-2 text-right">$28,500</td>
                            <td class="py-2 text-right">$32,000</td>
                        </tr>
                         <tr>
                            <td class="py-2">Total Savings</td>
                            <td class="py-2 text-right font-semibold text-green-600">$142,000</td>
                            <td class="py-2 text-right font-semibold text-green-600">$156,000</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        {:else if image === 'guard'}
            <!-- Port Coverage UI -->
            <div class="p-6 h-full flex flex-col justify-center">
                <div class="text-xs text-gray-400 mb-2">Real-Time Port Data</div>
                <div class="grid grid-cols-2 gap-4">
                    <div class="p-3 bg-blue-50 rounded border border-blue-100">
                        <div class="text-[10px] text-blue-600 uppercase">LA/LB Port</div>
                        <div class="text-sm font-bold text-blue-700">Connected</div>
                    </div>
                    <div class="p-3 bg-blue-50 rounded border border-blue-100">
                        <div class="text-[10px] text-blue-600 uppercase">NY/NJ Port</div>
                        <div class="text-sm font-bold text-blue-700">Connected</div>
                    </div>
                </div>
                <div class="grid grid-cols-2 gap-4 mt-4">
                    <div>
                        <div class="text-[10px] text-gray-400 uppercase">Terminals</div>
                        <div class="text-lg font-bold">230+</div>
                    </div>
                     <div>
                        <div class="text-[10px] text-gray-400 uppercase">Steamship Lines</div>
                        <div class="text-lg font-bold">23</div>
                    </div>
                </div>
            </div>
        {/if}
    </div>

    <!-- Footer -->
    <div class="flex items-end justify-between gap-4">
        <div class="max-w-xl">
            <p class="text-gray-900 text-lg leading-relaxed">
                <span class="font-bold">{boldDesc}</span> <span class="text-gray-600">{restDesc}</span>
            </p>
        </div>
        <button class="w-10 h-10 rounded-full border border-gray-300 flex items-center justify-center text-gray-600 hover:bg-black hover:text-white hover:border-black transition-colors flex-shrink-0">
            <svg class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <line x1="7" y1="17" x2="17" y2="7"></line>
                <polyline points="7 7 17 7 17 17"></polyline>
            </svg>
        </button>
    </div>
</div>
