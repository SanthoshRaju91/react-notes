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
