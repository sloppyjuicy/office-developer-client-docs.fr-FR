---
title: CompareBookmarks, méthode – Exemple (VJ++)
TOCTitle: CompareBookmarks method example (VJ++)
ms:assetid: f36f77ec-e51a-41dc-961f-0ec3166155bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250236(v=office.15)
ms:contentKeyID: 48548671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 355c20d6bec85effbfca9d603ba58095b72c6dfa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602905"
---
# <a name="comparebookmarks-method-example-vj"></a>CompareBookmarks, méthode – Exemple (VJ++)


**S’applique à** : Access 2013, Office 2013

Cet exemple illustre le fonctionnement de la méthode [CompareBookmarks](comparebookmarks-method-ado.md). La valeur relative des signets est rarement requise sauf si un signet particulier présente une caractéristique spéciale.

Désignez une ligne aléatoire d’un objet [Recordset](recordset-object-ado.md) dérivé de la table ***Authors*** comme cible d’une recherche. Affichez ensuite la position de chaque ligne par rapport à cette cible.

```java 
 
// BeginCompareBookmarksJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
import com.ms.com.*; 
 
public class CompareBookmarksX // 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 CompareBookmarksX(); 
 System.exit(0); 
 } 
 
 // CompareBookmarksX function 
 
 static void CompareBookmarksX() 
 { 
 // Define ADO Objects. 
 Recordset rstAuthors = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 int intCount; 
 Variant varTarget = null; 
 int intResult; 
 String strAns; 
 int intDisplaySize = 15; 
 
 try 
 { 
 rstAuthors = new Recordset(); 
 rstAuthors.open("SELECT * FROM authors", 
 strCnn, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TEXT); 
 intCount = rstAuthors.getRecordCount(); 
 System.out.println("Rows in the Recordset = " + 
 Integer.toString(intCount)); 
 
 // Exit if an empty recordset. 
 if(intCount == 0) 
 System.exit(0); 
 
 // Randomize. 
 intCount = (int)(intCount * Math.random()); 
 // Get position between 0 and count-1. 
 System.out.println("\nRandomly chosen row position = " + 
 Integer.toString(intCount)+ "\n"); 
 rstAuthors.move(intCount,new Integer(AdoEnums.Bookmark.FIRST)); // Move row to random position. 
 varTarget = (Variant)rstAuthors.getBookmark(); 
 // Remember the mystery row. 
 intCount = 0; 
 rstAuthors.moveFirst(); 
 
 // Loop through recordset. 
 while(!rstAuthors.getEOF()) 
 { 
 intResult = rstAuthors.compareBookmarks 
 ((Variant)rstAuthors.getBookmark(), varTarget); 
 if(intResult == AdoEnums.Compare.NOTEQUAL) 
 System.out.println("Row " + 
 Integer.toString(intCount) + 
 ": Bookmarks are not equal."); 
 else if(intResult == AdoEnums.Compare.NOTCOMPARABLE) 
 System.out.println("Row " + 
 Integer.toString(intCount) + 
 ": Bookmarks are not comparable."); 
 else 
 { 
 switch(intResult) 
 { 
 case AdoEnums.Compare.LESSTHAN : 
 strAns = "less than"; 
 break; 
 case AdoEnums.Compare.EQUAL : 
 strAns = "equal to"; 
 break; 
 case AdoEnums.Compare.GREATERTHAN : 
 strAns = "greater than"; 
 break; 
 default : 
 strAns = "in error comparing to"; 
 break; 
 } 
 System.out.println("Row position " + 
 Integer.toString(intCount) + 
 " is " + strAns + " the target."); 
 } 
 if(intCount % intDisplaySize == 0 && intCount > 0) 
 { 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 intCount++; 
 rstAuthors.moveNext(); 
 } 
 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
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
 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstAuthors != null) 
 if (rstAuthors.getState() == 1) 
 rstAuthors.close(); 
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
 
// EndCompareBookmarksJ 
```

