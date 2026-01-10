# Video Player

You just learned your first programming pattern. Let’s put it to use!

For this project, you’ll make three React components work together to create a responsive video player.

If you get stuck during this project or would like to see an experienced developer work through it, click “Get Unstuck“ to see a project walkthrough video.

Let’s get started!

Tasks

Mark the tasks as complete by checking them off
1.
Click Save, and take a look at your video player in the browser. It looks pretty good! But if you try interacting with it, you’ll find that there’s zero functionality.

Take a look at the App component. This component has one property stored as state using useState(): a src containing the address of a video file. App‘s job is to pass this src down to a stateless component, and to pass the ability to change the src down to a different stateless component.

Passing src is the easier part, so let’s do that first.

Inside of App‘s return statement, give <Video /> an attribute. Make this attribute’s name src, and the attribute’s value equal to src.

If we were to give <Video /> an attribute named title with the value of videoTitle, we’d write the following:

<Video title={videoTitle} />

Copy to Clipboard

2.
Let’s make <Video /> play its passed-in video file!

Select Video.js.

In Video‘s return statement, give <video /> a src attribute. Make src equal to the passed-in video file.

Remember to access the src property of props using the dot notation.

3.
Alright, the video player works! Now, let’s make the menu work as well.

You’ve made App pass the src down to <Video />. Now App needs to pass the ability to change the src down to <Menu />. If you want to pass the ability to change state, then first, you need to define a function that calls the state setter function returned by useState().

In App.js, define a function called onSelectVideoHandler() with a single string parameter called newVideo. Use newVideo to get a new source from VIDEOS and use this as an argument to setSrc.

Make sure to define the onSelectVideoHandler() function inside the App component, but before the return statement.

4.
If you pass onSelectVideoHandler() to <Menu />, then you will give <Menu /> the ability to update <App />‘s state.

In App‘s return statement, give Menu an onSelectVideo attribute. Set onSelectVideo‘s value equal to the onSelectVideoHandler() function.

Remember, when you pass a function as a value of an attribute, you should omit the parentheses that typically follow the name of a function.

5.
Alright, now you just have to attach this passed-in function to an event listener!

Select Menu.js.

In Menu‘s return statement, give the <form> element an onClick attribute. Set onClick‘s value equal to the passed-in onSelectVideo function.

Try selecting a video in the browser.

It doesn’t work! Do you know why?

onSelectVideo expects a string as an argument. But event handlers are automatically passed event objects, not strings.

Let’s fix this next.

Remember to access onSelectVideo property from the props object.

6.
Before using onSelectVideo, we’ll need to wrap it in a new function that can take an event object as an argument.

Define a new function in Menu named clickHandler() with a single parameter called event.

Inside the body of clickHandler(), declare a new constant named name. Set name equal to event.target.value. This will equal the value of a clicked radio button.

Next, call onSelectVideo() with name as an argument.

When you call the onSelectVideo() function, you’ll need to reference the props object first using the dot notation like below:

props.onSelectVideo(text);

Copy to Clipboard

7.
Only one more step! You need to use your new wrapper function as an event handler.

In Menu‘s return statement, replace {props.onSelectVideo} with {clickHandler}.

clickHandler() should be the new event handler for the <form> element’s onClick attribute.

8.
Great job!

App passes down src to Video. Video uses this info to display the chosen video.

App also passes down the ability to change src to Menu. Menu uses this ability to let a user select a new video.

You’ve put together a responsive video player and applied a React programming pattern often used by professional React developers.