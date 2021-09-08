## Standard Events

### Login Event

***// Android***
```
Bundle params = new Bundle()
	params.putString(Param.METHOD, method);
	
	firebaseAnalytics.logEvent(Event.LOGIN, params);
```

***// iOS***
```
Analytics.logEvent(AnalyticsEventLogin, parameters: [
	AnalyticsParameterMethod: method!
])
```
	
***// Facebook***
```
-- WE DO NOT TRACK THE EVENT --
```

### Sign up Event (Membership)

***// Android***
```
Bundle params = new Bundle()
	params.putString(Param.METHOD, method);
	
	firebaseAnalytics.logEvent(Event.SIGN_UP, params);
```

***// iOS***
```
Analytics.logEvent(AnalyticsEventSignUp, parameters: [
	AnalyticsParameterMethod: method!
])
```
	
***// Facebook***
```
NSDictionary *params = @{
	FBSDKAppEventParameterNameRegistrationMethod : registrationMethod
};

[FBSDKAppEvents logEvent:FBSDKAppEventNameCompletedRegistration
	parameters:params
];
```

### Tutorial Begin Event

***// Android***
```
Bundle params = new Bundle()
	
	firebaseAnalytics.logEvent(Event.TUTORIAL_BEGIN, null);
```

***// iOS***
```
Analytics.logEvent(AnalyticsEventTutorialBegin, parameters: [
	null!
])
```

***// Facebook***
```
ToDo
```

















































