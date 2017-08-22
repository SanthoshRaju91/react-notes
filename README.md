# React session notes

Agenda of the session can be found in the link [react-training-tracker](https://react-training-tracker.herokuapp.com/)

Link to online editor [stackblitz](https://stackblitz.com/)

1. Walkthrough with React core basics without JSX and explain about module imports. This would also explain about properties.

```  
  const Title = (props) => {
  const style = { color: props.color};
  return (
    React.createElement('h1', { style: style }, props.title)
  )
}

const Header = () => {
  return (
    React.createElement('div', null, 
      React.createElement(Title, { title: 'Welcome To React', color: 'red'})
    )
  )
};

```

2. React Paradigm, explains about why React is so popular. Compared to other frameworks React does not contain a model / service / factory / controller. 

Why JSX ? 

People usually get pretty grossed out by the HTML in the JavaScript and say it looks like 1998 when we were still writing JavaScript in our HTML. However, I assert that markup in JS is a good thing while JS in markup is a bad thing! Here, we're keeping all the concerns of a component in one place: the markup structure, the event listeners, the state, the state mutators, everything. If the component breaks, we know it broke there. That's really valuable.

3. React States

We've discussed props which all you to have immutable state passed from parents to children. However, as any seasoned UI developer will point out, user interfaces are inherently stateful. You app at some level must contain some level of mutability. React gives you a very controlled window to introduce this mutability to be able to reason easily about this mutability aptly called state.

While props are passed down from parents and are immutable, state is created, read, and mutated all inside of a component. In other words, if a component has state, that state cannot be mutated by a parent, child, or any other external influence; only that same component has access to the setState method which is the only way to mutate state. That component has the ability to expose methods to children that the child can call to let the parent know it should mutate its state, but again, it is totally up to the parent to respect that call and mutate the state; the child can only call methods exposed to it via passed-down props.

4. List and conditional rendering

```
  <iframe width="420" height="345" src="https://www.youtube.com/embed/1TYsjaXWLx0"></iframe>
```
