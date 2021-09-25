---
title: Status, propriété – Exemple (VJ++)
TOCTitle: Status property example (VJ++)
ms:assetid: bdfc1b26-b384-e7e5-ff4b-d63ed62f70ca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249922(v=office.15)
ms:contentKeyID: 48547452
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a6d1d5e319d1abc986519ab3fa6c2232fc16517d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568368"
---
# <a name="status-property-example-vj"></a>Status, propriété – Exemple (VJ++)


**S’applique à** : Access 2013, Office 2013

Cet exemple utilise la propriété [Status](status-property-ado-recordset.md) pour afficher les enregistrements ayant été modifiés dans une opération par lot avant la réalisation d'une mise à jour par lot.

```java 
 
// BeginStatusJ 
import java.io.*; 
import com.ms.wfc.data.*; 
 
public class StatusX 
{ 
 // The main entry point of the application. 
 
 public static void main (String[] args) 
 { 
 StatusX(); 
 System.exit(0); 
 } 
 // StatusX Function 
 
 static void StatusX() 
 { 
 // Define ADO Objects. 
 Recordset rstTitles = null; 
 
 // Declarations. 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';"+ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 BufferedReader in = 
 new BufferedReader(new InputStreamReader(System.in)); 
 
 try 
 { 
 // Open Recordset for batch update. 
 rstTitles = new Recordset(); 
 rstTitles.setCursorType(AdoEnums.CursorType.KEYSET); 
 rstTitles.setLockType(AdoEnums.LockType.BATCHOPTIMISTIC); 
 rstTitles.open("Titles", strCnn, AdoEnums.CursorType.KEYSET, 
 AdoEnums.LockType.BATCHOPTIMISTIC, 
 AdoEnums.CommandType.TABLE); 
 
 // Change the type of psychology titles. 
 while(!rstTitles.getEOF()) 
 { 
 if(rstTitles.getField("Type").getString().trim(). 
 equals(new String("psychology"))) 
 rstTitles.getField("Type").setString("self_help"); 
 
 rstTitles.moveNext(); 
 } 
 
 // Display Title ID and status. 
 rstTitles.moveFirst(); 
 
 while(!rstTitles.getEOF()) 
 { 
 if(rstTitles.getStatus()==AdoEnums.RecordStatus.MODIFIED) 
 System.out.println(rstTitles.getField("title_id"). 
 getString() + "- Modified"); 
 else 
 System.out.println(rstTitles.getField("title_id"). 
 getString()); 
 rstTitles.moveNext(); 
 } 
 
 // Cancel the update because this is a demonstration. 
 rstTitles.cancelBatch(); 
 
 System.out.println("Press <Enter> to continue.."); 
 in.readLine(); 
 } 
 catch(AdoException ae) 
 { 
 // Notify the user of any errors that result from ADO. 
 
 // As passing a Recordset, check for the null pointer first. 
 if(rstTitles != null) 
 { 
 PrintProviderError(rstTitles.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 // System read requires this catch. 
 catch(java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstTitles != null) 
 if (rstTitles.getState() == 1) 
 rstTitles.close(); 
 } 
 } 
 // PrintProviderError Function 
 static void PrintProviderError(Connection cnn1) 
 { 
 // Print Provider Errors from Connection Object. 
 // ErrItem is an item object in the Connections Errors Collection. 
 com.ms.wfc.data.Error ErrItem = null; 
 long nCount = 0; 
 int i = 0; 
 
 nCount = cnn1.getErrors().getCount(); 
 
 // If there are any errors in the collection, print them. 
 if ( nCount > 0) 
 { 
 // Collection ranges from 0 to nCount-1. 
 for ( i=0;i<nCount; i++) 
 { 
 ErrItem = cnn1.getErrors().getItem(i); 
 System.out.println("\t Error Number: " + ErrItem.getNumber() 
 + "\t" + ErrItem.getDescription()); 
 } 
 } 
 } 
 // PrintIOError Function 
 static void PrintIOError(java.io.IOException je) 
 { 
 System.out.println("Error: \n"); 
 System.out.println("\t Source: " + je.getClass() + "\n"); 
 System.out.println("\t Description: "+ je.getMessage() + "\n"); 
 } 
} 
// EndStatusJ 
```

