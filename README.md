# fmpxmlresult2xcdatamodel
FileMaker XML result to XCode/CoreData xcdatamodel, no records involved

This is a PoC( Proof of Concept )

Works fine with all field types; however number field will have to be manually post validated for now.

Note that adding a layout name in the FMPXMLRESULT export; before translating using this XSLT, will make the output more complete. FileMaker does usually skip layout name on exports, if you know when FileMaker actually outputs the layout name, please enlighten me.

<img alt="The Hub Framework" src="FormatUsingLayout.jpg" width="100%" max-width=1008>

How to use this file in terminal
---
xsltproc fmpxmlresult2xcdatamodel.xslt YourTable.fmpxmlresult.xml > TestCoreDataSwift/TestCoreDataSwift/TestCoreDataSwift.xcdatamodeld/TestCoreDataSwift.xcdatamodel/contents
