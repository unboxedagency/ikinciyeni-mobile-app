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

### Tutorial Complete Event

***// Android***
```
firebaseAnalytics.logEvent(Event.TUTORIAL_COMPLETE, null);
```

***// iOS***
```
Analytics.logEvent(AnalyticsEventTutorialComplete, parameters: [
	null!
])
```

***// Facebook***
```
ToDo
```

## Custom Events Events

### Carwizz Event

***// Android***
```
Bundle carArray = new Bundle()
	//The car details
	carArray.putDouble(Param.PRICE, price); // The valuation price, or 0 if Fail
	carArray.putString(Param.ITEM_ID, item_id);
	carArray.putString(Param.ITEM_BRAND, item_brand); // The car brand, for example 'Renault'
	carArray.putString(Param.ITEM_CATEGORY, item_category); // The car model, for example 'Clio'
	carArray.putString(Param.ITEM_CATEGORY2, item_category2); // The car body type, for example 'Sedan'
	carArray.putString(Param.ITEM_CATEGORY3, item_category3); // The car year, for example '2011'
	carArray.putString(Param.ITEM_CATEGORY4, item_category4); // The car trnsmission, for example 'Otomatik'
	carArray.putString(Param.ITEM_CATEGORY5, item_category5); // The car fule, for example 'Benzin'
	carArray.putString(Param.ITEM_VARIANT, item_variant); // TBD
	
Bundle params = new Bundle()
	params.putParcelableArray(Param.ITEMS, new Bundle[] {carArray});
	params.putString('cp_carwizz_step', cp_carwizz_step); // The incremetal step, for example, 1, 2, 3... (777 for Success, 999 for Fail)
	params.putString('cp_car_package', cp_car_package); // The car package, for example '30 Tfsi 116 Hp Dynamic Str Sback Pi+ Prestige Paket'
	params.putInteger('cp_car_horse_power', cp_car_horse_power); // The car horse poer, for example '150'
	params.putInteger('cp_car_mileage', cp_car_mileage); // The car mileage, for example '25000'
	params.putInteger('cp_car_damage_report', cp_car_damage_report);
	params.putInteger('cp_car_equipment', cp_car_equipment);
	params.putInteger(Param.SUCCESS); // The Carwizz Valuation reuslt, for example 1 for Success, 0 for Fail
	params.putString(Param.CURRENCY, currency); // 'TRY'
	params.putDouble(Param.VALUE, value); // The valuation estimate, for example '150000' (or 0 for Fail)
	
	firebaseAnalytics.logEvent('carwizz', params);
```

***// iOS***
```
ToDo
```
	
***// Facebook***
```
ToDo
```

### Expertise Apointment Event

***// Android***
```
Bundle params = new Bundle()
	params.putString('cp_sales_method', cp_sales_method);
	
	firebaseAnalytics.logEvent('expertise_apointment', params);
```

***// iOS***
```
Analytics.logEvent('expertise_appointment', parameters: [
	'cp_sales_type': cp_sales_type!
])
```
	
***// Facebook***
```
ToDo
```

### Send To Dealer Event

***// Android***
```
firebaseAnalytics.logEvent('send_to_dealer, null);
```

***// iOS***
```
Analytics.logEvent('send_to_dealer', parameters: [
	null!
])
```

***// Facebook***
```
ToDo
```

















































