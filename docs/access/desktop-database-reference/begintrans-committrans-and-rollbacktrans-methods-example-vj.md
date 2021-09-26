---
title: BeginTrans, CommitTrans, RollbackTrans, méthodes - Exemple (VJ++)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans methods example (VJ++)
ms:assetid: 8c1ca470-792e-4792-8913-fa7d3b46218f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249616(v=office.15)
ms:contentKeyID: 48546229
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b318b89e69088dec2e2df51a1d943d28a6bf5bae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607100"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-example-vj"></a>BeginTrans, CommitTrans et RollbackTrans, méthodes – Exemple (VJ++)


**S’applique à** : Access 2013, Office 2013

Cet exemple modifie le type de livre de tous les livres de la table ***Titles** _ de la base de données. Une fois [que la méthode BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) démarre une transaction qui isole toutes les modifications apportées à la table _ *_Titles_** , la méthode [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) enregistre les modifications. You can use the [Rollback](begintrans-committrans-and-rollbacktrans-methods-ado.md) method to undo changes that you saved using the [Update](update-method-ado.md) method.

```java 
 
// BeginBeginTransJ 
import com.ms.wfc.data.*; 
import java.io.*; 
 
public class BeginTransX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 BeginTransX(); 
 System.exit(0); 
 } 
 
 // BeginTransX function 
 static void BeginTransX() 
 { 
 // Define ADO Objects. 
 Connection cnConn1 = null; 
 Recordset rstTitles = null; 
 
 //Declarations. 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 String strTitle; 
 String strType; 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader (System.in)); 
 String line = null; 
 String strMessage=""; 
 int intChoice = 0; 
 int recordDisplaySize = 15; 
 int recordCount = 0; 
 
 try 
 { 
 // Open a connection. 
 
 cnConn1 = new Connection(); 
 cnConn1.open(strCnn,"","",AdoEnums.CommandType.UNSPECIFIED); 
 
 // Open the Titles table. 
 rstTitles = new Recordset (); 
 rstTitles.setCursorType(AdoEnums.CursorType.DYNAMIC); 
 rstTitles.setLockType(AdoEnums.LockType.PESSIMISTIC); 
 rstTitles.open("titles",cnConn1,AdoEnums.CursorType.DYNAMIC , 
 AdoEnums.LockType.PESSIMISTIC ,AdoEnums.CommandType.TABLE ); 
 
 rstTitles.moveFirst(); 
 cnConn1.beginTrans(); 
 
 // Loop through recordset and ask user if he/she wants 
 // to change the type for a specified title. 
 
 while (!rstTitles.getEOF()) 
 { 
 strType = rstTitles.getField("type").getString().trim(); 
 if ((rstTitles.getField("type").getString(). 
 trim()).compareTo("psychology")== 0) 
 { 
 strTitle = rstTitles.getField("title").getString().trim(); 
 System.out.println("\nTitle : " + strTitle + "\n\n" 
 + "Change type to self help (1 -> Yes / 2 -> No) ?"); 
 // Change the title for the specified book. 
 line = in.readLine().trim(); 
 intChoice = Integer.parseInt(line); 
 if ( intChoice == 1) 
 { 
 rstTitles.getField("type").setString("self_help"); 
 rstTitles.update(); 
 } 
 } 
 rstTitles.moveNext(); 
 } 
 
 // Ask if the user wants to commit to all the 
 // changes made above. 
 System.out.println 
 ("\n\nSave all changes (1 -> Yes / 2 -> No) ?"); 
 line = in.readLine().trim(); 
 intChoice = Integer.parseInt(line); 
 if ( intChoice == 1) 
 cnConn1.commitTrans(); 
 else 
 cnConn1.rollbackTrans(); 
 
 // Print current data in recordset. 
 rstTitles.requery(); 
 rstTitles.moveFirst(); 
 
 while(true) 
 { 
 strMessage = strMessage +"\n " + 
 rstTitles.getField("title").getString()+" - " 
 + rstTitles.getField("type").getString() ; 
 
 if ( recordCount == recordDisplaySize) 
 { 
 System.out.println(strMessage); 
 System.out.println("\n\nPress <Enter> key to continue.."); 
 line = in.readLine(); 
 strMessage = ""; 
 recordCount = 0; 
 } 
 recordCount++; 
 rstTitles.moveNext(); 
 if(rstTitles.getEOF()) 
 { 
 System.out.println(strMessage); 
 break; 
 } 
 } 
 System.out.println("\n\nPress <Enter> key to continue.."); 
 line = in.readLine(); 
 
 // Restore original data because this 
 // is a demonstration. 
 rstTitles.moveFirst(); 
 while (!rstTitles.getEOF()) 
 { 
 if ((rstTitles.getField("type").getString(). 
 trim().compareTo("self_help"))== 0) 
 { 
 rstTitles.getField("type").setString("psychology"); 
 rstTitles.update(); 
 } 
 rstTitles.moveNext(); 
 } 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // Check for null pointer for connection object. 
 if(rstTitles.getActiveConnection()==null) 
 System.out.println("Exception: " + ae.getMessage()); 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstTitles != null) 
 { 
 PrintProviderError(rstTitles.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 // System Read requires this catch. 
 catch( java.io.IOException je ) 
 { 
 PrintIOError(je); 
 } 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstTitles != null) 
 if (rstTitles.getState() == 1) 
 rstTitles.close(); 
 if (cnConn1 != null) 
 if (cnConn1.getState() == 1) 
 cnConn1.close(); 
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
 
 //.PrintIOError Function 
 
 static void PrintIOError( java.io.IOException je) 
 { 
 System.out.println("Error \n"); 
 System.out.println("\tSource = " + je.getClass() + "\n"); 
 System.out.println("\tDescription = " + je.getMessage() + "\n"); 
 } 
} 
 
// EndBeginTransJ 
```

