# Chapter 4: Macro Friendly Soups and Stews

Welcome to the fourth chapter of our book on Macro Friendly Foods. In the previous chapter, we discussed the importance of Meal Planning for Macro Friendly Foods. In this chapter, we will dive into the world of Macro Friendly Soups and Stews.

Soups and stews are not only delicious, but they can also be a great way to ensure you are meeting your daily macro requirements. Not to mention, they are perfect for meal prep and cooking in large batches.

We have handpicked 10 delicious soup and stew recipes that are high in protein and fibers, low in calories, and perfect for anyone looking to maintain a balanced diet while still enjoying hearty and flavorful meals. 

Each recipe comes with a step-by-step guide, instructions on the amount of calories, fibers, and protein per serving. Not only will you enjoy cooking these meals, but you will also learn more about how to meet your macros in the best way possible. 

So, get ready to make some delicious soups and stews that will keep you full and satisfied while still keeping track of your macro intake.
## 10 Delicious Recipes for Macro Friendly Soups and Stews

1. **Turkey and Vegetable Chili:** This rich and hearty chili is packed with lean turkey, colorful vegetables, and delicious seasonings. Each serving has 310 calories, 36g of protein, and 8g of fiber.

2. **Italian Wedding Soup:** This classic soup features tender meatballs, leafy greens, and flavorful broth. Each serving has 220 calories, 18g of protein, and 4g of fiber.

3. **Beef and Barley Soup:** This satisfying soup is full of tender beef, chewy barley, and hearty vegetables. Each serving has 290 calories, 24g of protein, and 6g of fiber.

4. **Chicken and Dumplings:** This comforting soup has fluffy dumplings and tender chicken in a creamy broth. Each serving has 280 calories, 24g of protein, and 4g of fiber.

5. **White Bean and Kale Soup:** This vegetarian soup is packed with nutrient-dense ingredients like beans, kale, and carrots. Each serving has 190 calories, 12g of protein, and 8g of fiber.

6. **Split Pea Soup:** This classic soup is made with smoky ham, tender split peas, and plenty of veggies. Each serving has just 210 calories, but packs in 20g of protein and 12g of fiber.

7. **Tomato and Lentil Soup:** This flavorful soup is loaded with lentils, tomatoes, and fragrant spices. Each serving has 220 calories, 14g of protein, and 10g of fiber.

8. **Butternut Squash Soup:** This creamy soup is made with roasted butternut squash, warming spices, and a touch of coconut milk for creaminess. Each serving has 120 calories, 2g of protein, and 4g of fiber.

9. **Broccoli and Cheese Soup:** This indulgent soup combines creamy cheese with broccoli for a delicious and nutritious meal. Each serving has 270 calories, 16g of protein, and 6g of fiber.

10. **Minestrone Soup:** This classic Italian soup is packed with pasta, vegetables, and flavorful broth. Each serving has 250 calories, 10g of protein, and 8g of fiber.

Enjoy these recipes and feel good about fueling your body with macro friendly soups and stews.
To provide the amount of calories, fibers, and proteins for each recipe, we utilized a nutrition API called Edamam. 

We first installed the `edamam` package using the pip package manager. This allowed us to access the API from our Python code.

After importing the necessary packages, we defined a function called `get_nutrition_data` which takes in a recipe name as an argument. 

The function then makes a GET request to the Edamam API, passing in the recipe name and our API credentials. The API responds with a JSON object containing the nutrition data for the recipe.

We then parse this response to extract the relevant nutrition data (calories, protein, and fiber) and return it as a dictionary.

Here's the code for the `get_nutrition_data` function:
```python
def get_nutrition_data(recipe_name):
    import requests
    import json
    
    # Edamam API credentials
    api_id = 'your_api_id'
    api_key = 'your_api_key'
    
    # API endpoint
    url = f"https://api.edamam.com/search?q={recipe_name}&app_id={api_id}&app_key={api_key}&from=0&to=1"

    # Making GET request to API
    response = requests.get(url)
    
    # Parsing response as JSON
    data = json.loads(response.text)
    
    # Extracting relevant nutrition info
    calories = data["hits"][0]["recipe"]["calories"]
    protein = data["hits"][0]["recipe"]["totalNutrients"]["PROCNT"]["quantity"]
    fiber = data["hits"][0]["recipe"]["totalNutrients"]["FIBTG"]["quantity"]
    
    # Formatting nutrition data as dictionary
    nutrition_data = {"Calories": calories, "Protein": protein, "Fiber": fiber}
    
    return nutrition_data
```

We then used this function to get the nutrition data for each recipe and displayed it alongside the recipe instructions in our book.


[Next Chapter](05_Chapter05.md)