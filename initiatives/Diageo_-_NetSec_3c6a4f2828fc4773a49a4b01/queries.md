Allow Internet Inboud - All NSG Rules 


#AzureNetworkAnalytics_CL |  where ResourceType == "NetworkSecurityGroupRule"
| where SourceAddressPrefix_s == "Internet" | where Access_s  contains "Allow"



#Allow Internet OutBout - All NSG Rules 

AzureNetworkAnalytics_CL |  where ResourceType == "NetworkSecurityGroupRule"
| where DestinationAddressPrefix_s == "Internet" | where Access_s  contains "Allow"
