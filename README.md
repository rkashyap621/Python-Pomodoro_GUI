# Python-Pomodoro_GUI

A Pomodoro time counter implementation using Python Tkinter Module.

The [Pomodoro Technique](https://en.wikipedia.org/wiki/Pomodoro_Technique) is a [time management](https://en.wikipedia.org/wiki/Time_management) method developed by Francesco Cirillo in the late 1980s. It uses a kitchen timer to break work into intervals, typically 25 minutes in length, separated by short breaks. Each interval is known as a pomodoro, from the Italian word for tomato, after the tomato-shaped kitchen timer that Cirillo used while he was a university student.

[Apps](https://en.wikipedia.org/wiki/Application_software) and websites providing timers and instructions have widely popularized the technique. Closely related to concepts such as [timeboxing](https://en.wikipedia.org/wiki/Timeboxing) and [iterative and incremental development](https://en.wikipedia.org/wiki/Iterative_and_incremental_development) used in software design, the method has been adopted in [pair programming](https://en.wikipedia.org/wiki/Pair_programming) contexts.

The original technique has six steps:

1. Deciding on the task to be done.
2. Setting the Pomodoro timer (typically for 25 minutes).
3. Working on the task.
4. Ending work when the timer rings and taking a short break (typically 5–10 minutes).
5. Going back to Step 2 and repeating until one completes four pomodori.
6. After four pomodori are done, one takes a long break (typically 20 to 30 minutes) instead of a short break. Once the long break is finished, one returns to step 2.



For the purposes of the technique, a pomodoro is an interval of work time (and pomodori is the plural form).

Once the script is run, the tkinter GUI appears in awindow like this:

![GUI_View](https://i.postimg.cc/vZLGFC5C/GH19.png)

Then, the use can click on **Start** button to begin the **Work Timer** which run the time countdown for 25 minutes to 0, during which the user can focus on the decided task.

![Start_Work_Timer](https://i.postimg.cc/g2w3gqRz/GH15.png)

Once the Work Timer reaches zero, it switches to **Short Break Timer**, and the green tick appears indiating the completion of 1 pomodoro.

![Short_break_timer](https://i.postimg.cc/jSWyMQNS/GH16.png)

Then, the above cycle of **Work Timer** followed by **Short Break Timer** until four green tick appears on the GUI screen ( Indicating completion of 4 pomodori). Now, the **Long Break Timer** Activates.

![Long Break Timer](https://i.postimg.cc/VkSXKBMN/GH17.png)

After the completion of **Long Break Timer** the green ticks dissappear from GUI screen and the **Work Timer** appears again and the above cycle continues.

![Work Timer Reappear](https://i.postimg.cc/T3yntqmT/GH18.png)

In any time, if the user want to stop the timer and reset it, they can aheive it by clicking on **Reset** button.
