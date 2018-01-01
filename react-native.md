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
static navigationOptions = ({ navigation }) => {
    const { state, setParams } = navigation;
    const { params = {} } = navigation.state;
    return {
      tabBarLabel: "Profil",
      headerTitle: (<Text style={{ fontFamily: themefontFamily }}>Profilim</Text>),
      tabBarIcon: ({ tintColor }) => (
        <MaterialCommunityIcons
          name="account"
          style={[styles.icon, { color: tintColor }]}
        />
      ),
      headerRight: (
        <MaterialCommunityIcons
          name="logout-variant"
          onPress={params.handleSave ? params.handleSave : () => null}
          style={{
            width: 26,
            fontSize: 26,
            marginRight: 5,
            height: 26
          }}
        />
      ),
    }
  };


  _handleSave = () => {
    alert("Handle");
  }

  componentDidMount() {
    // We can only set the function after the component has been initialized
    this.props.navigation.setParams({ handleSave: this._handleSave });
  }


```
