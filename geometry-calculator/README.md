# Geometry Calculator

A simple Python calculator to compute the area of **circles** and **rectangles** with interactive user input and robust error handling.

## Features

- Calculate the **area of a circle** given its radius.
- Calculate the **area of a rectangle** given its length and width.
- Handles **negative inputs** gracefully with error messages.
- Catches **non-numeric input** and informs the user.

## Usage

1. Run the script:

```bash
python geometry_calculator.py
```

2. Enter the shape you want to calculate: circle or rectangle.

3. Provide the required numeric inputs (radius, length, width).

4. The program will display the area rounded to 2 decimal places.

### Example

Which shape do you want to calculate the area for? **circle**
Enter the radius of the circle: **5**
**The area of the circle with radius 5.0 = 78.54**

Which shape do you want to calculate the area for? **rectangle**
Enter the length of the rectangle: **10**
Enter the width of the rectangle: **6**
The area of the rectangle with length 10.0 and width 6.0 = **60.00**

---

## 🔀 Git Workflow (Step-by-Step)
This project demonstrates a Git workflow using branching and stashing:

1. **Create a new branch for Circle Area feature**
   ```bash
   git checkout -b feature/circle-area
   ```

2. **Work on the circle area feature and stash changes**
   ```bash
   git stash
   git status  # Verify working directory is clean
   ```

3. **Create a new branch for Rectangle Area feature**
   ```bash
   git checkout -b feature/rectangle-area
   ```

4. **Work on the rectangle area feature and stash changes**
   ```bash
   git stash
   git status
   ```

5. **Switch back to Circle Area branch and retrieve stashed changes**
   ```bash
   git checkout feature/circle-area
   git stash pop
   ```

6. **Complete the circle feature, commit, and push**
   ```bash
   git add geometry_calculator.py
   git commit -m "Implemented circle area feature"
   git push origin feature/circle-area
   ```

7. **Switch back to Rectangle Area branch and retrieve stashed changes**
   ```bash
   git checkout feature/rectangle-area
   git stash pop
   ```

8. **Complete the rectangle feature, commit, and push**
   ```bash
   git add geometry_calculator.py
   git commit -m "Implemented rectangle area feature"
   git push origin feature/rectangle-area
   ```

9. **Create Pull Requests**
   - Create PRs from both feature branches to the `dev` branch.

10. **Review and Merge**
    - After approval, merge into `dev` and then into `main`.
