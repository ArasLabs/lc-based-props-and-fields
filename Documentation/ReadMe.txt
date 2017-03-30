Author:
-------
Rolf Laudenbach (rlaudenbach@aras.com)

Version:
--------
v1-3 (Nov 2012)


Description (Life Cycle Based Properties and Form Fields)
---------------------------------------------------------
It is common that properties defined by ItemType should also be checked as required properties based on a Life Cycle state
It is also common that visibility and disabled status of data fields (bound to properties) on a form can be controlled 
by Life Cylce State and/or defined Identities (User Groups)

Rather than writing custom logic for the above behavior a generic logic and data model is introduced to read addtional 
property configurations. To do so the data model of „Property-relationships“ and „Life Cycle Transition“ was extended.
The generic methods with „Validation“ logic can then be used on pre-Transition Actions and of Form event "OnFormPopulate"


Dependencies:
-------------
-depends on some methods from the "Common Utititites" package.
-data model add-on to core itemtype "Life Cycle Transition" (3 Properties)


Setup:
-------
After importing the basic parts no checks and form field handling will be activated.
For life-cycle based property checking, you have to add method "LC PreTransition Handler" to the pre-action of the
transitions to validate. 2 addional custom method could be added for subsequent custom logic.
Then for each property to check you have to edit the property on its source itemType (i.e. the "Document")
There you can add the checking rules for each life cycle transition. 
There you also can add behaviors (disabled, visible) of form fields connected to this property.

To enable the rule base generic form field handling. you must add a new method to the Form event "onFormPopulate"
You can clone the method "xxx" used on the Document form (added by this package).
Reuse the generic function "AAA" that calls a server side methods to return the field rules registered by Form name.



available as Community Project
------------------------------
No


available separetely on Partner Portal
--------------------------------------
No


Notice of Liability
-------------------
The information contained in this document and the import packages are distributed on an "As Is" basis, 
without warranty of any kind, express or implied, including, but not limited to, the implied warranties 
of merchantability and fitness for a particular purpose or a warranty of non-infringement. Aras shall have 
no liability to any person or entity with respect to any loss or damage caused or alleged to be caused 
directly or indirectly by the information contained in this document or by the software or hardware products 
described herein.

  