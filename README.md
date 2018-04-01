For an art project, I created an imaginary country, [abulia](https://abulia.online) a former colony from Swizerland and Poland.
And beside a flag and a moto, what else do we need? a language, Abülski.

So by feeding a markov chain with a mix of swiss german (mostly guidebook sentences, but a bunch from a friend) and polish (the constitution), shake it and voila, you have something that looks like a language.




## How It Works

**It is based on MarkovNameGen** is a Markov chain-based procedural name generator written in Haxe. Run it now [in your browser](http://www.samcodes.co.uk/project/markov-namegen/).


Demonstrates the [markov-namegen haxelib](http://lib.haxe.org/p/markov-namegen). Read the [documentation here](http://tw1ddle.github.io/MarkovNameGenerator/).

The [markov-namegen haxelib](http://lib.haxe.org/p/markov-namegen) uses [Markov chains](https://en.wikipedia.org/wiki/Markov_chain) to procedurally generate original words.

Using a set of words as [training data](https://en.wikipedia.org/wiki/Machine_learning), the library calculates the conditional probability of a letter coming up after a sequence of letters chosen so far. It looks back up to "n" characters, where "n" is the order of the model.

The generator can use several orders of models, each with memory n. Starting with the highest order models (models with bigger memories), it tries to get a new character, falling back to lower order models if necessary - an approach known as [Katz's back-off model](https://en.wikipedia.org/wiki/Katz%27s_back-off_model).

A [Dirichlet prior](https://en.wikipedia.org/wiki/Dirichlet_distribution#Special_cases) is used to add a constant probability that any letter may be picked as the next letter. This acts as an additive smoothing factor and adds a bit more "randomness" to the generated output.

Countless words are generated, and are then filtered and sorted according to several tweakable criteria like length, start and end characters, [similarity to a target word](https://en.wikipedia.org/wiki/Levenshtein_distance), and so on.

## Notes
* Many of the concepts used for the generator were suggested in [this article](http://www.roguebasin.com/index.php?title=Names_from_a_high_order_Markov_Process_and_a_simplified_Katz_back-off_scheme) by [Jeffrey Lund](https://github.com/jlund3).
* If you have any questions or suggestions then [get in touch](http://samcodes.co.uk/contact) or open an issue.
* Remember to read the [documentation](http://tw1ddle.github.io/MarkovNameGenerator/).

## License
The website and demo code are licensed under CC BY-NC. The [haxelib library](http://lib.haxe.org/p/markov-namegen/) itself is MIT licensed. The noUiSlider settings sliders are WTFPL. Most of the training data was compiled from sites like Wikipedia and census data sources.
