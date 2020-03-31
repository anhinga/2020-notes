### Research drafts

---

### January 2020

Title:

_Exploring functional reactive architectures for neural machines_

---

Abstract:
  * Is it fruitful to consider functional reactive implementations of neural machines?
    This draft starts to explore this question.

**March 31, 2020 follow-up to the functional reactive draft:**

While Elm is no longer a functional reactive language, its original functional reactive design
is alive in Julia Reactive:

https://juliagizmos.github.io/Reactive.jl/

For a number of reasons noted elsewhere in this repository, Julia is the best fit for the DMM development at the moment.
Julia Reactive is instrumental in GtkReactive and ImageView, so it is not disappearing any time soon
(no danger it will share the fate of original Elm and its Signal functionality). I have just tweaked GtkReactive so
that so that the movie in its player does not stop when the end is reached, 
but instead starts playing in the opposite direction, and so on indefinitely:

https://github.com/anhinga/GtkReactive.jl
