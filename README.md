# fmpxmlresult2xcdatamodel
FileMaker XML result to XCode/CoreData xcdatamodel, no records involved

This is a PoC( Proof of Concept )

Works fine with all field types; however number field will have to be manually post validated for now.

Note that adding a layout name in the FMPXMLRESULT export; before translating using this XSLT, will make the output more complete. FileMaker does usually skip layout name on exports, if you know when FileMaker actually outputs the layout name, please enlighten me.

<img alt="[x] Format Using Layout will provoke the export to populate the LAYOUT-attribute" src="FormatUsingLayout.png" width="100%" max-width=1008>

How to use this file in terminal
---
xsltproc fmpxmlresult2xcdatamodel.xslt YourTable.fmpxmlresult.xml > TestCoreDataSwift/TestCoreDataSwift/TestCoreDataSwift.xcdatamodeld/TestCoreDataSwift.xcdatamodel/contents

Use case
---
I use this stylesheet to generate CoreData local cache Entities with Attributes

License
=======

Copyright (c) 2015 Gjermund Gusland Thorsen, released under the MIT License.

All rights deserved.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

This piece of software comes with ABSOLUTELY NO WARRANTY, to the extent permitted by applicable law.
