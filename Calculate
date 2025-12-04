<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Area & Volume Calculator</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    @keyframes fadeInScale {
      from {
        opacity: 0;
        transform: scale(0.8);
      }
      to {
        opacity: 1;
        transform: scale(1);
      }
    }
    .fade-in {
      animation: fadeInScale 0.6s ease-out;
    }
  </style>
</head>
     <!-- Background -->
    <body style="background: url(https://static.promediateknologi.id/crop/0x0:0x0/750x500/webp/photo/p1/294/2024/02/05/oliver-sykes-3158845937.jpg" 
      class="min-h-screen flex items-center justify-center p-6">
        
     <!-- Area Tengah -->   
    <div class="min-h-screen flex items-center justify-center">
    <div class="bg-white rounded-2xl shadow-2xl p-8 w-full max-w-md space-y-6">
      <div class="flex items-center justify-center gap-3 mb-8">
      <img src="https://upload.wikimedia.org/wikipedia/id/8/80/President_University.jpg" 
      class="h-12 w-12 rounded-full border-2 border-Black shadow-lg">

    </div>
    <h1 class="text-2xl font-bold text-center text-Black-700"> Area & Volume Calculator</h1>
    
    <!-- Pilih Bangun -->
    <div>
      <label class="block font-semibold mb-1">Choose Shape:</label>
      <select id="shape" onchange="showFields()" 
        class="w-full border rounded-lg px-3 py-2 focus:ring-2 focus:ring-indigo-400">
        <option value="">-- Select --</option>
        <option value="square">Square (Area)</option>
        <option value="circle">Circle (Area)</option>
        <option value="cube">Cube (Volume)</option>
        <option value="cuboid">Cuboid (Volume)</option>
        <option value="sphere">Sphere (Volume)</option>
      </select>
    </div>

    <!-- Ilustrasi -->
    <div id="illustration" class="flex justify-center"></div>

    <!-- Input Dinamis -->
    <div id="inputs" class="space-y-3"></div>

    <!-- Tombol Hitung -->
    <button onclick="calculate()" 
      class="w-full bg-blue-600 text-white py-3 rounded-lg font-semibold hover:bg-yellow-700 transition">
      Calculate
    </button>

    <!-- Hasil -->
    <div id="result" class="text-center text-lg font-bold text-green-700"></div>
  </div>

  <script>
    function showFields() {
      const shape = document.getElementById("shape").value;
      const inputs = document.getElementById("inputs");
      const illustration = document.getElementById("illustration");
      inputs.innerHTML = "";
      illustration.innerHTML = "";

      let img = "";
      if (shape === "square") {
        img = "https://static.stands4.com/images/symbol/1815_square.png";
        inputs.innerHTML = `
          <label>Side Length:</label>
          <input id="side" type="number" class="w-full border rounded-lg px-3 py-2" placeholder="Enter side length">
        `;
      } else if (shape === "circle") {
        img = "https://img.freepik.com/free-vector/stroke-round-geometric-shape-vector_53876-175080.jpg?semt=ais_hybrid&w=740&q=80";
        inputs.innerHTML = `
          <label>Radius:</label>
          <input id="radius" type="number" class="w-full border rounded-lg px-3 py-2" placeholder="Enter radius">
        `;
      } else if (shape === "cube") {
        img = "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTVr7g1BdkCZtkEwFb_XmjW76GsUU99oavnQoMQ6YA-j0J4ikDZXnKTrkNIj2OROEg7O_A&usqp=CAU";
        inputs.innerHTML = `
          <label>Side Length:</label>
          <input id="side" type="number" class="w-full border rounded-lg px-3 py-2" placeholder="Enter side length">
        `;
      } else if (shape === "cuboid") {
        img = "https://upload.wikimedia.org/wikipedia/commons/thumb/f/f0/Cuboid_simple.svg/200px-Cuboid_simple.svg.png";
        inputs.innerHTML = `
          <label>Length:</label>
          <input id="length" type="number" class="w-full border rounded-lg px-3 py-2" placeholder="Enter length">
          <label>Width:</label>
          <input id="width" type="number" class="w-full border rounded-lg px-3 py-2" placeholder="Enter width">
          <label>Height:</label>
          <input id="height" type="number" class="w-full border rounded-lg px-3 py-2" placeholder="Enter height">
        `;
      } else if (shape === "sphere") {
        img = "https://study.com/cimages/multimages/16/sphere7414877865953853223.png";
        inputs.innerHTML = `
          <label>Radius:</label>
          <input id="radius" type="number" class="w-full border rounded-lg px-3 py-2" placeholder="Enter radius">
        `;
      }

      if (img) {
        illustration.innerHTML = `<img src="${img}" class="h-28 fade-in">`;
      }
    }

    function calculate() {
      const shape = document.getElementById("shape").value;
      let result = "";

      if (shape === "square") {
        const side = parseFloat(document.getElementById("side").value);
        result = `Area of Square = ${side * side}`;
      } 
      else if (shape === "circle") {
        const radius = parseFloat(document.getElementById("radius").value);
        result = `Area of Circle = ${(Math.PI * radius * radius).toFixed(2)}`;
      } 
      else if (shape === "cube") {
        const side = parseFloat(document.getElementById("side").value);
        result = `Volume of Cube = ${Math.pow(side, 3)}`;
      } 
      else if (shape === "cuboid") {
        const length = parseFloat(document.getElementById("length").value);
        const width = parseFloat(document.getElementById("width").value);
        const height = parseFloat(document.getElementById("height").value);
        result = `Volume of Cuboid = ${length * width * height}`;
      } 
      else if (shape === "sphere") {
        const radius = parseFloat(document.getElementById("radius").value);
        result = `Volume of Sphere = ${((4/3) * Math.PI * Math.pow(radius, 3)).toFixed(2)}`;
      } 
      else {
        result = "⚠️ Please select a shape first.";
      }

      document.getElementById("result").innerText = result;
    }
  </script>
</body>
</html>
