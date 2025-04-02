# Zenith-EditZ
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Asset Editor</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100 flex items-center justify-center min-h-screen">
    <div class="bg-white shadow-lg rounded-xl p-6 w-full max-w-lg">
        <h2 class="text-2xl font-bold mb-4 text-gray-700">Edit Asset</h2>
        <div class="mb-4">
            <label class="block text-gray-600 text-sm font-medium mb-1">Asset Name</label>
            <input type="text" id="assetName" class="w-full p-2 border rounded-md focus:ring focus:ring-blue-300">
        </div>
        <div class="mb-4">
            <label class="block text-gray-600 text-sm font-medium mb-1">Asset Description</label>
            <textarea id="assetDesc" class="w-full p-2 border rounded-md focus:ring focus:ring-blue-300"></textarea>
        </div>
        <div class="mb-4">
            <label class="block text-gray-600 text-sm font-medium mb-1">Asset Value</label>
            <input type="number" id="assetValue" class="w-full p-2 border rounded-md focus:ring focus:ring-blue-300">
        </div>
        <button onclick="saveAsset()" class="bg-blue-600 text-white px-4 py-2 rounded-md w-full hover:bg-blue-700 transition">Save</button>
        <p id="status" class="mt-3 text-green-600 text-sm"></p>
    </div>

    <script>
        function saveAsset() {
            const name = document.getElementById("assetName").value;
            const desc = document.getElementById("assetDesc").value;
            const value = document.getElementById("assetValue").value;
            
            if (name && desc && value) {
                document.getElementById("status").innerText = "Asset saved successfully!";
            } else {
                document.getElementById("status").innerText = "Please fill all fields.";
                document.getElementById("status").classList.add("text-red-600");
            }
        }
    </script>
</body>
</html>
