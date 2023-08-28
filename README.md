# React-sythecticevent
https://www.codingninjas.com/studio/library/synthetic-event-in-react

In order to create common events for cross browser applications.

React has created a wrapper same as a native browser. It will create common name for all events to across browsers. It will increase the performances.

ex. e.preventdefault()
    e.stopPropagation()
React wraps all html DOM events into synthetic event wrpper.react will provide event consistency for all browsers. 

aLl the events bubbling up from inner most dom to their parent. Event stop propagation will help for prevant the bubbleing from child to parent .

event stop propagation and stop immediate propagation is used for integrating third party library 


All the synthetic events propagate on the target to his parents. To stop this stop propagation or stop immediate propagation

React optimize the prefomrances using synthentic event objects which means a actual event handler finished their execution react will nullify the event object and use it later.

Referenece event from the the syncnchornous code we need to call the event presist to notify react to not to nullify.
SyntheticBaseEvent === HTML Events 

function App() {
  const handleClick = (e) => {
    console.log(e)
  }
    //SyntheticBaseEvent {_reactName: 'onClick', _targetInst: null, type: 'click', nativeEvent: PointerEvent, target: button, …}
  return (
    <div className="App">
     <button onClick={handleClick}></button>
    </div>
  );
}

export default App;
