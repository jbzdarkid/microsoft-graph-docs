---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)

headers := abstractions.NewRequestHeaders()
headers.Add("Prefer", "outlook.timezone=\"Pacific Standard Time\"")

requestParameters := &graphconfig.MeEventItemRequestBuilderGetQueryParameters{
	Select: [] string {"subject","body","bodyPreview","organizer","attendees","start","end","location","hideAttendees"},
}
configuration := &graphconfig.MeEventItemRequestBuilderGetRequestConfiguration{
	Headers: headers,
	QueryParameters: requestParameters,
}

result, err := graphClient.Me().EventsById("event-id").Get(context.Background(), configuration)


```