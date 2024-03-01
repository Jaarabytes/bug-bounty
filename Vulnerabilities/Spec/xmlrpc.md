The xmlrpc.php file (only accepts POST requests, yes?)

Send this:
<?xml version="1.0" encoding="utf-8" ?>
<?methodCall>
<?methodName>system.listMethods</methodName>
<?params></params>
<?/methodCall>
**Remove the question marks from the start**

Also:
System.MultiCall,getCapabilities,liistMethods
pmpto.getMemberLevelForUser,hasMembershipAccess
demo.sayHello,addTwoNumbers
