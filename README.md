# React session notes

Agenda of the session can be found in the link [react-training-tracker](https://react-training-tracker.herokuapp.com/)

Link to online editor [stackblitz](https://stackblitz.com/)

1. Walkthrough with React core basics without JSX and explain about module imports. This would also explain about properties.

 `  
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

 `


