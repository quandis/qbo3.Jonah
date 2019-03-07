# QBO3.Jonah

Use Cases:
1.	User 1 will create lists A,B,C
2.	User 2 will create lists D,E
3.	User 3 (QBO) will be granted access to lists A,C,D
4.	User 3 pulls daily:
	o	List A to launch workflow Z
	o	list C to launch workflow Y
	o	list D to launch workflow X

Tech:
QBO
Collection/JonahHome
Collection/JonahiService
Collection/JonahList?List={A}
-Create a Collection for List A
-Create a CollectionMember for each Loan
-Remove any CollectionMember that are not in feed
Collection/JonahProcess?List={A}&MethodSignature={B}&Analyze={All|Delta}
Collection/JonahAutoBind
*Set up Batch Apply job

UI:
Contact/Jonah.ashx
API/Contact/Jonah/Process
-CollectionTemplate=Jonah
-ImportTemplate=Jonah
