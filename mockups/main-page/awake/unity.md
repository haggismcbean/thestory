# Unity: How to make a 2d game like the one I want to :)

## 1. Players/NPCs

### Prefabs

(https://unity3d.com/learn/tutorials/projects/2d-roguelike-tutorial/player-and-enemy-animations?playlist=17150)

The first step is to create prefabs of all the characters with their animations loaded in. Assuming you already have a split spritesheet with all the animation components:
1. Create a GameObject
2. Name it Player (or Preditor, or Prey, or whatever)
3. Go to the spritesheet and highlight the necessary segments for one animation cycle (eg idle)
4. Drag the segments onto the Player GameObject
5. This will create a PlayerAnimationController and a PlayerIdle animation: move these to the appropriate folders
6. Drag the Player GameObject into the prefabs folder to create a prefab of it (you can then eg. delete the GameObject)

You may want to use the same animation logic for different GameObjects, in this case, instead of creating a Player2AnimatorController you create a Animator Override Controller (in the create dropdown in the bottom left). Then you drag the controller you want to mimick, and drag the animations you want to be mimicked, and then in the GameObject Animator component change the Controller to this new override controller