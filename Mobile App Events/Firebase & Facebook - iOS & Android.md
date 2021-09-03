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

















































