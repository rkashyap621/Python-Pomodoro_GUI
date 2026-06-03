import tkinter as tk
import math

# ---------------------------- CONSTANTS ------------------------------- #
PINK = "#e2979c"
RED = "#e7305b"
GREEN = "#9bdeac"
YELLOW = "#f7f5dd"
FONT_NAME = "Courier"
WORK_MIN = 25
SHORT_BREAK_MIN = 5
LONG_BREAK_MIN = 20
REPS = 8
DOWNTIMER = None
TICKS = ""

# ---------------------------- TIMER RESET ------------------------------- #

def reset_timer():
    global DOWNTIMER
    global TICKS
    global REPS
    window.after_cancel(DOWNTIMER)
    canvas.itemconfig(timer_text, text="00:00")
    title_label.config(text = "Timer")
    tick_label.config(text="")
    REPS = 8





# ---------------------------- TIMER MECHANISM ------------------------------- #
def start_timer():
    global REPS
    if REPS > 1 and REPS % 2 == 0:
        count_down(20)
        REPS -= 1
        title_label.config(text = "Work Timer", fg =GREEN)
    elif REPS > 1 and REPS % 2 == 1:
        count_down(10)
        REPS -= 1
        title_label.config(text="Short Break Timer", fg = PINK)
    else:
        count_down(30)
        REPS -= 1
        title_label.config(text="Long Break Timer", fg = RED)


# ---------------------------- COUNTDOWN MECHANISM ------------------------------- #
def count_down(count):
    global REPS
    global DOWNTIMER
    global TICKS
    count_min = math.floor(count / 60)
    count_sec = count % 60
    if count_sec <10:
        count_sec = str("0" + str(count_sec))
    if count_min < 10:
        count_min = str("0" + str(count_min))
    canvas.itemconfig(timer_text, text= f"{count_min}:{count_sec}")
    if count > 0:
       DOWNTIMER = window.after(1000, count_down, count-1)
    else:
        if REPS % 2 != 0:
            TICKS += "✓"
            tick_label.config(text = TICKS)
        elif REPS == 0:
            TICKS = ""
            tick_label.config(text=TICKS)
            REPS = 8
        start_timer()



# ---------------------------- UI SETUP ------------------------------- #
window = tk.Tk()
window.title("Pomodoro")
window.config(padx = 200, pady = 100, bg = YELLOW)

canvas = tk.Canvas(window, width = 500, height = 500, bg=YELLOW, highlightthickness = 0)
tomato_img = tk.PhotoImage(file = "tomato.png")
canvas.create_image(250,250, image = tomato_img)
timer_text = canvas.create_text(250,280, text = "00:00", fill = "white", font= (FONT_NAME, 35, "bold"))
canvas.grid(row = 1, column = 1)

title_label = tk.Label(text ="Timer", font = (FONT_NAME, 35, "bold"))
title_label.config(fg = GREEN, bg = YELLOW)
title_label.grid(row = 0, column = 1)


start_button = tk.Button(text = "Start", command = start_timer, font = (FONT_NAME, 16, "bold"))
start_button.config(fg = GREEN, bg = YELLOW, padx = 30)
start_button.grid(row = 2, column = 0)

reset_button = tk.Button(text = "Reset", command = reset_timer, font = (FONT_NAME, 16, "bold"))
reset_button.config(fg = RED, bg = YELLOW, padx = 30)
reset_button.grid(row = 2, column = 2)

tick_label = tk.Label(font = (FONT_NAME, 16, "bold"))
tick_label.config(fg = GREEN, bg = YELLOW)
tick_label.grid(row = 3, column = 1)

window.mainloop()
