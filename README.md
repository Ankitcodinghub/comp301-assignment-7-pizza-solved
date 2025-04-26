# comp301-assignment-7-pizza-solved
**TO GET THIS SOLUTION VISIT:** [Comp301 Assignment 7-pizza Solved](https://www.ankitcodinghub.com/product/comp301-a07-pizza-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;131797&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Comp301 Assignment 7-pizza Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
In this assignment, you’ll use the creational design patterns singleton, multiton, and factory method to control instantiation of some classes.

Imagine the process of ordering a pizza at a local pizza shop. What information does a customer need to provide so that they get the pizza they want?

1. What size should the pizza be?

2. What kind of crust should the pizza have?

3. What kind of cheese should be used?

4. What kind of sauce should be used?

5. What toppings should go on the pizza?

This assignment revolves around designing a series of classes that model the process of ordering pizza. In novice, you’ll create classes to represent the ingredients that go in a pizza. In adept, you’ll create a class to represent a pizza. And in jedi, you’ll create factory methods which are responsible for creating different pizza objects.

Novice

Let’s start by designing some classes to model pizza ingredients.

IngredientImpl

Check out the Ingredient interface. An ingredient is an object that encapsulates the following information:

1. The name of the ingredient, which is a string value.

2. A boolean value representing whether the ingredient is vegetarian or not.

3. A boolean value representing whether the ingredient is vegan or not.

Make a new class, IngredientImpl, which implements the Ingredient interface and encapsulates the above information. The

IngredientImpl class should be immutable. Add a suitable constructor to initialize the encapsulated fields using initial values passed in as parameter values.

Note: The order or type of the constructor’s parameters don’t matter to the autograder

Next, we’re going to create special subclasses of IngredientImpl to represent four different categories of pizza ingredients: crust, sauce, cheese, and toppings.

Crust

Create a new subclass of IngredientImpl, called Crust. This new class will use a variant of the multiton design pattern, so give it a private constructor.

Now let’s create and store a few Crust instances inside the Crust class. The instances we create will represent the different types of pizza crust that are available at the pizza shop. The pizza shop offers customers their choice of three types of crust:

| name | is vegetarian? | is vegan? | field name | |————-|—————-|———–|————-| | hand-tossed | yes | yes |

HAND_TOSSED | | thin | yes | yes | THIN | | deep dish | yes | yes | DEEP_DISH |

Using the field names and data values listed above, add three public static final fields to the Crust class. These fields will store references to the three types of crust offered by the pizza shop. For example, one of the field declarations might look like this:

java public static final Crust HAND_TOSSED = new Crust(“hand-tossed”, true, true);

Note: Your Crust constructor arguments might be different, depending on how you wrote the constructor

In accordance with the singleton and multiton design patterns, we would traditionally mark the HAND_TOSSED, THIN, and DEEP_DISH fields private, and expose them through a static factory method. However, since Crust instances are immutable, and the fields in question are final, it’s okay to expose them directly as constant values by simply assigning them the public access modifier.

Sauce

Add another subclass of IngredientImpl, called Sauce. This new class will be similar to Crust, except it represents the pizza sauce choices offered by the pizza shop.

Make the constructor of Sauce private, and include public static final Sauce fields for the following sauce options:

| name | is vegetarian? | is vegan? | field name | |————-|—————-|———–|————-| | tomato | yes | yes | TOMATO | | barbecue

| yes | yes | BARBECUE | | pesto | yes | yes | PESTO | | alfredo | yes | no | ALFREDO | | ranch | yes | no | RANCH |

Cheese

Add another subclass of IngredientImpl, called Cheese. This new class will be similar to Crust and Sauce, except it represents the pizza cheese choices offered by the pizza shop.

Make the constructor of Cheese private, and include public static final Cheese fields for the following cheese options:

| name | is vegetarian? | is vegan? | field name | |————-|—————-|———–|————-| | mozzarella | yes | no | MOZZARELLA | | blend | yes | no | BLEND | | vegan | yes | yes | VEGAN |

Topping

Finally, add one more subclass of IngredientImpl, called Topping. This new class will be similar to Crust, Sauce, and Cheese, except it represents the pizza topping choices offered by the pizza shop.

Make the constructor of Topping private, and include public static final Topping fields for the following toppings:

| name | is vegetarian? | is vegan? | field name | |——————|—————-|———–|——————| | tomato | yes | yes | TOMATO | | garlic | yes | yes | GARLIC | | mushrooms | yes | yes | MUSHROOMS | | pineapple | yes | yes | PINEAPPLE | | olives | yes | yes | OLIVES | | green pepper | yes | yes | GREEN_PEPPER | | spinach | yes | yes | SPINACH | | onion | yes | yes | ONION | | jalapeno | yes | yes | JALAPENO | | sun-dried tomato | yes | yes | SUN_DRIED_TOMATO | | pepperoni | no | no | PEPPERONI | | ground beef | no | no | GROUND_BEEF | | sausage | no | no | SAUSAGE | | bacon | no | no | BACON | | buffalo chicken | no | no | BUFFALO_CHICKEN | | ham | no | no | HAM | | anchovies | no | no | ANCHOVIES |

Adept

Now it’s time to create a class to represent a pizza.

PizzaImpl

Start by taking a look at the Pizza interface. A pizza is an object that encapsulates the following information:

1. The size of the pizza (either small, medium, or large), represented by a Size enum field

2. The type of crust on the pizza, represented by a Crust instance

3. The type of sauce on the pizza, represented by a Sauce instance

4. The type of cheese on the pizza, represented by a Cheese instance

5. The toppings on the pizza, represented by a Topping list or array

Make a new class, PizzaImpl, which implements the Pizza interface and encapsulates the above information. The PizzaImpl class should be immutable. Add a suitable constructor to initialize the encapsulated fields using initial values passed in as parameter values.

Note: The order or type of the constructor’s parameters don’t matter to the autograder

Most of the Pizza methods should be self-explanatory in terms of implementation. One exception, however, is getPrice(). The getPrice() method should be a derived getter which calculates and returns the price of the pizza as a double value based on the pizza size and number of toppings.

If the pizza is small, its price should be $7.00 plus $0.25 per topping. If it is medium, its price should be $9.00 plus $0.50 per topping. If it is large, its price should be $11.00 plus $0.75 per topping.

Jedi

The last step of the assignment is to write a series of static factory methods which will instantiate special types of pizza.

Add a new class, PizzaFactory, to your project. PizzaFactory will contain the factory methods that handle pizza instantiation.

inside the PizzaFactory class, add the following factory methods.

Cheese pizza

Add a factory method to the PizzaFactory class to instantiate a cheese pizza. The factory method should have the following signature:

java public static Pizza makeCheesePizza(Size size) { // Your code here }

The factory method should create and return a new Pizza instance with hand-tossed crust, tomato sauce, cheese blend, and no toppings. The returned Pizza object should also have the correct size as specified by the method’s parameter.

Hawaiian pizza

Add a factory method to the PizzaFactory class to instantiate a Hawaiian pizza. The factory method should have the following signature:

java public static Pizza makeHawaiianPizza(Size size) { // Your code here }

The factory method should create and return a new Pizza instance with hand-tossed crust, tomato sauce, cheese blend, and two toppings: ham and pineapple. The returned Pizza object should also have the correct size as specified by the method’s parameter.

Meat lover’s pizza

Add a factory method to the PizzaFactory class to instantiate a meat lover’s pizza. The factory method should have the following signature:

java public static Pizza makeMeatLoversPizza(Size size) { // Your code here }

The factory method should create and return a new Pizza instance with deep-dish crust, tomato sauce, cheese blend, and four toppings:

pepperoni, sausage, bacon, and ground beef. The returned Pizza object should also have the correct size as specified by the method’s parameter.

Veggie supreme pizza

Add a factory method to the PizzaFactory class to instantiate a veggie supreme pizza. The factory method should have the following signature:

java public static Pizza makeVeggieSupremePizza(Size size) { // Your code here }

The factory method should create and return a new Pizza instance with thin crust, tomato sauce, cheese blend, and four toppings: sun-dried tomato, green peppers, mushrooms, and olives. The returned Pizza object should also have the correct size as specified by the method’s parameter.

Daily special pizza

Finally, add one more factory method to the PizzaFactory class to instantiate a daily special pizza. The factory method should have the following signature:

java public static Pizza makeDailySpecialPizza() { // Your code here }

The factory method should create and return a new Pizza instance, but this time you get to choose what type of pizza to create. Instantiate and return your favorite type of pizza! Notice that this time, there is no size parameter; this is because you get to choose what size to return.
