<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Recipe Generator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
            text-align: center;
        }

        header {
            background-color: #333;
            color: #fff;
            padding: 1em;
        }

        main {
            padding: 1em;
        }

        button {
            padding: 10px;
            font-size: 16px;
            cursor: pointer;
        }

        #recipe-output {
            margin-top: 20px;
            text-align: left;
        }
    </style>
</head>
<body>

    <header>
        <h1>Recipe Generator</h1>
    </header>

    <main>
        <button onclick="generateRecipe()">Generate Recipe</button>
        <div id="recipe-output"></div>
    </main>

    <script>
        function generateRecipe() {
            // In a real application, you would have a more sophisticated logic for generating recipes.
            const recipes = [
                "Spaghetti Bolognese",
                "Chicken Alfredo",
                "Vegetarian Stir Fry",
                "Margherita Pizza",
                "Grilled Salmon"
            ];

            const randomIndex = Math.floor(Math.random() * recipes.length);
            const randomRecipe = recipes[randomIndex];

            const recipeOutput = document.getElementById('recipe-output');
            recipeOutput.innerHTML = `<h2>Your Random Recipe:</h2><p>${randomRecipe}</p>`;
        }
    </script>

</body>
</html>
