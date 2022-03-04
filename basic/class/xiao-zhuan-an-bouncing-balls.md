---
description: >-
  https://learn.arcade.academy/en/latest/chapters/18_window_class/window_class.html
---

# 小專案：Bouncing Balls

{% embed url="https://learn.arcade.academy/en/latest/chapters/17_class_methods/class_methods.html" %}

{% embed url="https://learn.arcade.academy/en/latest/chapters/18_window_class/window_class.html" %}

### Ball

![](<../../.gitbook/assets/image (122) (1).png>)

```python
import arcade

SCREEN_WIDTH = 800
SCREEN_HEIGHT = 600

class Ball():
    def __init__(self):
        # --- Class Attributes ---
        # Ball position
        self.x = 0
        self.y = 0

        # Ball's vector
        self.change_x = 1
        self.change_y = 2

        # Ball size
        self.size = 10

        # Ball color
        self.color = [255, 255, 255]

    # --- Class Methods ---
    def move(self):
        self.x += self.change_x
        self.y += self.change_y

    def draw(self):
        arcade.draw_circle_filled(self.x, self.y, self.size, self.color )

the_ball = Ball()

def on_draw(delta_time):
  arcade.start_render()
  the_ball.move()
  the_ball.draw()


def main():  
  arcade.open_window(SCREEN_WIDTH, SCREEN_HEIGHT, "Drawing with Functions")
  # R G B
  # Red Green Blue
  # arcade.set_background_color([255, 0, 0])
  # arcade.set_background_color(arcade.color.BLACK)

  # Finish and run
  # Call on_draw every 60th of a second.
  arcade.schedule(on_draw, 1/60)
  arcade.run()

main()
```

### Window

{% embed url="https://learn.arcade.academy/en/latest/chapters/18_window_class/window_class.html" %}

### 進階：使用者控制

[https://learn.arcade.academy/en/latest/chapters/19\_user\_control/user\_control.html](https://learn.arcade.academy/en/latest/chapters/19\_user\_control/user\_control.html)



