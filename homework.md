What are actions used for?
Actions are objects that are used to update the current state.

What type of object must an action be?
It has to be a plain JS object.

At a minimum, what is the one property the action should have? And what is this property used for?
It has to have a type at least, that indicates the type of action that will be used.  It is used to update the state.

What is the responsibility of the reducer?
The reducer knows how to update the state by taking in the action.

What is the responsibility of the store?
The store holds the state and it's current version and keeps track of it after every change.

Which of the following functions are pure: reducer3, reducer5

const reducer1 = (action, state) => {
  return state + 1;
}

const reducer2 = (action, state) => {
  state.push("Cat");
  return state;
}

const reducer3 = (action, state) => {
  return [...state, "Dog"];
}

const reducer4 = (action, state) => {
  return state.map(pet => {
    pet.price /= 2;
    return pet;
  });
}

const reducer5 = (action, state) => {
  return state.map(pet => {
    return { ...pet, pet.price: pet.price / 2 }
  });
}
