How do you hide the warnings in React Native iOS simulator?

```

console.disableYellowBox = true;

```

***



Redux-form  re-init  form values.

```
function mapStateToProps(state) {
  return {
    nav: state.nav,
    login: state.loginReducers,
    initialValues: state.loginReducers.data
  };
}


LoginScreen = reduxForm({ form: "login", enableReinitialize: true })(
  LoginScreen
);

```

***


React- Navigation custom right button action.

```
class MyScreen extends React.Component {
    static navigationOptions = {
        header: ({ state }) => ({
            right: <Button title={"Save"} onPress={state.params.handleSave} />
        })
    };

    saveDetails() {
        alert('Save Details');
    }

    componentDidMount() {
      this.props.navigation.setParams({ handleSave: this.saveDetails });
    }

    render() {
        return (
            <View />
        );
    }
}

```
