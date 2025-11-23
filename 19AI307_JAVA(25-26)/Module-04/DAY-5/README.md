# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Design a program where a Product model stores item info, and the view displays it. Implement a controller to update product price and refresh the view automatically.

## AIM:
To implement the Model–View–Controller (MVC) design pattern where the Product model stores item information, the view displays product details, and the controller updates the product price and automatically refreshes the view.

## ALGORITHM :
1.Create the Product Model

-Store product name and price.

-Provide getters and setters.

2.Create the Product View

-Implement a method to display product name and price.

3.Create the Controller

-Hold references to both model and view.

-Update the product price using a setter.

-After updating, call the view to refresh the product details.

4.In the main method

-Create a product object with initial values.

-Create a view object.

-Create a controller object that connects model and view.

-Display initial product details.

-Update the price using the controller.

-Observe automatic refresh on the view.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Samyuktha S
RegisterNumber: 212222240089 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ProductManagementSystem {

    // ===== Model =====
    static class Product {
        private String name;
        private double price;
        private String code;

        public Product(String name, double price, String code) {
            this.name = name;
            this.price = price;
            this.code = code;
        }

        public String getName() {
            return name;
        }

        public double getPrice() {
            return price;
        }

        public String getCode() {
            return code;
        }

        public void setPrice(double price) {
            this.price = price;
        }
    }

    // ===== View =====
    static class ProductView {
        public void displayProduct(String name, double price, String code) {
            System.out.println("--- Product Details ---");
            System.out.println("Name : " + name);
            System.out.println("Price: " + price);
            System.out.println("Code : " + code);
        }
    }

    // ===== Controller =====
    static class ProductController {
        private Product product;
        private ProductView view;

        public ProductController(Product product, ProductView view) {
            this.product = product;
            this.view = view;
        }

        public void updateView() {
            view.displayProduct(product.getName(), product.getPrice(), product.getCode());
        }

        public void updatePrice(double newPrice) {
            product.setPrice(newPrice);
            updateView();
        }
    }

    // ===== Main Method =====
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name = sc.next();
        double price = sc.nextDouble();
        String code = sc.next();
        double newPrice = sc.nextDouble();

        Product product = new Product(name, price, code);
        ProductView view = new ProductView();
        ProductController controller = new ProductController(product, view);

        controller.updateView();
        controller.updatePrice(newPrice);

        sc.close();
    }
}

```

## OUTPUT:
<img width="626" height="321" alt="image" src="https://github.com/user-attachments/assets/d47dfee5-834d-4dc7-b763-1884ee113d22" />

## RESULT:
Thus, the MVC-based Java program was successfully developed where the controller updates the product price in the model, and the view automatically refreshes to display the updated information.
