---
title: "Update email"
description: "Update the properties of an email object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update email
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of an [email](../resources/email.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /security/emailEvent/emails/{emailId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
[!INCLUDE [table-intro](../../includes/update-property-table-intro.md)]


|Property|Type|Description|
|:---|:---|:---|
|createdDateTime|DateTimeOffset|**TODO: Add Description** Required.|
|networkMessageId|String|**TODO: Add Description** Required.|
|internetMessageId|String|**TODO: Add Description** Required.|
|senderEmailFromAddress|String|**TODO: Add Description** Required.|
|senderFromAddress|String|**TODO: Add Description** Required.|
|senderDisplayName|String|**TODO: Add Description** Required.|
|returnPath|String|**TODO: Add Description** Required.|
|senderIPv4|String|**TODO: Add Description** Required.|
|recipientEmailAddress|String|**TODO: Add Description** Required.|
|subject|String|**TODO: Add Description** Required.|
|clusterId|String|**TODO: Add Description** Required.|
|directionality|directionality|**TODO: Add Description**. The possible values are: `inbound`, `outbound`, `intraOrg`. Required.|
|originalDeliveryAction|deliveryAction|**TODO: Add Description**. The possible values are: `delivered`, `deliveredToJunk`, `blocked`, `replaced`. Required.|
|latestDeliveryLocation|deliveryLocation|**TODO: Add Description**. The possible values are: `inboxOrFolder`, `onPremisesOrExternal`, `junk`, `quarantine`, `failed`, `dropped`, `deletedItems`. Required.|
|threatType|threatType|**TODO: Add Description**. The possible values are: `spam`, `malware`, `phish`, `none`. Required.|
|detectionMethod|detectionMethod|**TODO: Add Description**. The possible values are: `generalFilter`, `impersonationBrand`, `spoofExternalDomain`, `spoofDmarc`, `impersonationDomain`, `fileDetonation`, `fileReputation`, `fileDetonationReputation`, `fingerPrintMatching`, `mailboxIntelligenceImpersonation`, `domainReputation`, `spoofIntraOrg`, `advancedFilter`, `antiMalwareEngine`, `mixedAnalysisDetection`, `urlMaliciousReputation`, `urlDetonation`, `urlDetonationReputation`, `impersonationUser`, `campaign`. Required.|
|threatDetail|[threatDetail](../resources/threatdetail.md)|**TODO: Add Description** Required.|
|pishConfidenceLevel|String|**TODO: Add Description** Required.|
|spamConfidenceLevel|String|**TODO: Add Description** Required.|
|policyAction|emailActionPolicy|**TODO: Add Description**. The possible values are: `moveMessageToJunkMailFolder`, `addXHeader`, `modifySubject`, `deleteMessage`, `sendToQuarantine`, `noActionTaken`, `bccMessage`, `redirectMessage`. Required.|
|policy|emailPolicy|**TODO: Add Description**. The possible values are: `antispam`, `antiSpamHighConfidence`, `antiPhishingSpoof`, `antiPhishingDomainImpersonation`, `antiPhishingUserImpersonation`, `antiMalware`, `safeAttachments`, `exchangeTransportRule`, `antiPhishingGraphImpersonation`, `antiSpamBulkMail`, `antiSpamPhishing`. Required.|
|attachmentCount|String|**TODO: Add Description** Required.|
|urlCount|String|**TODO: Add Description** Required.|
|language|String|**TODO: Add Description** Required.|
|connector|String|**TODO: Add Description** Required.|
|recipientTag|String|**TODO: Add Description** Required.|
|senderTag|String|**TODO: Add Description** Required.|
|alertId|String|**TODO: Add Description** Required.|
|submissionId|String|**TODO: Add Description** Required.|
|junkMailboxRule|String|**TODO: Add Description** Required.|
|bulkComplaintLevel|String|**TODO: Add Description** Required.|
|dmarc|String|**TODO: Add Description** Required.|
|dkim|String|**TODO: Add Description** Required.|
|spf|String|**TODO: Add Description** Required.|
|compositeAuthentication|String|**TODO: Add Description** Required.|
|attachment|String|**TODO: Add Description** Required.|
|url|String|**TODO: Add Description** Required.|
|override|String|**TODO: Add Description** Required.|
|distributionList|String|**TODO: Add Description** Required.|
|senderEmailFromDomain|String|**TODO: Add Description** Required.|
|senderFromDomain|String|**TODO: Add Description** Required.|
|domainOwner|String|**TODO: Add Description** Required.|
|domainCreationDate|String|**TODO: Add Description** Required.|
|location|String|**TODO: Add Description** Required.|
|exchangeTransportRule|String|**TODO: Add Description** Required.|
|originalDeliveryLocation|deliveryLocation|**TODO: Add Description**. The possible values are: `inboxOrFolder`, `onPremisesOrExternal`, `junk`, `quarantine`, `failed`, `dropped`, `deletedItems`. Required.|



## Response

If successful, this method returns a `200 OK` response code and an updated [email](../resources/email.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_email"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/security/emailEvent/emails/{emailId}
Content-Type: application/json
Content-length: 1462

{
  "@odata.type": "#microsoft.graph.email",
  "networkMessageId": "String",
  "internetMessageId": "String",
  "senderEmailFromAddress": "String",
  "senderFromAddress": "String",
  "senderDisplayName": "String",
  "returnPath": "String",
  "senderIPv4": "String",
  "recipientEmailAddress": "String",
  "subject": "String",
  "clusterId": "String",
  "directionality": "String",
  "originalDeliveryAction": "String",
  "latestDeliveryLocation": "String",
  "threatType": "String",
  "detectionMethod": "String",
  "threatDetail": {
    "@odata.type": "microsoft.graph.threatDetail"
  },
  "pishConfidenceLevel": "String",
  "spamConfidenceLevel": "String",
  "policyAction": "String",
  "policy": "String",
  "attachmentCount": "String",
  "urlCount": "String",
  "language": "String",
  "connector": "String",
  "recipientTag": "String",
  "senderTag": "String",
  "alertId": "String",
  "submissionId": "String",
  "junkMailboxRule": "String",
  "bulkComplaintLevel": "String",
  "dmarc": "String",
  "dkim": "String",
  "spf": "String",
  "compositeAuthentication": "String",
  "attachment": "String",
  "url": "String",
  "override": "String",
  "distributionList": "String",
  "senderEmailFromDomain": "String",
  "senderFromDomain": "String",
  "domainOwner": "String",
  "domainCreationDate": "String",
  "location": "String",
  "exchangeTransportRule": "String",
  "originalDeliveryLocation": "String"
}
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.email",
  "id": "39b5b8db-b8db-39b5-dbb8-b539dbb8b539",
  "createdDateTime": "String (timestamp)",
  "networkMessageId": "String",
  "internetMessageId": "String",
  "senderEmailFromAddress": "String",
  "senderFromAddress": "String",
  "senderDisplayName": "String",
  "returnPath": "String",
  "senderIPv4": "String",
  "recipientEmailAddress": "String",
  "subject": "String",
  "clusterId": "String",
  "directionality": "String",
  "originalDeliveryAction": "String",
  "latestDeliveryLocation": "String",
  "threatType": "String",
  "detectionMethod": "String",
  "threatDetail": {
    "@odata.type": "microsoft.graph.threatDetail"
  },
  "pishConfidenceLevel": "String",
  "spamConfidenceLevel": "String",
  "policyAction": "String",
  "policy": "String",
  "attachmentCount": "String",
  "urlCount": "String",
  "language": "String",
  "connector": "String",
  "recipientTag": "String",
  "senderTag": "String",
  "alertId": "String",
  "submissionId": "String",
  "junkMailboxRule": "String",
  "bulkComplaintLevel": "String",
  "dmarc": "String",
  "dkim": "String",
  "spf": "String",
  "compositeAuthentication": "String",
  "attachment": "String",
  "url": "String",
  "override": "String",
  "distributionList": "String",
  "senderEmailFromDomain": "String",
  "senderFromDomain": "String",
  "domainOwner": "String",
  "domainCreationDate": "String",
  "location": "String",
  "exchangeTransportRule": "String",
  "originalDeliveryLocation": "String"
}
```
