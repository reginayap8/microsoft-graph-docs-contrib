---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# Code snippets are only available for the latest version. Current version is 1.x
from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.chat_message import ChatMessage
from msgraph_beta.generated.models.item_body import ItemBody
from msgraph_beta.generated.models.body_type import BodyType
from msgraph_beta.generated.models.chat_message_mention import ChatMessageMention
from msgraph_beta.generated.models.chat_message_mentioned_identity_set import ChatMessageMentionedIdentitySet
from msgraph_beta.generated.models.teamwork_tag_identity import TeamworkTagIdentity
# To initialize your graph_client, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=python
request_body = ChatMessage(
	body = ItemBody(
		content_type = BodyType.Html,
		content = "<at id=\"0\">TestTag</at>&nbsp;Testing Tags",
	),
	mentions = [
		ChatMessageMention(
			id = 0,
			mention_text = "TestTag",
			mentioned = ChatMessageMentionedIdentitySet(
				tag = TeamworkTagIdentity(
					id = "MjQzMmI1N2ItMGFiZC00M2RiLWFhN2ItMTZlYWRkMTE1ZDM0IyM2OGEzZTM2NS1mN2Q5LTRhNTYtYjQ5OS0yNDMzMmE5Y2M1NzIjI3RTMERJZ1Z1ZQ==",
					display_name = "TestTag",
				),
			),
		),
	],
)

result = await graph_client.teams.by_team_id('team-id').channels.by_channel_id('channel-id').messages.post(request_body)


```