---
title: MaxRecords, propriété – Exemple (VJ++)
TOCTitle: MaxRecords property example (VJ++)
ms:assetid: db8c1187-5e15-2c8a-6308-3468c113d962
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250107(v=office.15)
ms:contentKeyID: 48548106
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7783cbf6b5e2d9b7722bbc5d5840eeaea8101ece
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558274"
---
# <a name="maxrecords-property-example-vj"></a>MaxRecords, propriété – Exemple (VJ++)


**S’applique à** : Access 2013, Office 2013

Cet exemple utilise la propriété [MaxRecords](maxrecords-property-ado.md) pour ouvrir un [Recordset](recordset-object-ado.md) contenant les 10 titres les plus coûteux de la table ***Titles***.

```java 
 
// BeingMaxRecordsJ 
import java.io.*; 
import com.ms.wfc.data.*; 
 
public class MaxRecordsX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 MaxRecordsX(); 
 System.exit(0); 
 } 
 // MaxRecordsX Function 
 
 static void MaxRecordsX() 
 { 
 // Define ADO Objects 
 Recordset rstTemp = null; 
 
 try 
 { 
 // Declarations 
 BufferedReader in = 
 new BufferedReader(new InputStreamReader(System.in)); 
 
 // Open recordset containing the 10 most expensive 
 // titles in the Titles table. 
 String strCnn = " Provider='sqloledb';Data Source='MySqlServer';"+ 
 " Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 rstTemp = new Recordset(); 
 rstTemp.setMaxRecords(10); 
 rstTemp.open("select title,price from Titles" + 
 " order by price desc", strCnn,AdoEnums.CursorType.FORWARDONLY, 
 AdoEnums.LockType.READONLY, AdoEnums.CommandType.TEXT); 
 
 // Display the contents of the recordset. 
 System.out.println("Top Ten Titles by Price:\n"); 
 while (!rstTemp.getEOF()) 
 { 
 System.out.println(" "+ rstTemp.getField("title").getString() + 
 " - " + rstTemp.getField("Price").getString()); 
 rstTemp.moveNext(); 
 } 
 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 
 catch(AdoException ae) 
 { 
 // Notify the user of any errors that result from ADO. 
 
 // As passing a connection, check for null pointer first. 
 if (rstTemp!=null) 
 { 
 PrintProviderError(rstTemp.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getLocalizedMessage()); 
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
 if (rstTemp != null) 
 if (rstTemp.getState() == 1) 
 rstTemp.close(); 
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
// EndMaxRecordsJ 
```

