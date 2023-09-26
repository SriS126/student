---
toc: true
comments: false
layout: post
title: Image Player
description: Play around with images here!
type: hacks
courses: { compsci: {week: 3} }
---

    import tkinter as tk
    from tkinter import ttk
    from PIL import Image, ImageTk
    import random

# Function to create a random image
    def create_random_image():
    width, height = 400, 400
    image = Image.new("RGB", (width, height))
    pixels = image.load()

    for x in range(width):
        for y in range(height):
            r = random.randint(0, 255)
            g = random.randint(0, 255)
            b = random.randint(0, 255)
            pixels[x, y] = (r, g, b)

    return ImageTk.PhotoImage(image)

# Function to update the image colors based on slider values
    def update_image():
    red = red_slider.get()
    green = green_slider.get()
    blue = blue_slider.get()

    new_image = Image.new("RGB", (400, 400), (red, green, blue))
    canvas.image = ImageTk.PhotoImage(new_image)
    canvas.create_image(0, 0, anchor=tk.NW, image=canvas.image)

# Create the main window
    root = tk.Tk()
    root.title("Colorful Image Generator")

# Create a canvas to display the image
    canvas = tk.Canvas(root, width=400, height=400)
    canvas.pack()

# Create sliders for red, green, and blue channels
    red_slider = ttk.Scale(root, from_=0, to=255, orient=tk.HORIZONTAL, label="Red")
    green_slider = ttk.Scale(root, from_=0, to=255, orient=tk.HORIZONTAL, label="Green")
    blue_slider = ttk.Scale(root, from_=0, to=255, orient=tk.HORIZONTAL, label="Blue")

# Create a button to update the image
    update_button = ttk.Button(root, text="Update Image", command=update_image)

# Create a random image initially
    canvas.image = create_random_image()
    canvas.create_image(0, 0, anchor=tk.NW, image=canvas.image)

# Place widgets in the window
    red_slider.pack()
    green_slider.pack()
    blue_slider.pack()
    update_button.pack()

# Set initial slider values
    red_slider.set(128)
    green_slider.set(128)
    blue_slider.set(128)

# Start the main loop
    root.mainloop()