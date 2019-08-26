# Components-Props
• Components : When building react native application, many components are used. For example, 
       
	   1. <Text> component which holds some sort of text. 
       2. <View> component is same as <div> in html, which defines a section.
       3. <Image> component holds the image url to be rendered.

• Props : Most of the components can be customized using parameters called props. Props are the properties of the components. 
  For example,
	
		<Button onPress = () => {this.handlePress()}></Button>
	
onPress is a property of <Button> component which handles functionality of a button when pressed.
  
Customized components can also use props, i;e: Our own components can also use props like,

	import React, { Component } from 'react';
	import { AppRegistry, Text, View } from 'react-native';

			class Greeting extends Component {
				render() {
					return (
						<View style={{alignItems: 'center'}}>
							<Text>Hello {this.props.name}!</Text>
						</View>
					);
				}
			}

			export default class LotsOfGreetings extends Component {
				render() {
					return (
						<View style={{alignItems: 'center', top: 50}}>
							<Greeting name='Rexxar' />
							<Greeting name='Jaina' />
							<Greeting name='Valeera' />
						</View>
					);
				}
			}
			
Here, making a single component that can be used in many different places in the application, with slightly different properties in each place. Just refer to this.props in your render function, using name as a prop lets us customize the Greeting component, so that component cane be reused for each of the greetings. This example also uses the Greeting component in JSX, just like the built-in components.
