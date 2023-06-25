# Chapter 22: Eating Out - Tips for Staying on Track with your Macros

Congratulations on reaching Chapter 22! By now, you've mastered the art of preparing delicious macro-friendly meals at home. But what happens when you're on the go, traveling, or simply don't have access to your own kitchen? Fear not, dear reader, for in this chapter, we will provide you with tips and tricks to stay on track with your macros when eating out.

We are honored to have Chris Powell, celebrity fitness trainer and TV host, join us as a special guest for this chapter. Chris has spent years in the fitness industry, helping countless individuals achieve their health and fitness goals. His expertise and wisdom will be invaluable in navigating the challenges of eating out while maintaining your macros.

In this chapter, you will learn:
- The importance of planning ahead
- How to deconstruct restaurant menus to fit your macros
- Strategies for making healthy choices when dining out
- Meal planning and prepping for travel
- And much more!

We believe that you can enjoy eating out without sacrificing your hard-earned progress in achieving your health and fitness goals. Let's get started with Chapter 22 and learn how to stay on track with our macros even when dining out.
# Chapter 22: Eating Out - Tips for Staying on Track with your Macros

Congratulations on reaching Chapter 22! By now, you've mastered the art of preparing delicious macro-friendly meals at home. But what happens when you're on the go, traveling, or simply don't have access to your own kitchen? Fear not, dear reader, for in this chapter, we will provide you with tips and tricks to stay on track with your macros when eating out.

We are honored to have Chris Powell, celebrity fitness trainer and TV host, join us as a special guest for this chapter. Chris has spent years in the fitness industry, helping countless individuals achieve their health and fitness goals. His expertise and wisdom will be invaluable in navigating the challenges of eating out while maintaining your macros.

## Tips for Eating Out While Staying on Track with Your Macros
Eating out can be tricky when it comes to sticking to your macros. The best way to stay on track is to plan ahead and make informed decisions.

### 1. Research the Menu Ahead of Time
Many restaurants now offer nutritional information on their websites, so take advantage of this and plan your meal ahead of time. Look for high protein options and low calorie sides. 

### 2. Be Mindful of Portions
Restaurant portions are often much larger than what you would typically eat at home. Consider sharing an entree or taking half of it home for later.

### 3. Make Substitutions
Don't be afraid to ask the server to make substitutions to fit your macros. For example, ask for extra veggies instead of fries or for sauces and dressings on the side.

### 4. Don't Skip Meals
Skipping meals to save calories or macros for later can often lead to overeating and poor food choices. Make sure to have a healthy snack before going out to eat or plan for a healthy meal afterwards.

### 5. Be Prepared for Travel
Travel can be a challenge when it comes to sticking to your macros. Plan ahead by packing healthy snacks and meals for the journey, and research restaurants at your destination ahead of time.

### 6. Choose High-Protein Options
Protein is essential in maintaining muscle mass and feeling full, so choose high-protein options such as lean meats, fish, and tofu.

### 7. Don't Be Afraid of Spices and Herbs
Using spices and fresh herbs can add flavor to your meal without adding calories or macros. Plus, many herbs and spices have health benefits!

## Conclusion
Eating out doesn't have to derail your macros or progress towards your health and fitness goals. With a bit of planning and mindfulness, you can still enjoy dining out while sticking to your macros. Thank you for joining us in Chapter 22, and a special thank you to Chris Powell for sharing his expertise and wisdom with us.
To ensure you're staying on track with your macros while eating out, it's helpful to have access to a food database that provides nutritional information for the meals you consume. There are several food databases available online or in the form of mobile applications that can help you access this information on-the-go.

One such food database is [Nutritionix](https://www.nutritionix.com/). With the Nutritionix API, you can access a wide range of nutritional information for almost any restaurant, brand, or food item. Here's some sample code in Python that shows how to use the Nutritionix API to retrieve nutritional information for a specific food item:

```python
import requests

# Replace YOUR_APP_ID and YOUR_APP_KEY with your own Nutritionix API credentials
APP_ID = 'YOUR_APP_ID'
APP_KEY = 'YOUR_APP_KEY'

# Set up the API endpoint and parameters
url = 'https://api.nutritionix.com/v1_1/search/'
params = {
    'appId': APP_ID,
    'appKey': APP_KEY,
    'query': 'chicken teriyaki',
    'fields': ['item_name', 'nf_calories', 'nf_total_fat', 'nf_protein']
}

# Make the API request and retrieve the nutritional information
response = requests.get(url, params=params)
data = response.json()

# Print out the nutritional information
for item in data['hits']:
    print('{}, {} cal, {} g fat, {} g protein'.format(
        item['fields']['item_name'],
        item['fields']['nf_calories'],
        item['fields']['nf_total_fat'],
        item['fields']['nf_protein']
    ))
```

In this sample code, we import the `requests` library to make HTTP requests to the Nutritionix API. We then set up the API endpoint and parameters, including our own Nutritionix API credentials (`APP_ID` and `APP_KEY`).

We then make the API request using `requests.get()` and retrieve the nutritional information for the specified query (in this case, "chicken teriyaki"). Finally, we print out the nutritional information for each hit that matches the query.

By using a food database and API like Nutritionix, you can access the nutritional information of almost any food item, making it easier to stay on track with your macros while eating out.


[Next Chapter](23_Chapter23.md)