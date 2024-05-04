- 👋 Hi, I’m @eelliiuuss
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

# python 
import turtle

def draw_tree(name):
    # Set up the Turtle
    window = turtle.Screen()
    window.bgcolor("black")
    tree = turtle.Turtle()
    tree.color("orange")
    tree.speed(200)
    tree.left(90)
    tree.penup()
    tree.backward(100)
    tree.pendown()

    # Function to draw fractal tree
    def draw_branch(branch_length, level):
        if level == 0:
            return
        tree.pensize(level)
        tree.forward(branch_length)
        tree.right(30)
        draw_branch(branch_length * 0.8, level - 1)
        tree.left(60)
        draw_branch(branch_length * 0.8, level - 1)
        tree.right(30)
        tree.backward(branch_length)

    # Draw the fractal tree
    draw_branch(150, 10)

    # Write the name at the bottom
    tree.penup()
    tree.color("orange")
    tree.goto(0, -300)
    tree.write(name, align="center", font=("Courier", 20, "normal"))

    tree.hideturtle()
    window.mainloop()

# Call the function with the desired name
draw_tree("Md:Elius parvez")




<!---
eelliiuuss/eelliiuuss is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
