---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)

requestBody := graphmodels.NewExternalGroup()
id := "31bea3d537902000"
requestBody.SetId(&id) 
displayName := "Contoso Marketing"
requestBody.SetDisplayName(&displayName) 
description := "The product marketing team"
requestBody.SetDescription(&description) 

result, err := graphClient.External().ConnectionsById("externalConnection-id").Groups().Post(context.Background(), requestBody, nil)


```