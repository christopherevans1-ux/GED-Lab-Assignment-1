Name: Christopher Evans
Student Number: 100968759

Project Title: Project Running Man

Gameplay Loop: Player starts at the beginning of the level. They must traverse the level and dodge or kill enemies to get to the goal and beat the level.

Diagram: (psudocode)

  public class AudioManager : inherits from Singleton<grabbing AudioManager>
// ---Initialization---
  grab player gameobject
  sound effect jumpSound
  sound effect deathSound
  sound effect winSound
  sound effect enemyDeathSound
  Grab AudioSource (named audioSource)
  // ---GameLoop---
 function Update():
    player = find player gameobject
    audioSource = find object in scene with the same type as AudioSource
    if((player pressing spacebar & is not dead & is on ground & game is not paused):
      play jump sound effect
    if(player jumps on-top of an enemy):
      player jump sound and enemy death sound
    if(player is dead):
      play death sound effect
    if(player beat the level):
      play win sound effect
  Public class Singleton: Monobehaviour with placeholder component

  // ---Initialization---
  private Static instance of placeholder (_instance)

  //---GameLoop---
  Public Static placeholder Instance:
  get:
    if(_instance is null)
      _instance = find instance is scene
        if(_instance is null):
        crate new gameobject
        object name = placeholder name
        _instance = object with placeholder component

  return _instance


  public virtual void Awake():
    if(_instance is null):
      _instance = this placeholder
      do not destroy instance gameobject
    else:
    destroy instance gameobject

Question 1: The sound adopts my use of the singleton pattern. Rather than having sound effects dealt with on sperate objects with multiple audio sources. 
I have 1 audio source on the player that plays different sound effects given certain situations like jumping, death, and upon completing the level.

Question 2: The singleton pattern works well with an audio manager design since it allows me to easily keep track of sound effects across the entire game. 
If one sound is played incorrectly, I don't have to go digging through multiple files to find the source. IT allows all sound effects to live
comfortably in one space that never needs to be re-created upon restart, or a new level(scene).


External Assets used:
Mario jump sound effect from youtube
fortnite death sound effect from youtube
tom from tom and jerry scream sound effect from youtube
win sound effect no copyright from youtube
