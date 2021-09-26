---
title: Delete, méthode – Exemple (VJ++)
TOCTitle: Delete method example (VJ++)
ms:assetid: 052238ed-86e1-c104-2be6-4bbf45474db5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248810(v=office.15)
ms:contentKeyID: 48543026
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7e5b05e8e81513c713167d18b514fbecfdf0b746
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59632069"
---
# <a name="delete-method-example-vj"></a>Delete, méthode – Exemple (VJ++)


**S’applique à** : Access 2013, Office 2013

Cet exemple utilise la méthode [Delete](delete-method-ado-recordset.md) pour supprimer un enregistrement spécifié d'un objet [Recordset](recordset-object-ado.md).

```java 
 
// BeginDeleteJ 
// The WFC class includes the ADO objects. 
 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class DeleteX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 DeleteX(); 
 System.exit(0); 
 } 
 
 // DeleteX function 
 
 static void DeleteX() 
 { 
 
 // Define ADO Objects. 
 Recordset rstRoySched = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String line = null; 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 String strMessage=""; 
 String strTitleID; 
 int intLoRange =0; 
 int intHiRange =0; 
 int intRoyalty =0; 
 boolean bolFound; 
 
 try 
 { 
 rstRoySched = new Recordset(); 
 rstRoySched.setCursorLocation(AdoEnums.CursorLocation.CLIENT); 
 rstRoySched.setCursorType(AdoEnums.CursorType.STATIC); 
 rstRoySched.setLockType(AdoEnums.LockType.BATCHOPTIMISTIC); 
 
 // Open RoySched table. 
 rstRoySched.open("SELECT * FROM roysched " + 
 "WHERE royalty = 20", strCnn, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.BATCHOPTIMISTIC, 
 AdoEnums.CommandType.TEXT); 
 
 // Prompt for a record to delete. 
 strMessage = "Before delete there are " 
 + rstRoySched.getRecordCount() 
 + " titles with 20 percent royalty:" + "\n\n"; 
 while(!rstRoySched.getEOF()) 
 { 
 strMessage += rstRoySched.getField("title_id").getString() + 
 "\n\n"; 
 rstRoySched.moveNext(); 
 } 
 strMessage += "Enter the ID of a record to delete:" + "\n"; 
 System.out.println(strMessage); 
 strTitleID = in.readLine().trim().toUpperCase(); 
 
 // Move to the record and save data so it can be restored. 
 rstRoySched.setFilter("title_id = '" + strTitleID + "'"); 
 if(!(rstRoySched.getRecordCount()==0)) 
 { 
 intLoRange = rstRoySched.getField("lorange").getInt(); 
 intHiRange = rstRoySched.getField("hirange").getInt(); 
 intRoyalty = rstRoySched.getField("royalty").getInt(); 
 bolFound = true; 
 } 
 else 
 { 
 System.out.println("\nIncorrect ID. No Record deleted." ); 
 bolFound = false; 
 } 
 
 // Delete the record. 
 if(bolFound) 
 { 
 rstRoySched.delete(); 
 rstRoySched.updateBatch(); 
 } 
 // Show the results. 
 rstRoySched.setFilter(new Integer(AdoEnums.FilterGroup.NONE)); 
 rstRoySched.requery(); 
 strMessage =""; 
 strMessage = "\n\nAfter delete there are " 
 + rstRoySched.getRecordCount() 
 + " titles with 20 percent royalty:" + "\n\n"; 
 while(!rstRoySched.getEOF()) 
 { 
 strMessage += rstRoySched.getField("title_id").getString() + 
 "\n\n"; 
 rstRoySched.moveNext(); 
 } 
 System.out.println(strMessage); 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 // Restore the data because this is a demonstration. 
 if(bolFound) 
 { 
 rstRoySched.addNew(); 
 rstRoySched.getField("title_id").setString(strTitleID); 
 rstRoySched.getField("lorange").setInt(intLoRange); 
 rstRoySched.getField("hirange").setInt(intHiRange); 
 rstRoySched.getField("royalty").setInt(intRoyalty); 
 rstRoySched.updateBatch(); 
 } 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstRoySched != null) 
 { 
 PrintProviderError(rstRoySched.getActiveConnection()); 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 
 } 
 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstRoySched != null) 
 if (rstRoySched.getState() == 1) 
 rstRoySched.close(); 
 } 
 
 } 
 
 // PrintProviderError Function 
 
 static void PrintProviderError( Connection Cnn1 ) 
 { 
 // Print Provider errors from Connection object. 
 // ErrItem is an item object in the Connections Errors collection. 
 com.ms.wfc.data.Error ErrItem = null; 
 long nCount = 0; 
 int i = 0; 
 
 nCount = Cnn1.getErrors().getCount(); 
 
 // If there are any errors in the collection, print them. 
 if( nCount > 0); 
 { 
 // Collection ranges from 0 to nCount - 1 
 for (i = 0; i< nCount; i++) 
 { 
 ErrItem = Cnn1.getErrors().getItem(i); 
 System.out.println("\t Error number: " + ErrItem.getNumber() 
 + "\t" + ErrItem.getDescription() ); 
 } 
 } 
 
 } 
 
 // PrintIOError Function 
 
 static void PrintIOError( java.io.IOException je) 
 { 
 System.out.println("Error \n"); 
 System.out.println("\tSource = " + je.getClass() + "\n"); 
 System.out.println("\tDescription = " + je.getMessage() + "\n"); 
 } 
} 
 
// EndDeleteJ 
```

