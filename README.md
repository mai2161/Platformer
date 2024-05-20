
<a name="readme-top"></a>

<!-- PLATFORMER-->




  <h3 align="center">Best-README-Template</h3>

  <p align="center">
    An awesome README template to jumpstart your projects!
    <br />
    <a href="https://github.com/othneildrew/Best-README-Template"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/othneildrew/Best-README-Template">View Demo</a>
    ·
    <a href="https://github.com/othneildrew/Best-README-Template/issues/new?labels=bug&template=bug-report---.md">Report Bug</a>
    ·
    <a href="https://github.com/othneildrew/Best-README-Template/issues/new?labels=enhancement&template=feature-request---.md">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
    </li>
    ap</a></li>
    <li><a href="#contributors">Contributors</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

[Platformer Game Demo](https://www.youtube.com/watch?v=Vpm8Qu17pwo)

The Project focuses on designing and implementing a VGA-based
game using SystemVerilog on the DE-1O lite board. Our primary objective of the project is to
create an engaging and educational gaming experience and provide a learning experience
through the game development process, implementing the concepts learned in classes and
labs. It also showcases the efforts in logic designing, real-time dynamic visual feedback,
focusing on the details, providing clarity on clock working, while addressing the problems
faced on the way to deliver a gaming experience on the FPGA hardware. By utilising VGA
display, HEX display, KEY[0], KEY[1], SW[0:9], LEDR[0:9] as well as the clock, our game
provides an immersive experience in a dynamic virtual world filled with challenges and
rewards

●  Users select levels by activating the respective switches which are SW[0] for Level 1,
SW[1] for Level 2, and SW[2] for Level 3, and pressing KEY[0]. The text turns to
yellow when a level is selected. The text displayed along with the colours are methods
via pixel logic and rendering.

●  Platform movement logic - When the counter reaches the value of 1000000, it resets
zero and checks the position of platform 1. Depending on the position, the direction of
movement is adjusted accordingly. If the position is above or equal to 420, it changes
direction. The platform’s position is updated based on the direction of movement.

●  Player movement logic - It checks if a counter has reached a threshold, and then
resets the counter. Depending on the direction of the player character and its position,
the code adjusts the position of the player within the screen bounds. The direction
changes according to the continuous movement within screen limits.

●  Jumping behaviour and adjust ground- The jump height has been set to 50 pixels.
A counter tracks the duration of the jump and adjusts the player’s vertical position
based on the ascending or descending phase of the jump. If the player is about to land
on the platform, the position is adjusted accordingly and the ground is updated setting
it as a new ground. If the player is not jumping and the KEY[1] is pressed, the
character is set to jump in its place. The code makes sure that the player falls when no
platform is detected. It tracks the state of the jump button. If at the bottom, the ground
level is 450

●  Coin Collection and collision - This part of the code checks if the coin is visible on
screen and the player’s position overlaps with the coin position. If a collision is
detected, the coin’s visibility is set to 0 which indicates the coin has been selected and
the coin counter is increased to keep track of the collected coin and display it on the
HEX[3] and HEX[4].

●  Random coins generating logic - This part of the code checks if all the coins are
collected, it generates more coins by resetting their positions to make them visible
again. New positions are determined by randomizerCount and its variants.

●  Red platform Collision and reset the level - When the player collides with a red
platform, the game over screen is rendered from the second always block. It resets the
level by resetting the position and movement directions of all platforms and player
characters to their starting state. It reset the counters and flags related to jumping and
movement. The platforms and player is set to their starting state and randomizer
counters are reset to generate new positions for coins.

●  Counter and High score display on HEX displays - The counter decrements from
45 to 0 every second based on the clock. When the count reaches zero, it indicates the
end of the countdown, the flag is set to 1. The code also converts the second count
into a two-digit pattern for display on the HEX display.

●  Image rendering, pixel manipulation, and VGA display - This part of the code
renders various elements including the player, platform, and cons with different colors
based on the position. If the game-over conditions are met, it displays “GAME
OVER” on the screen with a black background. It also showcases different colour
backgrounds for different levels and the main page and game over the page.
RESULTS

●  The resources we used was the lab 5 file vga_controller.v to use for connecting to the
monitor. We used a monitor with a vga connection as well as the De-10 light board.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



### Built With

* Quartus Prime 20.1
* Verilog
* System Verilog
* DE10-Lite FPGA Board


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

1. Download or have Quartus Prime 20.1 installed
2. Download Game2.zip folder onto your desktop
3. Extract the files into the same folder
4. Open and Run the Quartus Prime Software
5. In the top left corner Open a new Project and open the extracted files
6. Connect your VGA cable to your board and monitor
7. Connect the board to your desktop
8. Run the quartus prime software (make sure you have selected and set up the board correctly)




<p align="right">(<a href="#readme-top">back to top</a>)</p>





<!-- CONTRIBUTORS -->
## Contributors
Winter 2024 3216 EECS Final Project
Bora Suda, Shreya Vaghani, and Mai Komar
<p align="right">(<a href="#readme-top">back to top</a>)</p>







<p align="right">(<a href="#readme-top">back to top</a>)</p>



