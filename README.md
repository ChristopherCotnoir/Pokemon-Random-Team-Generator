# Pokemon Random Team Generator
This is a tool to generate a random team to use in a playthrough of a main series Pokemon game. Currently all games in Generations I-III are supported.

## How it works
To use this tool, first clone the repository and then open Team.html in a browser. This page has various options the user can set to generate the kind of team they want. The program takes into account complexities such as version exclusives and how certain Pokemon are incompatible on the same team (such as Hitmonlee and Hitmonchan or Omastar and Kabutops in Generation I). Once the user has set those the way they want, they can press the "Generate Team" button and a random team of fully-evolved Pokemon will be generated. The team will be displayed as 6 sprites of the generated Pokemon from that game in a single image that can then be saved if desired.

The Pokemon are displayed approximately in the order they would be obtained if going through the game in the intended order. The order chosen is subjective to some extent in terms of when to do various side-paths or what order to do branches. Additionally, often times new areas give access to multiple new Pokemon. Typically Pokemon that appear in the Day have priority, followed by Morning and then Night. After that Pokemon with higher encounter rates are listed first. Backtracking when obtaining a new HM/Rod/etc. is generally immediate. Thie order won't be perfect, but most of the time it will be a reasonable representation of when you get the team members.

## Options

### Game
This option is a dropdown list of all the supported Pokemon games. This option determines which Pokemon are generated based on which Pokemon are available in that game. Only fully-evolved Pokemon available in that game before the Elite Four (Or Red in G/S/C) can be generated. This option also determines which sprites are used.

### Starters
Starters can be somewhat of a special case in random teams. There are 3 radio buttons representing the options for this setting:
 - Disallow
 - Allow
 - Guarantee
 
"Disallow" prevents any starter Pokemon from being generated. Often times people use random teams as a challenge or to use Pokemon they don't normally use and don't want to use starters for that. "Allow" allows starter Pokemon to potentially be generated. This is useful when people are OK with starters as a possibility. "Guarantee" always generates a random starter Pokemon (Pikachu is always used in Pokemon Yellow) as the first slot in the team. This makes it possible to play using only Pokemon from the team the entire time, rather than having to use the starter up until obtaining the first real team member.

### Trade Evolutions
Random teams are often a form of challenge, and usually these preclude trading with other games. This setting controls how to handle Pokemon that evolve by trade. There are 3 radio buttons representing the options for this setting:
 - Disallow Selecting
 - Disallow Evolving
 - Allow
 
"Disallow Selecting" ensures Pokemon families with trade evolutions are not selected, so that only fully-evolved Pokemon obtainable without connecting to other games are possible. "Disallow Evolving" allows selecting these Pokemon, but displays the Pokemon stage before the trade evolution, allowing these families to be selected but taking into account that the player will not be trading with other games. "Allow" allows trade evolutions to be generated, for people who are OK with simply trading to and from another game. This is only for trade evolutions and not version exclusives or otherwise unavailable Pokemon.

### Legendaries
Challenge runs generally do not allow Legendaries as they are too powerful. More casual playthroughs may or may not allow them. There are 2 radio buttons representing the options for this setting.
 - Disallow
 - Allow
 
"Disallow" prevents Legendaries from being generated as part of the team, whereas "Allow" permits it.

### Duplicate Types

Often times when people construct in-game teams, they like to avoid duplicate types for greater variety. This setting controls any possible type restrictions. There are 3 radio buttons representing the options for this setting.
 - Allow
 - Disallow Exact Match
 - Disallow Overlap
 
"Allow" doesn't take typing into account when generating teams, meaning duplicate types can appear. "Disallow Exact Match" is more restrictive. It prevents generating Pokemon with the exact same type combination, but does allow shared types. For example, Pelipper and Sharpedo would be allowed, while Pelipper and Gyarados would not. "Disallow Overlap" is the most restrictive option, preventing any Pokemon on the team from having any shared types.

### Blacklist
This option is a line-separated list of Pokemon. Any Pokemon listed here will not be generated. This can be used to avoid particularly annoying options like Unown or Shedinja, or to exclude Pokemon people really don't like or have already used.

### Number of Pokemon Guaranteed by Badge
This option allows the user to control when they get new Pokemon. This can be used to prevent getting the first Pokemon late and having to use the starter for too long, or getting most of the team too late in the game. Each badge has a dropdown where 0-6 can be selected (1-6 if Starters are guaranteed as 1 Pokemon will always be on the team in that case). All values for subsequent badges will be changed to be at least this much. This represents how many Pokemon you want the generator to guarantee will be available by each badge to tweak how quickly the team is completed. When the game is Gold, Silver, or Crystal 1-16 badges will be displayed instead of 1-8.

Note that since this is a measure of progress, each Pokemon is assigned a number of badges the user is likely to have when the Pokemon is acquired to be used by this option, not the minimum number of badges that absolutely must be acquired to obtain this Pokemon. In Kanto for instance, the player has a great deal of control over the order they get badges, only requiring Brock be first, Misty be second, Giovanni be last, and Koga be before Blaine. It is possible to get nearly every Pokemon in these games with just two badges, Pokemon that require surfing to access only need three and Articuno only needs four, which would make this a poor representation. Johto also allows Chuck, Jasmine, and Pryce to be battled in any order as well as all but the last of the Kanto Gym Leaders to be battled in any order. Hoenn allows skipping Brawly up until after Flannery and skipping Winona until right before the Elite Four. As such, instead it is generally assumed that the badges will be obtained in their intended order and that they will be obtained as soon as available. The exact cutoffs are somewhat subjective, but should be generally close.
