## Growtopia Item Database
A growtopia item database which gathers in-game data about items.

All the data is taken from in-game from the items i own, or screenshots of items i got from people and written to github by me.

* This project is licensed CC-BY-4.0, meaning you **must** provide credits before usage.

Any contributors are listed in the [Contributors](https://github.com/MrAugu/growtopia-item-database#contributors) section.
## Contribution
If you have any other item's information, find mistakes in the current data, feel free to screenshot info section in game and open an issue or even a pull request to add that information.

## Seeds
Item data file does NOT contain any seeds, only items because all items follow the same structure.

Seeds inherit the chi and the rarity of the item's seeds and have no properties.

Exception to this are fruits with the `A tree of this type can bear surprising fruit!` property - which mean that a tree can produce multiple types of items (such as tangram blocks, number blocks, surgical tools).
```
0. {Item Name} Seed
- Description: Plat this seed to grow a {Item Name} Tree.
- Chi: {Item Chi}
- Rarity: {Item Rarity}
```
## Existing Seeds
> Every single item a growtopia has a seed, though, there are only 60% items, approximatively, have an obtainable seed.

Which means that we need to deduce it.

Here's how we do it:
```
If (Item does not have property: 'This item never drops any seeds.')
  - Item has a seed.
Else If (Item is a clothing item [haves a clothing : arm/feet/hand/etc property] & Item does not have proerty: '- This item can't be spliced.')
  - Item has a seed.
Else
  - Item has no seed.
```
First case is the absence of the property which notes that item does not drop any seeds from which we can deduce that item has no seed.

Otherwise, if an item does have that property another case is compacting of the clothes which do have a small chance of dropping actual item seed - only spliceable clothes can be compacted.

If none of the 2 conditions above matched the item, it means that we can assume that the item seed is un-obtainable/inexistent (again, every single item in growtopia, even ringmaster, do have a seed, which is why there are some super glitched seeds such as bedrock).
## Contributors
*None outside the repository owner*
