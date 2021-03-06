# [Solving Your Own Games](@id own_game)

```@meta
CurrentModule = AlphaZero
```

Here are some recommended steps for using AlphaZero.jl on your own game.

1. Implement the [Game Interface](@ref game_interface) for your game. You can look at
   the examples in the `games` directory for inspiration.
2. Once you have defined an [`AbstractGameSpec`](@ref), you can use [`Scripts.test_game`](@ref)
   to run a series of sanity checks on your implementation.
3. Define your neural network architecture or reuse
   one from the [Networks Library](@ref networks_library).
3. Think about your training hyperparameters and define an
   [`Experiment`](@ref). Once again, you may draw inspiration from the provided examples.
4. Before running a complete training session, you can use
   [`Scripts.dummy_run`](@ref) to check the absence of potential runtime errors in your
   code.
5. Run a training session using [`Scripts.train`](@ref). You can interrupt training at any
   moment and resume it later since the current state of your agent is saved automatically
   in the `sessions` folder after each iteration.
6. Look at the generated plots and reports and adapt your hyperparameters if necessary.
   Also, you can visualize your current agent using [`Scripts.explore`](@ref).

If you've managed to train a successful agent, please consider sharing your experience
with us by [opening an issue](https://github.com/jonathan-laurent/AlphaZero.jl/issues) on
Github or posting on the [Julia Discourse](https://discourse.julialang.org/) forum.