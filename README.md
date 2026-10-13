# Task-13-NumPy-Random-Sampling

**Internship:** Data Science Intern at Veda Technology  
**Task:** Day 13 of 45

## Objective
Practice generating random numbers and selecting random samples using NumPy. Learn how a random seed helps make results reproducible.

## Tools Used
- Python
- NumPy
- Google Colab or Jupyter Notebook

## 1. Import NumPy
```python
import numpy as np

print("NumPy version:", np.__version__)
```

## 2. Generate Random Integers
```python
random_numbers = np.random.randint(1, 101, size=10)
print("Random integers:", random_numbers)
```
Generates 10 random integers from 1 through 100.

## 3. Generate Random Floating-Point Numbers
```python
random_floats = np.random.rand(5)
print("Random floating-point numbers:", random_floats)
```
Generates five decimal values in the range `[0, 1)`.

## 4. Reproducibility with a Random Seed
```python
np.random.seed(42)
numbers1 = np.random.randint(1, 101, size=5)
print("First result:", numbers1)

np.random.seed(42)
numbers2 = np.random.randint(1, 101, size=5)
print("Second result:", numbers2)
```
Resetting the same seed before generating values reproduces the same sequence.

## 5. Random Sampling from an Array
```python
students = np.array([
    "Ravi", "Priya", "Arjun", "Sneha",
    "Kiran", "Anu", "Rahul", "Divya"
])

sample = np.random.choice(students, size=3, replace=False)
print("Random sample:", sample)
```
`np.random.choice()` selects random items. `replace=False` prevents selecting the same item more than once in this sample.

## 6. Create a Simulated Student Marks Dataset
```python
np.random.seed(42)

student_names = [
    "Ravi", "Priya", "Arjun", "Sneha", "Kiran",
    "Anu", "Rahul", "Divya", "Manoj", "Sita"
]

marks = np.random.randint(35, 101, size=10)

student_data = {
    "Name": student_names,
    "Marks": marks
}

for name, mark in zip(student_data["Name"], student_data["Marks"]):
    print(f"{name}: {mark}")
```
Creates sample marks between 35 and 100 for ten students.

## 7. Sample Marks and Calculate Their Average
```python
sample_marks = np.random.choice(marks, size=4, replace=False)

print("All marks:", marks)
print("Randomly selected marks:", sample_marks)
print("Average of sampled marks:", np.mean(sample_marks))
```

## Key Concepts Learned
- `np.random.randint()` generates random integers.
- `np.random.rand()` generates floating-point values in the range `[0, 1)`.
- `np.random.seed()` helps reproduce random sequences.
- `np.random.choice()` selects random elements from an array.
- `replace=False` samples without replacement.
- `np.mean()` calculates the average.

## How to Run
1. Open Google Colab or Jupyter Notebook.
2. Create a Python notebook.
3. Run the code examples in order.
4. Save your notebook as `numpy_random_sampling.ipynb`.

## Interview Questions
1. What is NumPy?
2. What is random sampling?
3. What is the difference between `randint()` and `rand()`?
4. Why is a random seed useful?
5. What does `np.random.choice()` do?
6. What is the difference between sampling with and without replacement?

---
Completed as part of the Data Science Internship at Veda Technology.
