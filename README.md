# Reinventing Pixel Dungeon: An AI-Driven Journey
Welcome to our ambitious initiative to reinvent Pixel Dungeon Shattered! Combining AI technologies and modern game development strategies, we're on a quest to craft a gaming experience that's not only more adaptable and modular but also profoundly community-centric.
Our key objective is to safeguard the spirit and mechanics of the original game while reshaping its architecture to be more flexible and customizable.

## Index
1. [Descending…](#descending)
    * [Sewers: AI-Powered DSL](#sewers) 
    * [Prison: Content migration](#prison) 
    * [Caves: Modular Structure](#caves) 
    * [Dwarven City: Game System Engineering](#dwarven-city) 
    * [Demon Halls: Testing, Deployment, and Community Connection](#demon-halls) 
2. [AI Contributions](#ai-contributions) 
3.  [Participation Opportunities](#collaborate) 
4.  [Project Commencement](#commencement) 
5.  [Human-Readable Configuration](#sample-config-file) 
6.  [Acknowledgements](#acknowledgements) 
7.  [License](#license) 


## <a  id="descending"></a>Descending…
1. <a  id="sewers"></a>Sewers: AI-Powered DSL
Our first mission involves designing a Domain-Specific Language (DSL) with the aid of AI to define game components such as mobs, items, and hero classes.
2. <a  id="prison"></a>Prison: Content migration
Relying on AI, we'll magically transfer content from the classic Pixel Dungeon Shattered to our reimagined platform.
3. <a  id="caves"></a>Caves: Modular Structure
In this stage, we'll craft a modular architecture that's vital for a seamless evolution of the game, with a little help from our AI comrades.
4. <a  id="dwarven-city"></a>Dwarven City: Game System Engineering
At this point, we'll engineer systems to manage game mechanics and content, integrating them with data models originating from our DSL.
5. <a  id="demon-halls"></a>Demon Halls: Testing, Deployment, and Community Connection
Our final mission includes ensuring smooth gameplay and fostering a dynamic community around our reimagined Pixel Dungeon.

## <a  id="ai-contributions"></a>AI Contributions
AI will be instrumental in several areas of our project:
1. DSL Design: Crafting a flexible DSL for game components using AI.
2. Content Migration: Utilizing AI algorithms for a flawless and seamless content transfer process.
3. Game Mechanics Refinement: Identifying opportunities for enhancement and recommending refinements to game mechanics with the aid of AI.
4. Balancing Game Elements: Maintaining balanced gameplay through AI-driven scrutiny of character abilities, item attributes, and the like.
5. Procedural Content Generation: Implementing AI methods to devise dynamic, procedurally generated content such as levels, quests, and challenges.
6. AI Behavior Enrichment: Enhancing the AI behavior of in-game characters and mobs for a more reactive, engaging player experience.

## <a  id="collaborate"></a>Participation Opportunities
Developers can contribute by extending the codebase, while players and community members can offer valuable feedback and insights into elusive in-game scenarios. Donations are also appreciated to offset costs associated with using the OpenAI API for AI-assisted development.

## <a  id="commencement"></a>Project Commencement
We're thrilled to initiate our AI-powered Pixel Dungeon Shattered reimagination, which is now live and open source! We've harnessed the power of AI to maintain a more malleable gameplay experience, preserving the original game mechanics and content.
Our ambition is to simplify the path for developers and modders to create, modify, and expand game content through simple configuration files. Here's a placeholder example of what a human-readable configuration file could look like:

<a  id="sample-config-file"></a>

```yaml

mechanic mob_combat {
  loop while: enemy_health > 0 and self_health > 0 {
    if: distance_to_enemy <= attack_range {
      action: attack
      target: enemy
      damage: self_attack_damage
    } else {
      action: move
      target: enemy
      mechanic: self.walk_mechanic
    }
    if: enemy_health <= 0 {
      action: celebrate_victory
      target: self
    }
    if: self_health <= 0 {
      action: die
      target: self
    }
  }
}
```

```yml
mob base_mob {
  walk_mechanic default_walk
  walk_attribute {
    speed: 1.0
    agility: 1.0
    step_distance: 1.0
  }
  combat_mechanic mob_combat
  combat_attribute {
    attack_range: 1.0
    attack_damage: 10.0
  }
}
mob albino_rat inherits base_mob {
  walk_attribute {
    agility: 0.8
  }
  combat_attribute {
    attack_damage: 8.0
  }
}
mob spider inherits base_mob {
  walk_mechanic wall_walk
  walk_attribute {
    speed: 1.5
    agility: 1.2
  }
  combat_attribute {
    attack_range: 2.0
    attack_damage: 12.0
  }
}
}
```

This is just a glimpse of what we're aiming to build. We invite you to join us on this thrilling odyssey. You can contribute by extending the code, offering feedback, making suggestions, or even donating to support the use of the OpenAI API. Together, we can add new chapters to the legend of Pixel Dungeon!
## <a  id="acknowledgements"></a>Acknowledgements
Hearty shout-out to the mastermind behind <a href="https://github.com/watabou/pixel-dungeon" target=_blank>Pixel Dungeon</a>, Watabou, and the wizard of <a href="https://github.com/00-Evan/shattered-pixel-dungeon" target=_blank>Pixel Dungeon Shattered</a>, 00-Evan. Your extraordinary craftsmanship was the bedrock for this venture. We're all set to carry forward your legacy, spicing it up with our unique flavor and cutting-edge methods. The digital gaming realm owes you big time, buddies!
## <a  id="license"></a>License 
This project, while a major rewrite, is a fork of "Pixel Dungeon Shattered". As such, we're upholding the original GPL-3.0 License. Please review it if you're planning to contribute or use our project.
