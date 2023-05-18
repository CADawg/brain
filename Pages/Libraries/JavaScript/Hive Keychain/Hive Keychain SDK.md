NPM: [NPM - Hive Keychain SDK](https://www.npmjs.com/package/keychain-sdk)

### Signing A Challenge (Login):
```jsx
function GenerateChallenge(username: string) {  
	// unix seconds expiry (5 minutes)  
	const expiry = Math.floor(Date.now() / 1000) + 300;  
  
	return JSON.stringify({  
		username: username,  
		type: "login",  
		app: "appname",  
		expiry: expiry  
	});  
}  
  
function GetSignBuffer(username: string): SignBuffer {  
	const challenge = GenerateChallenge(username);  
	  
	return {  
			username: username,  
			message: challenge,  
			method: KeychainKeyTypes.active,  
			title: "Login to appname"  
	}  
}
```

### Detecting Keychain (With #Firefox Support)
```jsx
useEffect(() => {  
	keychain.isKeychainInstalled().then((result) => {  
		setHasKeychain(true);  
		  
		let attemptCount = 0;  
		  
		// Fix for firefox (keychain takes a small amount of time to load)  
		if (!result) {  
			const interval = setInterval(() => {  
					keychain.isKeychainInstalled().then((result) => {  
					setHasKeychain(result);  
					  
					if (result || attemptCount > 100) {  
						clearInterval(interval);  
					}  
					  
					attemptCount++;  
				});  
			}, 10);  
		}  
	});  
});
```

#HiveKeychain