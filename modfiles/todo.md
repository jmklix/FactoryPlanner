# TODO

# Any time

- Quality effect is multiplied by 10 in machine/beacon dialogs
- Use button's `auto_toggle` argument? Sounds really nice, in combination with `toggle` elsewhere maybe
- Look into using the new sprite button definition style if that's a thing
  - Seems there might be nothing new, but disabling buttons now modifies their icon, which is undesirable in come cases
- Figure out how to generate offshore pump prototypes again
- Figure out how energy consumption and drain works in the new API
- Check out how to handle emissions for different pollutant types? Do I just need to show all if applicable?
  - Only implemented `"pollution"` for now
- Redo rocket handling now that they can't take specific items anymore, which hopefully is a simplification
- Combinators are completely changed due to logistic groups, so all that logic needs redoing
  - Logistic groups might impact other stuff as well, or could be useful for the mod (utility item requests anyone?)
- Is `base_productivity` not a thing on Entities anymore? If not, remove from code, otherwise migrate
- Are `limitations` on module items not a thing anymore? What replaces that system?
  - `allowed_effects` now a thing on recipes apparently
  - also effect_receiver :: EffectReceiverPrototype ?
- Fix _porter.import_factories(), probably by adjusting the factory string
  - Example subfactory also doesn't work, needs some general migration fix it seems
- Holy shit quality fucks up a lot of stuff.
  - Every place I need a property that can be influenced by quality, I can specify that quality.
  - So theoretically every place I use such a prototype I could offer a choice of which prototype to use.
  - Which also means I'd need to keep around a value for every possible quality and account for it everywhere.
  - This is quite insane, so for the first version I'll assume everything has normal quality.
- Kinda need the better indication of cyclic recipes for this crap, due to space platform recipes
- Remove pasting items over products, replacing the latter. Only have it set the amount if identical
- Remove RB support and add Factoriopedia support
- Apparently the custom blueprint prototype is unnessecary now?
- Deal with new beacon effect logic

# Waiting on

- Uncomment all the `.hidden` uses that were missing from the API
- Wait on item group order getting fixed
- Find out what's wrong with `wide_as_column_count` on tables

# Release

- Update other language docs for the new `plural_for_parameter` format
- Verify custom arcosphere logic

# Nice-to-have

- Adjust utility dialog handcrafting to behave like vanilla crafting does in all ways
- The mod should create districts per planet automatically, once districts are implemented. First one should be called Nauvis too