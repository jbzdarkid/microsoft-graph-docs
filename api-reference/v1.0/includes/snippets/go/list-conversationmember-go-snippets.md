---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


result, err := graphClient.TeamsById("team-id").ChannelsById("channel-id").SharedWithTeamsById("sharedWithChannelTeamInfo-id").AllowedMembers().Get(context.Background(), nil)


```