---
title: Sort, propriété – Exemple (VJ++)
TOCTitle: Sort property example (VJ++)
ms:assetid: 29f34b9d-a75a-baa3-2505-ebd70e71950f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249051(v=office.15)
ms:contentKeyID: 48543896
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 64e7b6f1481b263b4002d25545a5ae36f3d42de6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621814"
---
# <a name="sort-property-example-vj"></a>Sort, propriété – Exemple (VJ++)


**S’applique à** : Access 2013, Office 2013

Cet exemple utilise la propriété [Sort](sort-property-ado.md) de l’objet [Recordset](recordset-object-ado.md) pour réorder les lignes d’un jeu **d’enregistrements** dérivé de la table Authors _ de la base de données ***_*_Pubs._** Une routine utilitaire secondaire imprime chaque ligne.

```java 
 
// BeginSortJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class SortX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 SortX(); 
 System.exit(0); 
 } 
 
 // SortX function 
 
 static void SortX() 
 { 
 // Define ADO Objects. 
 Connection cnConn1 = null; 
 Recordset rstAuthors = null; 
 
 // Declarations. 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 try 
 { 
 cnConn1 = new Connection(); 
 cnConn1.open(strCnn); 
 rstAuthors = new Recordset(); 
 rstAuthors.setCursorLocation(AdoEnums.CursorLocation.CLIENT); 
 rstAuthors.open("SELECT * FROM Authors", 
 cnConn1, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TEXT); 
 SortXprint("Initial Order",rstAuthors); 
 
 rstAuthors.setSort("au_lname ASC, au_fname ASC"); 
 SortXprint("Last Name Ascending",rstAuthors); 
 
 rstAuthors.setSort("au_lname DESC, au_fname ASC"); 
 SortXprint("Last Name Descending",rstAuthors); 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstAuthors != null) 
 { 
 PrintProviderError(rstAuthors.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstAuthors != null) 
 if (rstAuthors.getState() == 1) 
 rstAuthors.close(); 
 if (cnConn1 != null) 
 if (cnConn1.getState() == 1) 
 cnConn1.close(); 
 } 
 
 } 
 
 // SortXprint function 
 
 static void SortXprint(String strTitle,Recordset rstp) 
 { 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 int intDisplaysize = 15; 
 int intCount = 1; 
 try 
 { 
 System.out.println("---------------" + 
 strTitle + 
 "---------------"); 
 System.out.println("First Name Last Name" + "\n" + 
 "-------------------------" + 
 "-------------------------"); 
 rstp.moveFirst(); 
 while(!rstp.getEOF()) 
 { 
 System.out.println(rstp.getField("au_fname").getString() + 
 " " + 
 rstp.getField("au_lname").getString()); 
 if(intCount % intDisplaysize == 0) 
 { 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 intCount = 0; 
 } 
 intCount++; 
 rstp.moveNext(); 
 } 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstp != null) 
 { 
 PrintProviderError(rstp.getActiveConnection()); 
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
// EndSortJ 
```

