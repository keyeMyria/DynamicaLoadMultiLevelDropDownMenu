# DynamicaLoadMultiLevelDropDownMenu
Angular 2 dynamically load multi-level drop down menu


How to run?
After download, go to folder

npm install

npm start

demo :http://plnkr.co/edit/wLqLUoBQYgcDwOgSoRfF?p=preview
*********************************************************************
After plnkr demo opened, Click "launch preview in a separate windows" button at right top. squeeze edge of screen slowly and we can see menu line up for mobile devices.
Now if you drage edge of screen slower to increese size of screen, untill centain time, screen large enough and menu will be back as tablet/ipad/desktop screen automatically then release screen edge, then when you put your cursor on level1 -> level2 -> level3 and you can see "my page" is pup up inside the screen.
********************************************************************
Question to angular team, when we can have this kind of smartmenu in ng2, not as jquery plugin?

**********************************************************************

Ok, Angular2 component router cannot solve my problem. 
I have hundreds pages on a web site and don't want my users to make lots of clicks on router componet then find,  they are not sure where to go, they don't even know which pannel to start with(This is your problem ng2 componet router!).

Make things worse, business want to decide which web pages to show after users logon.

Currently, jquery smartmenus (https://github.com/vadikom/smartmenus, http://www.smartmenus.org/) can be help for first part of problem. it is mobile/tablet/ipad user friendly as well(I will explain more later on). Thanks Smartmenus! My https://github.com/Longfld/DynamicalRouter  can solve second part of issue.

Now, our chanllege is to plug in jquery smartmenu into existing ng2 application.

It all starts from https://github.com/Longfld/DynamicalRouter.

Add a Output EventEmitter in MyRouterLink to tell its parent router links have been added.
Its parrent componet app.component will call  $('#main-menu').smartmenus() after get the message.


********************************************************

Here is smartmenus domo: http://plnkr.co/edit/GhgAWHv78qerLDcKgKDm?p=preview
