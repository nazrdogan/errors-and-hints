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

