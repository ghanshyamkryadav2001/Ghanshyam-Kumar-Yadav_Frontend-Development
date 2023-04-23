# Ghanshyam-Kumar-Yadav_Frontend-Development

1. Explain what the simple List component does.

Ans- 
    The List component in this code is a React component that renders a list of items with the ability to select an item by clicking on it.

2. What problems / warnings are there with code ?

Ans- 
      (1) items prop default value: The items prop in the WrappedListComponent has a default value of null, which is not valid for an array. 
          A better default value would be an empty array []

     (2) isSelected prop in SingleListItem: The isSelected prop in the SingleListItem component is supposed to be a boolean value, but it's currently 
         being passed the selectedIndex state variable, which is a number. This may cause unexpected behavior when the component is rendered.

     (3) setSelectedIndex in WrappedListComponent: The setSelectedIndex state setter function in the WrappedListComponent is being incorrectly used as 
         the state variable itself. It should be used as const [selectedIndex, setSelectedIndex] = useState();

     (4) onClickHandler in SingleListItem: The onClickHandler prop in the SingleListItem component is currently not being passed the index of the item 
         correctly. Instead of passing the index directly, it should be wrapped in an arrow function to prevent it from being immediately invoked on 
         render.

     (5) propTypes for items: The propTypes definition for items is incorrect. It should be defined as PropTypes.arrayOf(PropTypes.shape({text: 
         PropTypes.string.isRequired})).
