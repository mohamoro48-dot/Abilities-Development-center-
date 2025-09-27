# Abilities-Development-center-
<!-- Chosen Palette: المؤسسية (Primary #1f22c6)، الحيوية والتفاؤل (#f4d127)، الرقمنة والوضوح (#2fd3ec) -->
<!-- Application Structure Plan: The architecture is strategically reordered (The Authority Flow): 1. الرؤية والتشغيل (The Market Opportunity & Core Operations). 2. القيادة الرقمية (The Proprietary AI Suite - showcasing 4 LLM tools to validate feasibility). 3. خطة التنفيذ والنمو (The Execution Plan). 4. الأداء المالي (The Financial Proof/ROI). This structure, driven by a 20-year expert persona, prioritizes selling the defensible, tech-enabled operational efficiency first to overcome the financial conservatism associated with the 20-student target. All AI tools are grouped under a single powerful section to maximize impact. -->
<!-- Visualization & Content Choices: All four AI tools are simulated for 100% reliability. Financials use Chart.js for Donut (Budget Allocation) and Bar (Revenue/Expenses Comparison). The focus remains on clear, Arabic-centric UI/UX with full responsiveness, ensuring easy navigation between the strategically ordered sections. CONFIRMING NO SVG/Mermaid, using only Chart.js/Canvas and structured HTML/Tailwind. -->
<!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
<style>
  /* Base style for the responsive chart container */
  .chart-container {
    position: relative;
    width: 100%;
    max-width: 650px; /* Max width to prevent overly wide charts on desktop */
    margin-left: auto;
    margin-right: auto;
    height: 350px; /* Base height for desktop */
    max-height: 450px;
  }
  @media (max-width: 768px) {
    .chart-container {
      height: 300px; /* Slightly smaller height on mobile */
    }
  }
</style>
<script src="https://cdn.tailwindcss.com"></script>
<script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.2/dist/chart.umd.min.js"></script>
<script>
  // --- طبقة الحماية التقنية (لمنع النسخ السهل) ---
  document.addEventListener('contextmenu', event => event.preventDefault());
  document.addEventListener('keydown', event => {
    // منع مفاتيح F12، Ctrl+Shift+I, Ctrl+Shift+J, Ctrl+U
    if (event.keyCode === 123 || (event.ctrlKey && event.shiftKey && (event.keyCode === 73 || event.keyCode === 74)) || (event.ctrlKey && event.keyCode === 85)) {
      event.preventDefault();
    }
  });
  // --- نهاية طبقة الحماية ---
  
  tailwind.config = {
    theme: {
      extend: {
        colors: {
          'primary-stone': '#44403c',
          'trust-blue': '#1f22c6', /* الأزرق الداكن (المؤسسية) */
          'accent-amber': '#f4d127', /* الأصفر الذهبي (التفاؤل) */
          'soft-sand': '#f5f5f4',
          'highlight-cyan': '#2fd3ec', /* الأزرق الفاتح (الرقمنة والأخصائي) */
          'highlight-emerald': '#10b981', /* لون ثانوي للاستبقاء */
        }
      }
    }
  }
</script>

<div id="app" class="min-h-screen bg-soft-sand text-primary-stone font-sans p-4 md:p-8" dir="rtl">

  <!-- Header and Title -->
  <header class="text-center mb-10 p-6 bg-white shadow-2xl rounded-xl border-b-4 border-trust-blue">
    <!-- Logo area using Unicode/HTML elements -->
    <div class="flex flex-col items-center mb-4">
        <!-- Sun icon using the brand yellow/amber -->
        <div class="text-6xl text-accent-amber mb-2">☀️</div>
        <h1 class="text-4xl md:text-5xl font-extrabold text-trust-blue">مركز تنمية القدرات</h1>
        <p class="text-lg text-gray-600 mt-1">Abilities Development Center (ADC)</p>
    </div>
    
    <p class="text-xl md:text-2xl font-extrabold text-primary-stone">القيادة الرقمية لتأهيل أصحاب الهمم</p>
    <p class="text-base mt-2 text-accent-amber font-semibold">دراسة جدوى استراتيجية | مُقدمة من سيدي محمد صلاح الدين بوسعدية</p>
  </header>

  <!-- Navigation Tabs (for quick jump) -->
  <nav class="sticky top-0 z-10 bg-white p-3 shadow-lg rounded-xl mb-8 flex justify-center space-x-2 md:space-x-6 overflow-x-auto">
    <button onclick="scrollToSection('operations')" class="nav-btn bg-primary-stone text-white hover:bg-gray-700 px-4 py-2 rounded-lg text-sm md:text-base whitespace-nowrap transition duration-300 shadow">الرؤية والتشغيل</button>
    <button onclick="scrollToSection('ai_tools')" class="nav-btn bg-trust-blue text-white hover:bg-blue-700 px-4 py-2 rounded-lg text-sm md:text-base whitespace-nowrap transition duration-300 shadow">الميزة التكنولوجية (الذكاء الاصطناعي)</button>
    <button onclick="scrollToSection('strategy')" class="nav-btn bg-gray-200 text-primary-stone hover:bg-gray-300 px-4 py-2 rounded-lg text-sm md:text-base whitespace-nowrap transition duration-300 shadow">التنفيذ والنمو</button>
    <button onclick="scrollToSection('financials')" class="nav-btn bg-accent-amber text-primary-stone hover:bg-yellow-500 px-4 py-2 rounded-lg text-sm md:text-base whitespace-nowrap transition duration-300 shadow">الأداء المالي (مؤشرات الأداء)</button>
  </nav>

  <!-- Section 1: The Vision and Operations -->
  <section id="operations" class="mb-12 p-6 bg-white shadow-2xl rounded-xl border-t-4 border-primary-stone">
    <h2 class="text-2xl md:text-3xl font-bold mb-6 border-b pb-2 text-trust-blue">1. الرؤية وآلية التشغيل (تقليل مخاطر الاستثمار)</h2>
    <p class="mb-6 text-gray-600 font-medium">نحن لا ننشئ مركزاً آخر؛ نحن نبني منصة قادرة على التوسع إقليمياً. الآلية التشغيلية مصممة لتقليل التكاليف وزيادة مرونة الخدمة، وهو مفتاح النجاح في الخدمات المتخصصة.</p>

    <!-- Operational Flow -->
    <div class="space-y-4 mb-8">
        <h3 class="text-xl font-semibold text-trust-blue">آلية العمل المتكاملة:</h3>
        <div class="p-4 bg-gray-50 rounded-lg border border-gray-200 shadow-sm flex items-center">
            <span class="font-bold text-accent-amber w-1/4">1. التقييم:</span> <span class="text-sm">استمارة إلكترونية $\rightarrow$ تقييم أولي من الأخصائي.</span>
        </div>
        <div class="p-4 bg-gray-50 rounded-lg border border-gray-200 shadow-sm flex items-center">
            <span class="font-bold text-accent-amber w-1/4">2. الأتمتة:</span> <span class="text-sm">إنشاء **خطة فردية مُولّدة بالذكاء الاصطناعي** وربطها بالمكتبة التعليمية.</span>
        </div>
        <div class="p-4 bg-gray-50 rounded-lg border border-gray-200 shadow-sm flex items-center">
            <span class="font-bold text-accent-amber w-1/4">3. المتابعة:</span> <span class="text-sm">ولي الأمر يرفع فيديو تطبيق الطالب $\rightarrow$ الأخصائي يقيم ويرسل **ملخصاً آلياً**.</span>
        </div>
    </div>
    
    <!-- Benefits -->
    <h3 class="text-xl font-semibold mt-8 mb-4 text-primary-stone">العوائد الاستراتيجية المضمونة:</h3>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
        <div class="p-4 bg-highlight-emerald/10 rounded-lg shadow-inner text-center">
            <p class="font-bold text-highlight-emerald text-lg">انتشار غير محدود</p>
            <p class="text-sm mt-1">كسر حاجز الموقع الجغرافي والوصول إلى أسواق إقليمية جديدة.</p>
        </div>
        <div class="p-4 bg-highlight-cyan/10 rounded-lg shadow-inner text-center">
            <p class="font-bold text-highlight-cyan text-lg">تحسين قيمة العميل (LTV)</p>
            <p class="text-sm mt-1">دعم فوري ومستمر لولي الأمر، مما يضمن بقاء العميل لأطول فترة ممكنة.</p>
        </div>
        <div class="p-4 bg-accent-amber/10 rounded-lg shadow-inner text-center">
            <p class="font-bold text-accent-amber text-lg">تقليل التكلفة التشغيلية</p>
            <p class="text-sm mt-1">تفريغ الأخصائيين من 40% من مهامهم الإدارية والورقية عبر الأتمتة.</p>
        </div>
    </div>
  </section>
  
  <!-- Section 2: AI Capabilities - The Competitive Edge (Highest Priority) -->
  <section id="ai_tools" class="mb-12 p-6 bg-white shadow-2xl rounded-xl border-t-4 border-trust-blue">
    <h2 class="text-2xl md:text-3xl font-bold mb-6 border-b pb-2 text-trust-blue">2. القيادة الرقمية: أدوات الذكاء الاصطناعي الأربعة</h2>
    <p class="mb-6 text-gray-600 font-medium">هنا تكمن القيمة الحقيقية للاستثمار. الأخصائي هو قائد العملية، بينما تضاعف أدوات الذكاء الاصطناعي من كفاءته ودقة الخدمة المقدمة، مما يضمن جودة عالية بتكلفة أقل.</p>

    <!-- AI Tools Grouped by Function -->
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
        
        <!-- Group 1: SPECIALIST EFFICIENCY (CYAN) -->
        <div class="space-y-6">
            <h3 class="text-xl font-bold text-highlight-cyan border-b-2 border-highlight-cyan pb-2 flex items-center">
                <span class="text-2xl mr-2">⚙️</span> كفاءة الأخصائي والأتمتة
            </h3>
            
            <!-- AI Tool 1: Specialist Plan Builder -->
            <div class="p-6 bg-highlight-cyan/10 rounded-xl border border-highlight-cyan shadow-md">
                <h4 class="text-lg font-bold text-highlight-cyan flex items-center mb-4">
                    <span class="text-2xl mr-2">🤖</span> مُنشئ خطط العمل الفردية السريع
                </h4>
                <p class="text-gray-700 mb-4 text-sm">يولد خطط فردية قابلة للتنفيذ في ثوانٍ، مما يقلل الوقت اللازم للتخطيط. **دور الأخصائي:** مراجعة الخطة المولدة، تعديلها، وتخصيصها لتناسب حالة الطالب بدقة.</p>

                <div class="flex flex-col md:flex-row gap-4 mb-4">
                    <select id="specialtySelector" class="flex-grow p-3 border border-gray-300 rounded-lg focus:ring-highlight-cyan focus:border-highlight-cyan bg-white text-primary-stone">
                        <option value="">اختر مجال التخصص...</option>
                        <option value="life_skills">مهارات حياتية</option>
                        <option value="behavior_mod">تعديل سلوك</option>
                        <option value="vocational">تأهيل مهني (Canva)</option>
                        <option value="occupational">علاج وظيفي</option>
                        <option value="academic">أكاديمي (القراءة)</option>
                    </select>
                    <button id="generatePlanBtn" onclick="generatePlan()" class="w-full md:w-auto px-6 py-2 bg-highlight-cyan text-white font-semibold rounded-lg hover:bg-cyan-600 transition duration-300 shadow-lg">عرض الخطة النموذجية</button>
                </div>
                <div id="planOutput" class="p-4 bg-white rounded-lg border border-gray-300 text-xs hidden">
                    <h5 class="font-bold text-primary-stone mb-1">الخطة المولدة:</h5>
                    <pre id="planContent" class="whitespace-pre-wrap font-mono text-gray-800"></pre>
                </div>
            </div>

            <!-- AI Tool 3: Instant Behavioral Support Consultant -->
            <div class="p-6 bg-highlight-cyan/10 rounded-xl border border-highlight-cyan shadow-md">
                <h4 class="text-lg font-bold text-highlight-cyan flex items-center mb-4">
                    <span class="text-2xl mr-2">💡</span> مستشار الدعم السلوكي الفوري
                </h4>
                <p class="text-gray-700 mb-4 text-sm">يقدم إرشادات سريعة ومصاغة باحترافية **للأخصائي** ليتمكن من الرد الفوري على أسئلة الولي. **دور الأخصائي:** يستخدم الرد كمسودة مرجعية ويصيغ الرد النهائي بلمسة شخصية.</p>
                
                <button id="showQnABtn" onclick="showQnA()" class="w-full px-6 py-2 bg-highlight-cyan text-white font-semibold rounded-lg hover:bg-cyan-600 transition duration-300 shadow-lg mb-4">عرض نموذج استشارة</button>

                <div id="qnaInput" class="p-4 bg-gray-100 rounded-lg border border-gray-300 text-xs hidden">
                    <h5 class="font-bold mb-1 text-gray-700">سؤال الولي (المدخل):</h5>
                    <pre id="qnaContentInput" class="whitespace-pre-wrap font-mono text-gray-800"></pre>
                </div>

                <div id="qnaOutput" class="mt-2 p-4 bg-white rounded-lg border border-gray-300 text-xs hidden">
                    <h5 class="font-bold text-primary-stone mb-1">إجابة المستشار (المخرج - تُصاغ بواسطة الأخصائي):</h5>
                    <pre id="qnaContentOutput" class="whitespace-pre-wrap font-mono text-gray-800"></pre>
                </div>
            </div>

        </div>

        <!-- Group 2: CLIENT RETENTION & ACQUISITION (EMERALD/AMBER) -->
        <div class="space-y-6">
            <h3 class="text-xl font-bold text-highlight-emerald border-b-2 border-highlight-emerald pb-2 flex items-center">
                <span class="text-2xl mr-2">💖</span> التواصل والاستبقاء (قيمة العميل الدائمة)
            </h3>

            <!-- AI Tool 2: Periodic Report Summarizer -->
            <div class="p-6 bg-highlight-emerald/10 rounded-xl border border-highlight-emerald shadow-md">
                <h4 class="text-lg font-bold text-highlight-emerald flex items-center mb-4">
                    <span class="text-2xl mr-2">📊</span> مُلخص التقارير الدورية الآلي
                </h4>
                <p class="text-gray-700 mb-4 text-sm">يقلب التقارير المعقدة إلى ملخصات موجزة وإجراءات منزلية فورية. **دور الأخصائي:** يراجع الملخص الآلي للتأكد من دقته ثم يرسله لولي الأمر، مما يرفع من جودة خدمة العملاء.</p>

                <button id="showReportBtn" onclick="showReportSummary()" class="w-full px-6 py-2 bg-highlight-emerald text-white font-semibold rounded-lg hover:bg-emerald-600 transition duration-300 shadow-lg mb-4">عرض نموذج الملخص التلقائي</button>

                <div id="reportInput" class="p-4 bg-gray-100 rounded-lg border border-gray-300 text-xs hidden">
                    <h5 class="font-bold mb-1 text-gray-700">تقرير الأخصائي المفصل (المدخل):</h5>
                    <pre id="reportContentInput" class="whitespace-pre-wrap font-mono text-gray-800"></pre>
                </div>

                <div id="summaryOutput" class="mt-2 p-4 bg-white rounded-lg border border-gray-300 text-xs hidden">
                    <h5 class="font-bold text-primary-stone mb-1">الملخص والإجراءات المقترحة (المخرج):</h5>
                    <pre id="summaryContent" class="whitespace-pre-wrap font-mono text-gray-800"></pre>
                    <pre id="recommendationsContent" class="whitespace-pre-wrap font-mono text-gray-800 mt-2 border-t pt-2"></pre>
                </div>
            </div>

            <!-- AI Tool 4: Marketing Slogan Generator (Now Interactive) -->
            <div class="p-6 bg-accent-amber/10 rounded-xl border border-accent-amber shadow-md">
                <h4 class="text-lg font-bold text-accent-amber flex items-center mb-4">
                    <span class="text-2xl mr-2">🚀</span> مُولِّد الأفكار التسويقية التفاعلي
                </h4>
                <p class="text-gray-700 mb-4 text-sm">أداة تسويقية تتيح للمركز توليد أفكار وشعارات جديدة ومناسبة لـ **تحسين محركات البحث (SEO)** بناءً على مفاهيم مبتكرة. **يمكن مشاركة الإخراج مباشرة مع المستثمر.**</p>
                
                <input type="text" id="marketingIdeaInput" placeholder="اكتب فكرة تسويقية للتحليل (مثلاً: ضمان استمرارية العلاج)..." class="w-full p-2 border border-gray-300 rounded-lg focus:ring-accent-amber focus:border-accent-amber mb-3 text-sm text-primary-stone" />
                <button id="generateMarketingIdeaBtn" onclick="generateMarketingIdea()" class="w-full px-6 py-2 bg-accent-amber text-primary-stone font-semibold rounded-lg hover:bg-yellow-500 transition duration-300 shadow-lg">توليد زوايا تسويقية (ذكاء اصطناعي)</button>
                
                <div id="marketingOutput" class="mt-4 p-4 bg-white rounded-lg border border-gray-300 text-xs hidden">
                    <!-- Output will be displayed here -->
                </div>
            </div>

        </div>
    </div>

  </section>

  <!-- Section 3: Execution and Growth Plan -->
  <section id="strategy" class="mb-12 p-6 bg-white shadow-2xl rounded-xl border-t-4 border-accent-amber">
    <h2 class="text-2xl md:text-3xl font-bold mb-6 border-b pb-2 text-primary-stone">3. خطة التنفيذ والنمو (Execution and Scale)</h2>
    <p class="mb-6 text-gray-600 font-medium">الخطة مصممة بعناية لتقليل المخاطر في المراحل المبكرة وضمان الإطلاق السلس للمنصة (الميزانية الأولية: $60,000$ د.إ).</p>

    <!-- Timeline Grid -->
    <h3 class="text-xl font-semibold mb-3 text-trust-blue">الخطة الزمنية (12 شهرًا)</h3>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8 text-center">
      <!-- Phase 1 -->
      <div class="p-4 bg-soft-sand rounded-lg border-b-4 border-red-500 shadow-md">
        <p class="font-bold text-lg mb-1">شهر 1 – 3</p>
        <p class="text-sm font-medium">بناء المنصة والتطبيق ($44,000$ د.إ) + تجهيز المحتوى التعليمي.</p>
      </div>
      <!-- Phase 2 -->
      <div class="p-4 bg-soft-sand rounded-lg border-b-4 border-yellow-500 shadow-md">
        <p class="font-bold text-lg mb-1">شهر 4 – 6</p>
        <p class="text-sm font-medium">إطلاق تجريبي + بدء حملات التسويق ($6,000$ د.إ) + إطلاق **تحسين محركات البحث (SEO)**.</p>
      </div>
      <!-- Phase 3 -->
      <div class="p-4 bg-soft-sand rounded-lg border-b-4 border-green-500 shadow-md">
        <p class="font-bold text-lg mb-1">شهر 7 – 12</p>
        <p class="text-sm font-medium">التوسع التدريجي + إطلاق خدمات استشارية جديدة + تجاوز هدف الـ 20 طالبًا.</p>
      </div>
    </div>
    
    <!-- Marketing Strategy -->
    <h3 class="text-xl font-semibold mt-10 mb-4 text-trust-blue">استراتيجية التسويق والانتشار:</h3>
    <ul class="list-disc list-inside text-primary-stone text-sm space-y-2">
        <li>**التركيز على القيمة (LTV):** استخدام أدوات الذكاء الاصطناعي كدليل على جودة الخدمة العالية في المحتوى الإعلاني.</li>
        <li>**التسويق العضوي (SEO):** تحسين محركات البحث للظهور في نتائج "علاج وظيفي عن بعد" لتقليل **تكلفة اكتساب العميل (CAC)**.</li>
        <li>**الشراكات الاستراتيجية:** التعاون مع جمعيات ومؤسسات ذوي الهمم للوصول إلى الجمهور المستهدف بثقة عالية.</li>
    </ul>

  </section>

  <!-- Section 4: Financial Summary and KPIs (The Final Proof) -->
  <section id="financials" class="mb-12 p-6 bg-white shadow-2xl rounded-xl border-t-4 border-trust-blue">
    <h2 class="text-2xl md:text-3xl font-bold mb-6 border-b pb-2 text-trust-blue">4. الأداء المالي ومؤشرات الأداء الرئيسية (KPIs)</h2>
    <p class="mb-6 text-gray-600 font-medium">الهدف متحفظ ($20$ طالب)، لكن التكاليف التشغيلية المنخفضة بفضل الأتمتة تضمن **الربحية والاستدامة**.</p>

    <!-- Financial Metrics Grid -->
    <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mb-8">
      <!-- Metric 1 (Students) -->
      <div class="bg-soft-sand p-4 rounded-lg shadow-inner text-center">
        <p class="text-3xl font-extrabold text-accent-amber" id="metric-students">20</p>
        <p class="text-sm font-semibold text-primary-stone">الطلاب المستهدفون (س1)</p>
      </div>
      <!-- Metric 2 (Revenue) -->
      <div class="bg-soft-sand p-4 rounded-lg shadow-inner text-center">
        <p class="text-3xl font-extrabold text-highlight-emerald" id="metric-revenue">240,000</p>
        <p class="text-sm font-semibold text-primary-stone">الإيرادات السنوية المتوقعة (د.إ)</p>
      </div>
      <!-- Metric 3 (Profit) -->
      <div class="bg-soft-sand p-4 rounded-lg shadow-inner text-center">
        <p class="text-3xl font-extrabold text-highlight-cyan" id="metric-profit">10,000 - 30,000</p>
        <p class="text-sm font-semibold text-primary-stone">صافي الأرباح المتوقع (د.إ) *</p>
      </div>
      <!-- Metric 4 (Break-Even) -->
      <div class="bg-soft-sand p-4 rounded-lg shadow-inner text-center">
        <p class="text-3xl font-extrabold text-primary-stone" id="metric-breakeven">3 - 4</p>
        <p class="text-sm font-semibold text-gray-600">أشهر نقطة التعادل (للتطوير)</p>
      </div>
    </div>
    <p class="text-xs text-gray-500 mt-2">* صافي الربح بعد خصم التكاليف التشغيلية السنوية واسترداد تكلفة التطوير الأولية ($60,000$ د.إ).</p>

    <!-- Chart Row: Budget vs Revenue -->
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 mt-10">
      
      <!-- Chart 1: Budget Distribution -->
      <div>
        <h3 class="text-xl font-semibold mb-3 text-primary-stone">توزيع ميزانية التطوير الأولية ($60,000$ د.إ)</h3>
        <p class="text-sm text-gray-500 mb-4">يجب أن تُستخدم هذه الميزانية لضمان أن المنصة متوافقة مع متطلبات الذكاء الاصطناعي الموضحة.</p>
        <div class="chart-container h-80">
          <canvas id="budgetChart"></canvas>
        </div>
      </div>

      <!-- Chart 2: Revenue vs Expenses -->
      <div>
        <h3 class="text-xl font-semibold mb-3 text-primary-stone">مقارنة الإيرادات بالتكاليف الثابتة</h3>
        <p class="text-sm text-gray-500 mb-4">نعمل على ضمان أن تكون **قيمة العميل الدائمة $\gg$ تكلفة اكتساب العميل** باستخدام استراتيجية الذكاء الاصطناعي الموضحة.</p>
        <div class="chart-container h-80">
          <canvas id="revenueChart"></canvas>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="text-center p-4 mt-8 text-sm text-gray-500 border-t border-gray-300">
    <p>&copy; 2025 القيادة الرقمية لتأهيل أصحاب الهمم. هذا العرض محمي بحقوق الملكية الفكرية.</p>
  </footer>

</div>

<script>
  
  const APP_STATE = {
    targetStudents: 20,
    avgMonthlySubscription: 1000, // AED
    annualRevenue: 240000, // 20 * 1000 * 12
    fixedDevelopmentCost: 60000, // AED
    estimatedOperatingExpenses: 150000, // AED (Salaries, Marketing, Maintenance)
    netProfit: 30000, // Simplified for presentation: Revenue - Dev Cost - OpEx
  };

  const budgetData = {
    labels: ['تطوير المنصة', 'تطبيق الهاتف', 'التدريب والمحتوى', 'التسويق الرقمي', 'احتياطي وصيانة'],
    data: [27000, 17000, 5000, 6000, 5000],
    colors: ['#f4d127', '#1f22c6', '#2fd3ec', '#10b981', '#44403c'] // Using brand colors and tertiary
  };

  const revenueData = {
    labels: ['الإيرادات السنوية (20 طالب)', 'التكاليف التشغيلية (المقدرة)', 'تكلفة التطوير الثابتة'],
    values: [
      APP_STATE.annualRevenue,
      APP_STATE.estimatedOperatingExpenses,
      APP_STATE.fixedDevelopmentCost
    ],
    colors: ['#10b981', '#f4d127', '#1f22c6'] // Using brand colors and secondary
  };

  // --- LLM Simulation Data (Ensures 100% Functionality) ---
  const simulatedPlans = {
    'life_skills': `## خطة عمل فردية: الاستقلالية في ارتداء الملابس

**الهدف العام:** أن يتمكن الطالب من ارتداء سرواله (بنطاله) وقميصه (التي شيرت) بمساعدة جزئية خلال 30 يومًا.

**المجال التخصصي:** المهارات الحياتية - الاستقلالية.

**المستوى الحالي:** مبتدئ (يحتاج مساعدة كلية وتوجيهاً كاملاً).

### الخطوات القابلة للقياس (A - B - C)

#### 1. التدريب على المكونات الأولية (المهارة الجزئية)
* **الخطوة:** يتعلم الطالب سحب أو دفع الملابس (السروال) للأمام والخلف لمسافة قصيرة (15 سم) بعد أن يكون الأهل قد أدخلوا ساقه الأولى بشكل كامل.
* **المتابعة والقياس:** يتم تسجيل 5 محاولات ناجحة يوميًا بدون أي مقاومة، مع استخدام التعزيز الإيجابي.

#### 2. ربط المهارات (التسلسل)
* **الخطوة:** يقوم الطالب بإدخال الساقين في السروال وهو جالس، ثم يقف ويكمل سحب السروال إلى أعلى الركبتين بمساعدة إشارة لفظية فقط من ولي الأمر.
* **المتابعة والقياس:** نجاح الطالب في تنفيذ هذا التسلسل لمدة 7 أيام متتالية بمساعدة لفظية فقط (دون تدخل جسدي).

#### 3. التعميم والاستقلالية الجزئية
* **الخطوة:** يتمكن الطالب من ارتداء السروال والقميص (بدءاً من إدخال الرأس والذراعين) بشكل شبه مستقل، حيث يقدم ولي الأمر المساعدة فقط في الأجزاء المعقدة مثل الأزرار أو تعديل القبة.
* **المتابعة والقياس:** يتم تحقيق الهدف عندما يتمكن الطالب من ارتداء 70% من ملابسه دون مساعدة جسدية، ويتم توثيق ذلك بفيديو يرسل للأخصائي نهاية كل أسبوع.`,
    
    'behavior_mod': `## خطة عمل فردية: التعامل مع نوبات الغضب

**الهدف العام:** تقليل تكرار نوبات الغضب بنسبة 50% وتخفيض مدتها إلى أقل من دقيقتين خلال 6 أسابيع.

**المجال التخصصي:** تعديل السلوك.

**المستوى الحالي:** متكرر (يحدث 3-4 مرات يومياً بمتوسط 5 دقائق).

### الخطوات القابلة للقياس (A - B - C)

#### 1. تحديد السبب والمحفزات
* **الخطوة:** يقوم ولي الأمر بتسجيل وقت ومكان ومحفز كل نوبة غضب (A-B-C Analysis) لمدة أسبوعين.
* **المتابعة والقياس:** تحديد المحفزات الأكثر شيوعاً (مثل: الإحباط من مهمة صعبة أو الانتقال من نشاط محبب لآخر).

#### 2. التدريب على مهارات الاستجابة البديلة
* **الخطوة:** تعليم الطالب استراتيجيتين للاستجابة (مثل: التنفس العميق 5 مرات، أو طلب استراحة).
* **المتابعة والقياس:** تسجيل 5 استخدامات ناجحة لمهارة الاستجابة البديلة قبل البدء في النوبة.

#### 3. التعزيز التفاضلي والتهدئة الذاتية
* **الخطوة:** تجاهل السلوك غير المرغوب به (نوبة الغضب) وتعزيز السلوكيات الإيجابية (الهدوء واللعب الهادئ).
* **المتابعة والقياس:** تسجيل أسبوعين متتاليين بمتوسط نوبة غضب واحدة يومياً أو أقل بمدة لا تتجاوز دقيقتين.`,

    'vocational': `## خطة عمل فردية: التدريب على استخدام تطبيقات التصميم (Canva)

**الهدف العام:** تصميم بطاقة تهنئة بسيطة باستخدام تطبيق Canva بشكل مستقل خلال 5 جلسات تدريبية أسبوعية.

**المجال التخصصي:** التأهيل المهني (الأعمال الرقمية).

**المستوى الحالي:** مبتدئ (لا يمتلك معرفة بالمنصة، يحتاج مساعدة في التوجيه البصري).

### الخطوات القابلة للقياس (A - B - C)

#### 1. التعرف على واجهة التطبيق
* **الخطوة:** يتعرف الطالب على واجهة Canva، ويستطيع تحديد شريط الأدوات الرئيسي (النصوص، العناصر، الخلفيات).
* **المتابعة والقياس:** نجاح الطالب في تحديد واستدعاء 3 أدوات أساسية عند الطلب المباشر من الأخصائي.

#### 2. استخدام القوالب والتعديل البسيط
* **الخطوة:** يتمكن الطالب من اختيار قالب بطاقة تهنئة جاهز، وتغيير النصوص والألوان الأساسية فيه.
* **المتابعة والقياس:** إنشاء 3 بطاقات تهنئة مختلفة في الأسبوع، مع تخصيص 3 عناصر في كل بطاقة (لون، خط، صورة).

#### 3. تصميم بطاقة بسيطة من الصفر
* **الخطوة:** يتمكن الطالب من فتح صفحة بيضاء (قماش فارغ) واختيار الخلفية والعناصر، وكتابة نص مناسب بشكل مستقل.
* **المتابعة والقياس:** يتم تحقيق الهدف عندما يقدم الطالب بطاقة تهنئة كاملة وعملية للمركز أو العائلة، تُظهر استخدامه الوظيفي لـ 5 أدوات مختلفة في Canva.`,
    
    'occupational': `## خطة عمل فردية: تحسين الإمساك الدقيق (Fine Motor Skills)

**الهدف العام:** أن يتمكن الطالب من الإمساك بقلم الرصاص والكتابة بضغط مناسب والتحكم في حركات الأصابع بشكل وظيفي خلال 4 أسابيع.

**المجال التخصصي:** العلاج الوظيفي.

**المستوى الحالي:** متوسط (يستخدم قبضة راحة اليد الكاملة، وضغط قوي أو ضعيف جداً).

### الخطوات القابلة للقياس (A - B - C)

#### 1. تقوية العضلات الدقيقة والأوتار
* **الخطوة:** تنفيذ أنشطة ضغط متكررة (مثل الضغط على كرات مطاطية صغيرة أو العجن بمعجون اللعب) لمدة 5 دقائق يوميًا.
* **المتابعة والقياس:** يتم تسجيل القدرة على الضغط بشكل ثابت وموحد على الكرات، وتوثيق ذلك بالفيديو من ولي الأمر مرتين أسبوعيًا.

#### 2. تطوير قبضة القلم الثلاثية (Tripod Grasp)
* **الخطوة:** استخدام أدوات مساعدة (مثل مقبض القلم السميك - Pencil Grip) للتدريب على الإمساك الصحيح بين الإبهام والسبابة والوسطى.
* **المتابعة والقياس:** نجاح الطالب في الإمساك الصحيح (قبضة الثلاثية) أثناء محاولات التلوين أو الرسم لمدة 10 دقائق متواصلة.

#### 3. التحكم في الضغط والتتبع البصري الحركي
* **الخطوة:** التدرب على تمارين "التتبع" (Tracing) لخطوط وأشكال هندسية، مع توجيه ولي الأمر لضبط ضغط القلم على الورقة.
* **المتابعة والقياس:** يتم تحقيق الهدف عندما يتمكن الطالب من تتبع 90% من خطوط الأشكال دون خروج أو تمزيق للورقة بسبب الضغط المفرط.`,
    
    'academic': `## خطة عمل فردية: تحسين مهارات القراءة (Academic)

**الهدف العام:** أن يتمكن الطالب من قراءة جمل بسيطة من 3 كلمات بشكل مستقل بمساعدة صور توضيحية خلال 8 أسابيع.

**المجال التخصصي:** المجال الأكاديمي.

**المستوى الحالي:** مبتدئ (يتعرف على الحروف، يخلط بين الكلمات).

### الخطوات القابلة للقياس (A - B - C)

#### 1. مطابقة الكلمة بالصورة
* **الخطوة:** التدرب على مجموعة من 10 كلمات أساسية (مثل: كرة، قطة، بيت)، ومطابقتها بالصور المقابلة.
* **المتابعة والقياس:** نجاح الطالب في مطابقة 9 من 10 كلمات بالصورة الصحيحة في 3 جلسات متتالية.

#### 2. قراءة الكلمات المجمعة في جمل قصيرة
* **الخطوة:** قراءة جمل بسيطة مكونة من كلمتين (مثل: "القطة تنام"، "الولد يلعب") بمساعدة الولي.
* **المتابعة والقياس:** قراءة 5 جمل قصيرة يوميًا بشكل صحيح مع مساعدة جزئية (تذكير بالكلمات الصعبة).

#### 3. القراءة المستقلة للجمل البسيطة
* **الخطوة:** يتمكن الطالب من قراءة جمل بسيطة من 3 كلمات (مثل: "الولد يأكل التفاحة") دون مساعدة، بالاعتماد على الصور التوضيحية.
* **المتابعة والقياس:** قراءة 3 جمل جديدة بشكل مستقل دون مساعدة أو تصحيح، ويتم توثيق ذلك بفيديو مرة واحدة أسبوعيًا.`,
  };

  const simulatedSummary = {
    input: `التقرير الأسبوعي للطالب خالد: تم إحراز تقدم جيد في الهدف الأول المتعلق بمهارة ارتداء السروال. قام خالد بنجاح بإدخال ساقيه في 4 من 5 محاولات بمساعدة لفظية فقط. ومع ذلك، لا تزال هناك مقاومة عند الانتقال إلى مهمة ارتداء القميص، حيث أظهر نوبة غضب قصيرة (30 ثانية) في يوم الأربعاء عند مواجهة صعوبة في تمرير ذراعه اليمنى. الجلسات البصرية لتمارين التركيز تم تنفيذها بالكامل، وكانت مدتها 7 دقائق في المتوسط. يحتاج الولي لزيادة التعزيز الإيجابي عند محاولته ارتداء القميص، حتى لو لم ينجح بشكل كامل. يجب أيضاً تخفيف الضغط في الأنشطة الصباحية.`,
    summary: `**ملخص أداء خالد الأسبوعي:** تقدم ممتاز في ارتداء السروال بالاعتماد على التوجيه اللفظي. التحدي الرئيسي هو مقاومة عند ارتداء القميص وظهور نوبة غضب قصيرة واحدة.`,
    recommendations: `**الخطوات المقترحة للأسبوع القادم:**
        1. **التركيز على القميص:** تقسيم مهمة ارتداء القميص إلى خطوتين صغيرتين جداً (إدخال الرأس أولاً فقط).
        2. **زيادة التعزيز:** استخدام مكافأة فورية محببة لخالد مباشرة بعد كل محاولة لارتداء القميص، بغض النظر عن النتيجة.
        3. **تطبيق الاستراحة النشطة:** دمج 5 دقائق من النشاط البدني الخفيف بين التمارين السلوكية لتخفيف الضغط.`
  };
  
  const simulatedQnA = {
    question: "كيف يمكنني مساعدة ابني المصاب بالتوحد على تقليل فرط الحساسية للضوضاء العالية في الأماكن العامة؟",
    answer: `## استجابة المستشار السلوكي الفوري

**الطلب:** استراتيجية لتقليل حساسية الضوضاء العالية في الأماكن العامة.

**1. الإعداد المسبق:**
* **التطبيق:** قبل الذهاب إلى مكان صاخب (مثل مركز تسوق)، قم بعرض مقطع صوتي مشابه للضوضاء في المنزل بمستويات صوت منخفضة جداً وزيادتها تدريجياً.
* **الهدف:** بناء تحمل تدريجي وتجنب عنصر المفاجأة.

**2. أدوات المساعدة الحسية:**
* **التطبيق:** استخدم سماعات إلغاء الضوضاء (Noise-canceling headphones) أو سدادات الأذن كأداة وقائية في البداية.
* **الهدف:** توفير سيطرة فورية على المدخلات السمعية وتقليل القلق.

**3. استراتيجية "الإشارات المرئية":**
* **التطبيق:** علّم الطفل إشارة يد أو رمزاً مرئياً معيناً يعني "أحتاج الابتعاد/الهدوء". استخدم هذه الإشارة فوراً عند ملاحظة أول علامة انزعاج لديه.
* **الهدف:** تمكين الطفل من التعبير عن حاجته دون اللجوء إلى السلوك الصعب.

**4. التعزيز الفوري:**
* **التطبيق:** قم بتعزيز سلوك الصبر والهدوء فوراً بعد مرور فترة زمنية قصيرة (دقيقة واحدة) في البيئة الصاخبة، ثم زد الفترة تدريجياً في المرات اللاحقة.
* **الهدف:** ربط تحمل الضوضاء بنتائج إيجابية ومكافآت.`
};

  // --- Chart Initialization ---

  document.addEventListener('DOMContentLoaded', () => {
    
    // 1. Budget Chart (Donut)
    const budgetCtx = document.getElementById('budgetChart').getContext('2d');
    new Chart(budgetCtx, {
      type: 'doughnut',
      data: {
        labels: budgetData.labels,
        datasets: [{
          data: budgetData.data,
          backgroundColor: budgetData.colors,
          hoverOffset: 4
        }]
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        plugins: {
          legend: {
            position: 'top',
            labels: {
              font: {
                family: 'sans-serif' 
              },
              boxWidth: 20
            }
          },
          title: {
            display: false,
          },
          tooltip: {
            callbacks: {
              label: function(context) {
                let label = context.label || '';
                if (label) {
                  label += ': ';
                }
                label += new Intl.NumberFormat('ar-AE', { style: 'currency', currency: 'AED' }).format(context.parsed);
                return label;
              }
            }
          }
        }
      }
    });

    // 2. Revenue Chart (Bar)
    const revenueCtx = document.getElementById('revenueChart').getContext('2d');
    new Chart(revenueCtx, {
      type: 'bar',
      data: {
        labels: revenueData.labels,
        datasets: [{
          label: 'القيمة بالدرهم الإماراتي',
          data: revenueData.values,
          backgroundColor: revenueData.colors,
          borderRadius: 5,
          borderWidth: 1
        }]
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        scales: {
          y: {
            beginAtZero: true,
            ticks: {
                callback: function(value, index, values) {
                    return value.toLocaleString('ar-AE') + ' د.إ';
                }
            }
          },
          x: {
             ticks: {
              font: {
                family: 'sans-serif' 
              }
            }
          }
        },
        plugins: {
          legend: {
            display: false
          },
          tooltip: {
            callbacks: {
              label: function(context) {
                let label = context.dataset.label || '';
                if (label) {
                  label += ': ';
                }
                label += new Intl.NumberFormat('ar-AE', { style: 'currency', currency: 'AED' }).format(context.parsed.y);
                return label;
              }
            }
          }
        }
      }
    });
  });

  // --- JS Functions ---

  function scrollToSection(id) {
    document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
  }

  function generatePlan() {
    const selector = document.getElementById('specialtySelector');
    const selectedPlanKey = selector.value;
    const planOutputDiv = document.getElementById('planOutput');
    const planContentPre = document.getElementById('planContent');

    if (!selectedPlanKey) {
        planOutputDiv.classList.add('hidden');
        return;
    }

    const planText = simulatedPlans[selectedPlanKey] || "لم يتم العثور على خطة لهذا التخصص بعد.";
    
    planContentPre.textContent = planText;
    planOutputDiv.classList.remove('hidden');
  }

  function showReportSummary() {
      const reportInputDiv = document.getElementById('reportInput');
      const reportContentInput = document.getElementById('reportContentInput');
      const summaryOutputDiv = document.getElementById('summaryOutput');
      const summaryContentPre = document.getElementById('summaryContent');
      const recommendationsContentPre = document.getElementById('recommendationsContent');

      // Set input and output content from the simulation data
      reportContentInput.textContent = simulatedSummary.input;
      summaryContentPre.innerHTML = simulatedSummary.summary;
      recommendationsContentPre.innerHTML = simulatedSummary.recommendations;

      // Show the hidden divs
      reportInputDiv.classList.remove('hidden');
      summaryOutputDiv.classList.remove('hidden');
      
      document.getElementById('showReportBtn').textContent = 'تم عرض النموذج بنجاح';
  }
  
  function showQnA() {
      const qnaInputDiv = document.getElementById('qnaInput');
      const qnaContentInput = document.getElementById('qnaContentInput');
      const qnaOutputDiv = document.getElementById('qnaOutput');
      const qnaContentOutput = document.getElementById('qnaContentOutput');

      // Set input and output content from the simulation data
      qnaContentInput.textContent = simulatedQnA.question;
      qnaContentOutput.innerHTML = simulatedQnA.answer;

      // Show the hidden divs
      qnaInputDiv.classList.remove('hidden');
      qnaOutputDiv.classList.remove('hidden');
      
      document.getElementById('showQnABtn').textContent = 'تم عرض الاستشارة بنجاح';
  }

  function generateMarketingIdea() {
      const inputField = document.getElementById('marketingIdeaInput');
      const inputIdea = inputField.value.trim();
      const outputDiv = document.getElementById('marketingOutput');

      if (inputIdea === "") {
          outputDiv.innerHTML = `<p class="text-red-500 font-bold">الرجاء إدخال فكرة تسويقية أو مفهوم للتحليل (مثلاً: ضمان استمرارية العلاج).</p>`;
          outputDiv.classList.remove('hidden');
          return;
      }

      // Simulated AI response based on the input
      const simulatedResponse = `
          <h5 class="font-bold text-trust-blue mb-2">تحليل المفهوم: "${inputIdea}"</h5>
          <div class="space-y-3 mt-3">
              <div class="p-3 bg-white rounded-lg shadow-sm">
                  <p class="font-semibold text-primary-stone text-sm">زاوية 1: الشعار العاطفي</p>
                  <p class="text-accent-amber italic mt-1 text-xs">"أصبح تأهيل طفلك رحلة من بيتك. ${inputIdea.slice(0, 40)}... يبني مستقبلاً أفضل."</p>
              </div>
              <div class="p-3 bg-white rounded-lg shadow-sm">
                  <p class="font-semibold text-primary-stone text-sm">زاوية 2: الشعار المنطقي (حل المشكلة)</p>
                  <p class="text-accent-amber italic mt-1 text-xs">"توقف عن البحث عن مراكز بعيدة. نقدّم ${inputIdea.slice(0, 40)}... بأقل تكلفة وجهد تحت إشراف متخصص."</p>
              </div>
              <div class="p-3 bg-white rounded-lg shadow-sm">
                  <p class="font-semibold text-primary-stone text-sm">زاوية 3: دعوة العمل الموجهة</p>
                  <p class="text-accent-amber italic mt-1 text-xs">"ابدأ الآن خطوة ${inputIdea.slice(0, 40)}... استشر أخصائيينا لتأكيد التوافق."</p>
              </div>
          </div>
      `;

      outputDiv.innerHTML = simulatedResponse;
      outputDiv.classList.remove('hidden');
  }
</script>

