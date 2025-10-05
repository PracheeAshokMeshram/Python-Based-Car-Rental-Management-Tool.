# 🚗 Python-Based Car Rental Management Tool

## 📖 Introduction
The **Python-Based Car Rental Management Tool** is a beginner-friendly project designed to simulate a simple car rental system.  
It helps manage car availability, customer details, and rental transactions — all using **Python’s core data structures** like lists and dictionaries.  

This project is ideal for:
- Students learning Python fundamentals  
- Beginners exploring data management with functions  
- Mini-project submissions or portfolio demonstrations  

---

## 💡 Objective
The goal of this project is to provide a simple, console-based system that allows:
- Renting and returning cars  
- Keeping track of which customer rented which car  
- Managing rental fees and basic records  

---

## 🧠 Key Features

- 🚙 **Car Management:** Maintain a list of available cars with details such as make, model, and year.  
- 👥 **Customer Management:** Store customer details and track their rented cars.  
- 🔄 **Rental Operations:** Rent and return cars using simple functions.  
- 💰 **Rental Fee Tracking:** Record rental IDs and corresponding charges.  
- 📜 **Dynamic Updates:** Automatically update car availability when rented or returned.  
- 🧾 **Display Reports:** Print clear summaries of customer rentals and total transactions.  
- 🧩 **Code Simplicity:** Uses core Python only — no external dependencies.

---

## 🧩 System Architecture
The system is structured into three core data components:

| Component | Description | Example |
|------------|-------------|----------|
| **Cars** | Stores car details and availability | `{ 'car_id': 'C001', 'make': 'Toyota', 'model': 'Innova', 'year': 2022, 'available': True }` |
| **Customers** | Stores customer information and their rented cars | `{ 'customer_id': 'CU001', 'name': 'Adarsh', 'rented_cars': [] }` |
| **Rentals** | Stores rental transactions | `{ 'rental_id': 'R001', 'customer': customers[0], 'car': cars[0], 'rental_fee': 500.0 }` |

---

## ⚙️ Code Explanation

### 🔹 1. Car and Customer Initialization
```python
cars = [
    {'car_id': 'C001', 'make': 'Toyota', 'model': 'Innova', 'year': 2022, 'available': True},
    {'car_id': 'C002', 'make': 'Honda', 'model': 'Accord', 'year': 2022, 'available': True},
    {'car_id': 'C003', 'make': 'Maruti', 'model': 'Swift', 'year': 2022, 'available': True}
]
A list of dictionaries stores each car with its properties. Similarly, customers are initialized with unique IDs and names.

🔹 2. Renting a Car
python
Copy code
def rent_car(customer, car):
    if car['available']:
        car['available'] = False
        customer['rented_cars'].append(car)
        return True
    return False
Checks if a car is available; if yes, it marks it as rented and links it to the customer.

🔹 3. Returning a Car
python
Copy code
def return_car(customer, car):
    if car in customer['rented_cars']:
        car['available'] = True
        customer['rented_cars'].remove(car)
        return True
    return False
Updates the car’s availability status and removes it from the customer’s list.

🔹 4. Recording Rentals
python
Copy code
rentals.append({'rental_id': "R001", 'customer': customers[0], 'car': cars[0], 'rental_fee': 500.0})
Stores details of each rental in a separate list for easy tracking.

📊 Example Output

Adarsh's Rented Cars:['Toyota']
Minu's Rented Cars:['Honda']
Sonu's Rented Cars:['Maruti']

Adarsh's Updated Rented Cars:[]
Minu's Updated Rented Cars:['Honda']
Sonu's Updated Rented Cars:[]

Rental ID:R001,Customer:Adarsh,Car:Toyota,Rental Fee:INR500.0
Rental ID:R002,Customer:Minu,Car:Honda,Rental Fee:INR450.0
Rental ID:R003,Customer:Sonu,Car:Maruti,Rental Fee:INR350.0

🧠 Use Cases

🎓 Educational Use: Demonstrates basic data handling in Python.
🧑‍💻 Mini Project: Suitable for academic submissions.
🧰 Learning Reference: Great example for understanding Python dictionaries and lists.
⚙️ Foundation for Larger Projects: Can be extended to include file handling, user inputs, and GUIs.

🚀 Future Enhancements

🔸 Add user input for dynamic car/customer creation.
🔸 Save data to a file or database.
🔸 Implement a simple text-based or GUI interface.
🔸 Add rental duration and late fee calculation.
🔸 Generate summary reports or invoices.

🤝 Contribution
Contributions are welcome!
If you’d like to improve the system:
Fork the repo
Create a feature branch (feature-newfunction)
Commit your changes
Open a pull request

👩‍💻 Author :

Prachee A. Meshram
📧 prachee.ajm20@gmail.com
🔗 GitHub Profile - https://github.com/PracheeAshokMeshram
🔗 LinkedIn Profile- www.linkedin.com/in/prachee-a-meshram-975766296

🏁 Conclusion
The Python-Based Car Rental Management Tool is a compact yet effective example of how Python can be used to design simple management systems.
It reinforces programming fundamentals like:
Data organization
Functional logic
Real-world system modeling
Perfect for anyone starting their Python development journey!
