# CSS_group0

### Group members
Leon Kuiper, Elizabeth Law, Jing Hu, Dennis Curti

# Basic model
We implemented the basic Bak-Sneppen model for 1D and 2D. The code is written in Python 3.9.7 and the packages we used were numpy, matplotlib.pyplot and matplotlib.animation.

The parameters were changed for a much lower runtime. Now it takes around 2.5 minutes to run the main notebook on a PC and around 9 minutes on a slower laptop.

# Migration attempt
We have looked at the migration extension of the model, where every cell of the grid moves in a timestep. The issue that we had with the code was that we could not find out the order in which to mutate the cells, since moving all the cells instantly is not possible without some sort of bias incurred by looping through the grid in the same order every timestep. We have tried to move them in a specific order (highest /lowest fitness first), randomly and made sure that they do not collide, but that did not seem to work. One other confusion that we had was that the paper mentions that the "marks" of the cells live for one timestep, but they do not mention anywhere in the paper if the current timestep will be the lifespan of the marks or the next one. That leads to the question of whether all marks get deleted in the next timestep or if we should delete the marks for one more timestep after the current one. I could not find any code for the paper either, and since all of these methods failed, we ran out of time. That is why we only used the basic model for our presentation.
