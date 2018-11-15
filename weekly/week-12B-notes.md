# Week 12B - More Vue.js

## I. Topics
- [Vue Part II - Ajax and Vue.js](https://github.com/tonethar/IGME-330-Master/blob/master/notes/vue-2.md)
- [Vue Part III - Simple Vue Components](https://github.com/tonethar/IGME-330-Master/blob/master/notes/vue-3.md)
- [Vue Part IV - Nested Components](https://github.com/tonethar/IGME-330-Master/blob/master/notes/vue-4.md)

<a id="review"></a>

## II. ReVue (get it?)
1. What is ***Reactive Programming*** ?
1. In a ***MVVM*** Vue.js app - what is role of the:
    - Model
    - View
    - ViewModel
1. Using a Vue *directive*, create a 2-way binding between an &lt;input> field and a Vue data property named `score`
1. Suppose you have a Vue `.method` named `doStuff` and a button with an id of `btn`. Write code that calls `doStuff()` when the button is clicked on:
    - do this *imperatively* utilizing DOM methods such as `document.querySelector()` as well as DOM event handlers
    - do this *declaratively* utilizing a Vue directive

## III. Reference
- **Reactive Programming** - I like the definition from [here](https://dl.acm.org/citation.cfm?id=2501666) - "Reactive programming has recently gained popularity as a paradigm that is well-suited for developing event-driven and interactive applications. It facilitates the development of such applications by providing abstractions to express time-varying values and automatically managing dependencies between such values."
- **MVVM ("Model–view–viewmodel")** - https://en.wikipedia.org/wiki/Model-view-viewmodel - the ViewModel of MVVM is a value converter, meaning the view model is responsible for exposing (converting) the data objects from the model in such a way that objects are easily managed and presented. ViewModel handles data binding, ensuring that the data changed in the Model immediately affects the View layer and vice versa. 
- **MVC v. MVVM** - https://stackoverflow.com/questions/667781/what-is-the-difference-between-mvc-and-mvvm
<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-12A-notes.md**](week-12A-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-13A-notes.md**](week-13A-notes.md)
