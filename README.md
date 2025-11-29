<html lang="th">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>NutriScan AI - Food Analyzer</title>

    <!-- Tailwind -->
    <script src="https://cdn.tailwindcss.com"></script>

    <!-- ฟอนต์ Kanit -->
    <link
      href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600&display=swap"
      rel="stylesheet"
    />

    <style>
      body {
        font-family: "Kanit", sans-serif;
        background-color: #f0f9ff;
      }
    </style>

    <!-- importmap สำหรับ React / Lucide / Recharts / Gemini -->
    <script type="importmap">
      {
        "imports": {
          "lucide-react": "https://aistudiocdn.com/lucide-react@^0.555.0",
          "@google/genai": "https://aistudiocdn.com/@google/genai@^1.30.0",
          "recharts": "https://aistudiocdn.com/recharts@^3.5.1",
          "react-dom/": "https://aistudiocdn.com/react-dom@^19.2.0/",
          "react": "https://aistudiocdn.com/react@^19.2.0",
          "react/": "https://aistudiocdn.com/react@^19.2.0/"
        }
      }
    </script>

    <!-- ถ้ามีไฟล์ index.css ให้ใส่ไว้ใน repo เดียวกัน -->
    <link rel="stylesheet" href="/index.css" />
  </head>
  <body>
    <div id="root"></div>

    <!-- จุดเริ่มต้นของแอป React (index.tsx ในโปรเจกต์ของคุณ) -->
    <script type="module" src="/index.tsx"></script>
  </body>
</html>
