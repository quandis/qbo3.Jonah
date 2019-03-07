# QBO3.Jonah

Use Cases:
User 1 will create lists A,B,C
User 2 will create lists D,E
User 3 (QBO) will be granted access to lists A,C,D
User 3 pulls daily:
	List A to launch workflow Z
	List C to launch workflow Y
	List D to launch workflow X

Tech:
QBO
Collection/JonahHome
Collection/JonahiService
Collection/JonahList?List={A}
	Create a Collection for List A
	Create a CollectionMember for each Loan
	Remove any CollectionMember that are not in feed
Collection/JonahProcess?List={A}&MethodSignature={B}&Analyze={All|Delta}
Collection/JonahAutoBind
*Set up Batch Apply job

UI
Contact/Jonah.ashx
API/Contact/Jonah/Process
	CollectionTemplate=Jonah
	ImportTemplate=Jonah
