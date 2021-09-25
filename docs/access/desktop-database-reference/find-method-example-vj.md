---
title: Find, méthode – Exemple (VJ++)
TOCTitle: Find method example (VJ++)
ms:assetid: 622abf93-01f2-7721-4ca5-54c2c773089b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249367(v=office.15)
ms:contentKeyID: 48545232
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 450aa9bba66c3d2ce3fb737feeaa8a5425843852
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568998"
---
# <a name="find-method-example-vj"></a>Find, méthode – Exemple (VJ++)


**S’applique à** : Access 2013, Office 2013

Cet exemple utilise la méthode [Find](find-method-ado.md) de l’objet [Recordset](recordset-object-ado.md) pour localiser et compter le nombre de titres de fonctions dans la base de données ***Pubs***. Il est supposé, dans l'exemple, que le fournisseur sous-jacent ne prend pas en charge de fonctionnalité similaire.

```java 
 
// BeginFindJ 
// The WFC class includes the ADO objects. 
import com.ms.wfc.data.*; 
import java.io.* ; 
import com.ms.com.*; 
 
public class FindX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 FindX(); 
 System.exit(0); 
 } 
 
 // FindX function 
 
 static void FindX() 
 { 
 
 // Define ADO Objects. 
 Connection cnConn1 = null; 
 Recordset rstTitles = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 Variant varMark = null; 
 int intCount = 0; 
 
 try 
 { 
 cnConn1 = new Connection(); 
 cnConn1.open(strCnn); 
 rstTitles = new Recordset(); 
 rstTitles.open("SELECT title_id FROM titles", 
 cnConn1, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TEXT); 
 
 // The default parameters are sufficient to search forward 
 // through a Recordset. 
 rstTitles.find("title_id LIKE 'BU%'"); 
 
 // Skip current record to avoid finding the same row repeatedly. 
 // The bookmark is redundant because Find searches from current 
 // position. 
 while(!rstTitles.getEOF()) // Continue if last find succeeded. 
 { 
 System.out.println("Title ID: " 
 + rstTitles.getField("title_id").getString()); 
 intCount++; // Count the last title found. 
 varMark = (Variant)rstTitles.getBookmark(); 
 // Note current position. 
 rstTitles.find("title_id LIKE 'BU%'", 
 1, 
 AdoEnums.SearchDirection.FORWARD, 
 varMark); 
 } 
 
 System.out.println("\nThe number of business titles is " + 
 Integer.toString(intCount)); 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
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
 
 // System read requires this catch. 
 catch( java.io.IOException je) 
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
 
 // PrintIOError Function 
 
 static void PrintIOError( java.io.IOException je) 
 { 
 System.out.println("Error \n"); 
 System.out.println("\tSource = " + je.getClass() + "\n"); 
 System.out.println("\tDescription = " + je.getMessage() + "\n"); 
 } 
} 
// EndFindJ 
```

