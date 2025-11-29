<html lang="th">
  <head>
    <meta charset="UTF-8" />
    <title>Nutriton Scan | AI Food & Nutrition Analyzer</title>
    <meta name="viewport" content="width=device-width, initial-scale=1" />

    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>

    <!-- Google Font -->
    <link
      href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600;700&display=swap"
      rel="stylesheet"
    />

    <style>
      body {
        font-family: "Kanit", system-ui, -apple-system, BlinkMacSystemFont,
          "Segoe UI", sans-serif;
      }
      .glass-card {
        background: rgba(255, 255, 255, 0.92);
        backdrop-filter: blur(16px);
      }
      .pill {
        border-radius: 999px;
      }
    </style>
  </head>
  <body class="min-h-screen bg-gradient-to-br from-emerald-50 via-green-50 to-emerald-100">
    <div
      class="min-h-screen flex items-center justify-center px-4 py-6 sm:px-6 lg:px-8"
    >
      <div
        class="max-w-5xl w-full glass-card shadow-2xl rounded-3xl border border-emerald-100/60 p-6 sm:p-8 lg:p-10"
      >
        <!-- Header -->
        <header class="flex flex-col lg:flex-row gap-4 lg:items-center mb-6">
          <div
            class="flex items-center gap-3 bg-gradient-to-r from-emerald-500 to-lime-500 text-white px-4 py-3 rounded-2xl shadow-lg"
          >
            <div
              class="w-10 h-10 flex items-center justify-center bg-white/10 rounded-2xl"
            >
              🍽️
            </div>
            <div>
              <h1 class="text-xl sm:text-2xl font-semibold tracking-wide">
                Nutriton Scan
              </h1>
              <p class="text-xs sm:text-sm text-emerald-50/90">
                แอปช่วยสแกนอาหาร & วิเคราะห์โภชนาการอย่างรวดเร็ว
              </p>
            </div>
          </div>

          <div class="flex-1 flex flex-wrap gap-2 justify-end text-xs sm:text-sm">
            <span
              class="pill px-3 py-1 bg-emerald-50 text-emerald-700 border border-emerald-200 flex items-center gap-1"
            >
              <span class="w-2 h-2 rounded-full bg-emerald-500"></span>
              ใช้งานบนเว็บได้ทันที
            </span>
            <span
              class="pill px-3 py-1 bg-white text-emerald-700 border border-emerald-200"
            >
              ระบุพลังงาน (kcal) • โปรตีน • คาร์บ • ไขมัน
            </span>
          </div>
        </header>

        <!-- Main layout -->
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-6 lg:gap-8">
          <!-- LEFT: Input Panel -->
          <section
            class="space-y-4 sm:space-y-5 bg-emerald-50/60 border border-emerald-100 rounded-2xl p-4 sm:p-5"
          >
            <h2 class="font-semibold text-emerald-900 flex items-center gap-2">
              <span
                class="w-8 h-8 flex items-center justify-center bg-white rounded-2xl shadow-sm"
                >🧪</span
              >
              กรอกข้อมูลอาหาร / อัปโหลดรูป
            </h2>

            <!-- Food name -->
            <div class="space-y-1.5">
              <label
                for="food-name"
                class="text-sm font-medium text-emerald-900"
              >
                ชื่ออาหาร <span class="text-emerald-500">(ภาษาไทย/อังกฤษ)</span>
              </label>
              <input
                id="food-name"
                type="text"
                placeholder="เช่น ข้าวไก่ย่าง, ส้มตำไทย, grilled chicken, latte"
                class="w-full text-sm rounded-xl border border-emerald-200 px-3 py-2.5 focus:outline-none focus:ring-2 focus:ring-emerald-400 focus:border-emerald-400 bg-white/80"
              />
              <p class="text-[11px] text-emerald-600">
                ถ้าไม่กรอกชื่อ ระบบจะใช้ค่ามาตรฐานอาหารจานทั่วไป
              </p>
            </div>

            <!-- Portion -->
            <div class="grid grid-cols-2 gap-3">
              <div class="space-y-1.5">
                <label
                  for="portion"
                  class="text-sm font-medium text-emerald-900"
                >
                  ปริมาณ (กรัม)
                </label>
                <input
                  id="portion"
                  type="number"
                  min="1"
                  step="1"
                  placeholder="100"
                  class="w-full text-sm rounded-xl border border-emerald-200 px-3 py-2.5 focus:outline-none focus:ring-2 focus:ring-emerald-400 focus:border-emerald-400 bg-white/80"
                />
                <p class="text-[11px] text-emerald-600">
                  ถ้าไม่ระบุ ระบบจะคิดที่ 100 กรัม
                </p>
              </div>

              <div class="space-y-1.5">
                <span class="text-sm font-medium text-emerald-900">
                  มื้ออาหาร
                </span>
                <div
                  class="grid grid-cols-3 gap-2 text-[11px] sm:text-xs font-medium"
                >
                  <button
                    type="button"
                    data-meal="เช้า"
                    class="meal-btn pill px-2.5 py-1.5 bg-white border border-emerald-200 text-emerald-700 hover:bg-emerald-50"
                  >
                    เช้า
                  </button>
                  <button
                    type="button"
                    data-meal="กลางวัน"
                    class="meal-btn pill px-2.5 py-1.5 bg-white border border-emerald-200 text-emerald-700 hover:bg-emerald-50"
                  >
                    กลางวัน
                  </button>
                  <button
                    type="button"
                    data-meal="เย็น"
                    class="meal-btn pill px-2.5 py-1.5 bg-white border border-emerald-200 text-emerald-700 hover:bg-emerald-50"
                  >
                    เย็น
                  </button>
                </div>
              </div>
            </div>

            <!-- Upload area -->
            <div class="space-y-2">
              <span class="text-sm font-medium text-emerald-900">
                อัปโหลดภาพอาหาร
              </span>
              <label
                for="food-image"
                class="flex flex-col items-center justify-center gap-2 border-2 border-dashed border-emerald-200 bg-white/80 hover:bg-emerald-50 transition rounded-2xl px-4 py-5 cursor-pointer"
              >
                <div
                  class="w-10 h-10 flex items-center justify-center rounded-2xl bg-emerald-50 text-2xl"
                >
                  📷
                </div>
                <div class="text-center">
                  <p class="text-sm font-medium text-emerald-900">
                    แตะเพื่อเลือกภาพจากเครื่อง
                  </p>
                  <p class="text-xs text-emerald-600">
                    รองรับไฟล์ .jpg, .png ขนาดไม่เกิน ~5MB
                  </p>
                </div>
                <span
                  id="file-name"
                  class="text-[11px] text-emerald-700 mt-1"
                ></span>
              </label>
              <input
                id="food-image"
                type="file"
                accept="image/*"
                class="hidden"
              />
              <p class="text-[11px] text-emerald-500">
                * ตัวอย่างนี้เป็นการจำลองผลลัพธ์ สามารถเชื่อมต่อ AI
                หรือฐานข้อมูลโภชนาการจริงเพิ่มเติมได้ภายหลัง
              </p>
            </div>

            <!-- Preview -->
            <div id="preview-wrapper" class="hidden">
              <p class="text-xs font-medium text-emerald-900 mb-1.5">
                ตัวอย่างภาพที่เลือก
              </p>
              <img
                id="preview-image"
                alt="Food preview"
                class="w-full rounded-2xl border border-emerald-200/70 object-cover max-h-48"
              />
            </div>

            <!-- Button -->
            <button
              id="analyze-btn"
              class="w-full mt-2 inline-flex items-center justify-center gap-2 rounded-2xl bg-gradient-to-r from-emerald-500 to-lime-500 text-white font-semibold text-sm py-3.5 shadow-lg hover:shadow-xl hover:from-emerald-600 hover:to-lime-500 focus:outline-none focus:ring-2 focus:ring-emerald-400 focus:ring-offset-2 focus:ring-offset-emerald-50"
            >
              🔍 วิเคราะห์โภชนาการ
            </button>
          </section>

          <!-- RIGHT: Result Panel -->
          <section class="space-y-4 sm:space-y-5">
            <div
              class="bg-emerald-900 text-emerald-50 rounded-2xl p-4 sm:p-5 flex flex-col gap-3"
            >
              <div class="flex justify-between items-start gap-3">
                <div>
                  <h2 class="font-semibold text-lg">
                    ผลวิเคราะห์โภชนาการโดยประมาณ
                  </h2>
                  <p class="text-xs sm:text-sm text-emerald-100/80">
                    ใช้เพื่อการเรียนรู้เท่านั้น ไม่ใช่ข้อมูลทางการแพทย์
                  </p>
                </div>
                <div
                  id="meal-tag"
                  class="pill px-3 py-1 text-xs bg-emerald-800/80 border border-emerald-700/80"
                >
                  มื้อ: -
                </div>
              </div>

              <div class="flex items-center gap-4 mt-1">
                <div
                  class="w-16 h-16 rounded-2xl bg-emerald-800/80 flex flex-col items-center justify-center text-center"
                >
                  <span class="text-[11px] text-emerald-200">พลังงาน</span>
                  <span
                    id="calories"
                    class="text-xl font-semibold text-emerald-50"
                    >0</span
                  >
                  <span class="text-[11px] text-emerald-200">kcal</span>
                </div>
                <div class="flex-1 grid grid-cols-3 gap-2 text-xs">
                  <div
                    class="bg-emerald-800/70 rounded-xl p-2 flex flex-col gap-1"
                  >
                    <span class="text-emerald-200/90">โปรตีน</span>
                    <strong id="protein" class="text-emerald-50">0 g</strong>
                    <div class="w-full h-1.5 bg-emerald-950 rounded-full">
                      <div
                        id="protein-bar"
                        class="h-1.5 rounded-full bg-emerald-400"
                        style="width: 0%"
                      ></div>
                    </div>
                  </div>
                  <div
                    class="bg-emerald-800/70 rounded-xl p-2 flex flex-col gap-1"
                  >
                    <span class="text-emerald-200/90">คาร์โบไฮเดรต</span>
                    <strong id="carbs" class="text-emerald-50">0 g</strong>
                    <div class="w-full h-1.5 bg-emerald-950 rounded-full">
                      <div
                        id="carbs-bar"
                        class="h-1.5 rounded-full bg-lime-400"
                        style="width: 0%"
                      ></div>
                    </div>
                  </div>
                  <div
                    class="bg-emerald-800/70 rounded-xl p-2 flex flex-col gap-1"
                  >
                    <span class="text-emerald-200/90">ไขมัน</span>
                    <strong id="fat" class="text-emerald-50">0 g</strong>
                    <div class="w-full h-1.5 bg-emerald-950 rounded-full">
                      <div
                        id="fat-bar"
                        class="h-1.5 rounded-full bg-emerald-300"
                        style="width: 0%"
                      ></div>
                    </div>
                  </div>
                </div>
              </div>

              <p id="summary" class="text-[11px] sm:text-xs text-emerald-100/90">
                กรอกชื่ออาหาร ปริมาณ และอัปโหลดรูป จากนั้นกด
                “วิเคราะห์โภชนาการ” เพื่อดูรายละเอียดโดยประมาณ
              </p>
            </div>

            <!-- Vitamins & Minerals -->
            <div
              class="bg-white rounded-2xl border border-emerald-100 p-4 sm:p-5 space-y-3"
            >
              <h3 class="font-semibold text-emerald-900 text-sm flex gap-2">
                🧬 วิตามิน & แร่ธาตุโดยประมาณ
              </h3>
              <div class="grid grid-cols-1 sm:grid-cols-2 gap-3 text-xs">
                <div>
                  <p class="text-[11px] text-emerald-600 mb-1.5">
                    กลุ่มวิตามินที่มักพบ
                  </p>
                  <div
                    id="vitamins"
                    class="flex flex-wrap gap-1.5 text-[11px]"
                  ></div>
                </div>
                <div>
                  <p class="text-[11px] text-emerald-600 mb-1.5">
                    แร่ธาตุที่มักพบ
                  </p>
                  <div
                    id="minerals"
                    class="flex flex-wrap gap-1.5 text-[11px]"
                  ></div>
                </div>
              </div>
              <p class="text-[11px] text-emerald-500">
                * ข้อมูลชุดนี้เป็นค่าประมาณจากประเภทอาหาร
                สามารถเชื่อมต่อฐานข้อมูลโภชนาการจริง เช่น USDA / Thai Food
                Composition Database ในเวอร์ชันถัดไป
              </p>
            </div>

            <!-- Tips -->
            <div
              class="bg-emerald-50 rounded-2xl border border-emerald-100 p-4 sm:p-5 text-xs space-y-2"
            >
              <h3 class="font-semibold text-emerald-900 flex gap-2">
                💡 เคล็ดลับการใช้ Nutriton Scan เพื่อการเรียนรู้
              </h3>
              <ul class="list-disc list-inside text-emerald-800 space-y-1">
                <li>
                  ใช้ให้นักเรียนลองสแกนอาหารในชีวิตประจำวัน
                  แล้วสะท้อนการเลือกอาหารของตนเอง
                </li>
                <li>
                  เปรียบเทียบเมนูเดียวกันแต่ปริมาณต่างกัน
                  เพื่อเห็นผลของ “portion size” ต่อพลังงานและสารอาหาร
                </li>
                <li>
                  ต่อยอดเชื่อมต่อกับ AI / API
                  เพื่อให้ระบบเรียนรู้ภาพอาหารจากกล้องได้จริง
                </li>
              </ul>
            </div>
          </section>
        </div>
      </div>
    </div>

    <script>
      // โปรไฟล์ตัวอย่าง (ต่อ 100 กรัม) – เป็นค่าประมาณง่าย ๆ
      const FOOD_PROFILES = [
        {
          name: "ข้าวขาว",
          keywords: ["ข้าวขาว", "ข้าวสวย", "rice", "plain rice"],
          energy: 130,
          protein: 2.4,
          carbs: 28,
          fat: 0.3,
          vitamins: ["วิตามินบี1", "วิตามินบี3"],
          minerals: ["แมงกานีส", "เหล็ก"],
        },
        {
          name: "ไก่ย่าง",
          keywords: ["ไก่ย่าง", "ไก่", "chicken", "grilled chicken"],
          energy: 165,
          protein: 31,
          carbs: 0,
          fat: 3.6,
          vitamins: ["วิตามินบี6", "วิตามินบี12"],
          minerals: ["ฟอสฟอรัส", "ซีลีเนียม"],
        },
        {
          name: "ส้มตำไทย",
          keywords: ["ส้มตำ", "somtum", "papaya salad"],
          energy: 90,
          protein: 2.5,
          carbs: 15,
          fat: 2,
          vitamins: ["วิตามินเอ", "วิตามินซี"],
          minerals: ["โพแทสเซียม"],
        },
        {
          name: "นมจืด",
          keywords: ["นม", "นมจืด", "milk"],
          energy: 64,
          protein: 3.4,
          carbs: 5,
          fat: 3.5,
          vitamins: ["วิตามินบี2", "วิตามินดี"],
          minerals: ["แคลเซียม", "ฟอสฟอรัส"],
        },
        {
          name: "ขนมปังโฮลวีต",
          keywords: ["โฮลวีต", "whole wheat", "ขนมปัง"],
          energy: 247,
          protein: 13,
          carbs: 41,
          fat: 4.2,
          vitamins: ["วิตามินบี1", "โฟเลต"],
          minerals: ["แมกนีเซียม", "สังกะสี"],
        },
        {
          name: "เมนูทั่วไป",
          keywords: [],
          energy: 160,
          protein: 6,
          carbs: 22,
          fat: 5,
          vitamins: ["วิตามินบีรวม (โดยประมาณ)"],
          minerals: ["โซเดียม", "โพแทสเซียม"],
        },
      ];

      const el = (id) => document.getElementById(id);

      const caloriesEl = el("calories");
      const proteinEl = el("protein");
      const carbsEl = el("carbs");
      const fatEl = el("fat");
      const proteinBar = el("protein-bar");
      const carbsBar = el("carbs-bar");
      const fatBar = el("fat-bar");
      const vitaminsEl = el("vitamins");
      const mineralsEl = el("minerals");
      const summaryEl = el("summary");
      const mealTagEl = el("meal-tag");

      const mealButtons = document.querySelectorAll(".meal-btn");
      let currentMeal = "-";

      mealButtons.forEach((btn) => {
        btn.addEventListener("click", () => {
          mealButtons.forEach((b) =>
            b.classList.remove("bg-emerald-600", "text-white")
          );
          mealButtons.forEach((b) =>
            b.classList.add("bg-white", "text-emerald-700")
          );

          btn.classList.remove("bg-white", "text-emerald-700");
          btn.classList.add("bg-emerald-600", "text-white");

          currentMeal = btn.getAttribute("data-meal");
          mealTagEl.textContent = "มื้อ: " + currentMeal;
        });
      });

      // เลือกไฟล์ภาพ
      const fileInput = el("food-image");
      const fileNameEl = el("file-name");
      const previewWrapper = el("preview-wrapper");
      const previewImage = el("preview-image");

      fileInput.addEventListener("change", (e) => {
        const file = e.target.files[0];
        if (!file) {
          fileNameEl.textContent = "";
          previewWrapper.classList.add("hidden");
          return;
        }

        fileNameEl.textContent = "ไฟล์ที่เลือก: " + file.name;

        const reader = new FileReader();
        reader.onload = (event) => {
          previewImage.src = event.target.result;
          previewWrapper.classList.remove("hidden");
        };
        reader.readAsDataURL(file);
      });

      // ฟังก์ชันค้นหาโปรไฟล์อาหาร
      function findFoodProfile(foodName) {
        const name = (foodName || "").toLowerCase().trim();
        if (!name) {
          return FOOD_PROFILES[FOOD_PROFILES.length - 1]; // เมนูทั่วไป
        }
        for (const profile of FOOD_PROFILES) {
          if (
            profile.keywords.some((kw) =>
              name.includes(kw.toLowerCase().trim())
            )
          ) {
            return profile;
          }
        }
        return FOOD_PROFILES[FOOD_PROFILES.length - 1];
      }

      // แสดงผลวิตามิน / แร่ธาตุ
      function renderPills(container, items) {
        container.innerHTML = "";
        if (!items || !items.length) {
          container.innerHTML =
            '<span class="pill px-2.5 py-1 bg-emerald-50 text-emerald-700 border border-emerald-100">ไม่มีข้อมูล</span>';
          return;
        }
        items.forEach((item) => {
          const span = document.createElement("span");
          span.className =
            "pill px-2.5 py-1 bg-emerald-50 text-emerald-700 border border-emerald-100";
          span.textContent = item;
          container.appendChild(span);
        });
      }

      // คำนวณและอัปเดตแถบ progress
      function updateMacroBars(p, c, f) {
        const maxVal = Math.max(p, c, f, 1);
        proteinBar.style.width = Math.round((p / maxVal) * 100) + "%";
        carbsBar.style.width = Math.round((c / maxVal) * 100) + "%";
        fatBar.style.width = Math.round((f / maxVal) * 100) + "%";
      }

      // วิเคราะห์โภชนาการ (จำลอง)
      function analyzeFood() {
        const foodName = el("food-name").value;
        const portion = parseFloat(el("portion").value) || 100;
        const profile = findFoodProfile(foodName);

        const factor = portion / 100;
        const energy = Math.round(profile.energy * factor);
        const protein = +(profile.protein * factor).toFixed(1);
        const carbs = +(profile.carbs * factor).toFixed(1);
        const fat = +(profile.fat * factor).toFixed(1);

        caloriesEl.textContent = energy;
        proteinEl.textContent = protein + " g";
        carbsEl.textContent = carbs + " g";
        fatEl.textContent = fat + " g";

        updateMacroBars(protein, carbs, fat);
        renderPills(vitaminsEl, profile.vitamins);
        renderPills(mineralsEl, profile.minerals);

        const displayName = foodName?.trim()
          ? `"${foodName.trim()}"`
          : profile.name;

        summaryEl.textContent =
          "ผลลัพธ์โดยประมาณสำหรับ " +
          displayName +
          " ปริมาณ " +
          portion +
          " กรัม" +
          (currentMeal !== "-" ? " (มื้อ " + currentMeal + ")" : "") +
          " • พลังงานรวมประมาณ " +
          energy +
          " kcal • โปรตีน " +
          protein +
          " g • คาร์โบไฮเดรต " +
          carbs +
          " g • ไขมัน " +
          fat +
          " g. ใช้เพื่อการเรียนรู้และการตระหนักรู้ด้านโภชนาการเท่านั้น ไม่ใช่คำแนะนำทางการแพทย์.";
      }

      document
        .getElementById("analyze-btn")
        .addEventListener("click", analyzeFood);
    </script>
  </body>
</html>
