---
title: Item, propriété – Exemple (VJ++)
TOCTitle: Item property example (VJ++)
ms:assetid: be6f14f1-5d3e-6b13-00fc-cfea12e89dcf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249923(v=office.15)
ms:contentKeyID: 48547461
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 166896b6b1f5d512d488aff4afd44dfcfc5c1eed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615325"
---
# <a name="item-property-example-vj"></a>Item, propriété – Exemple (VJ++)


**S’applique à** : Access 2013, Office 2013

Cet exemple montre comment la propriété [Item](item-property-ado.md) accède aux membres d’une collection. L’exemple ouvre la table ***Authors** _ de la base de données _ *_Pubs_** avec une commande paramétisée.

Le paramètre de la commande émise sur la base de données est accédé à partir de la collection [Parameters](command-object-ado.md) de l'objet [Command](parameters-collection-ado.md) par index et par nom. Les champs de l'objet [Recordset](recordset-object-ado.md) retourné sont ensuite accédés à partir de la collection [Fields](fields-collection-ado.md) de cet objet par index et par nom.

```java 
 
// BeginItemJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
import com.ms.com.*; 
 
public class ItemX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 ItemX(); 
 System.exit(0); 
 } 
 
 // ItemX function 
 
 static void ItemX() 
 { 
 
 // Define ADO Objects. 
 Connection cnConn1 = null; 
 Recordset rstAuthors = null; 
 Command cmd = null; 
 Parameter prm = null; 
 Field fld = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 Variant [] varColumn = null; 
 int intIndex; 
 int intLimit; 
 
 try 
 { 
 cnConn1 = new Connection(); 
 rstAuthors = new Recordset(); 
 cmd = new Command(); 
 
 // Set the array with the Authors table field (column) names. 
 varColumn = new Variant[9]; 
 varColumn[0] = new Variant("au_id"); 
 varColumn[1] = new Variant("au_lname"); 
 varColumn[2] = new Variant("au_fname"); 
 varColumn[3] = new Variant("phone"); 
 varColumn[4] = new Variant("address"); 
 varColumn[5] = new Variant("city"); 
 varColumn[6] = new Variant("state"); 
 varColumn[7] = new Variant("zip"); 
 varColumn[8] = new Variant("contract"); 
 
 cmd.setCommandText("SELECT * FROM Authors WHERE state = ?"); 
 prm = cmd.createParameter("ItemXparm", 
 AdoEnums.DataType.CHAR, 
 AdoEnums.ParameterDirection.INPUT, 
 2, 
 "CA"); 
 cmd.getParameters().append(prm); 
 
 cnConn1.open(strCnn); 
 cmd.setActiveConnection(cnConn1); 
 
 // Connection and CommandType are omitted 
 // because a Command Object is provided. 
 rstAuthors.open(cmd, 
 null , 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.READONLY); 
 
 System.out.println( 
 "The Parameters collection accessed by index..."); 
 prm = cmd.getParameters().getItem(0); 
 System.out.println("Parameter name = '" + 
 prm.getName() + 
 "', value = '" + 
 prm.getValue().toString() + "'\n"); 
 
 System.out.println( 
 "The Parameters collection accessed by name..."); 
 prm = cmd.getParameters().getItem("ItemXparm"); 
 System.out.println("Parameters name = '" + 
 prm.getName() + 
 "', value = '" + 
 prm.getValue().toString() + "'\n"); 
 System.out.println("Press <Enter> to continue.."); 
 in.readLine(); 
 
 System.out.println( 
 "The Fields collection accessed by index..."); 
 rstAuthors.moveFirst(); 
 intLimit = rstAuthors.getFields().getCount() - 1; 
 for(intIndex = 0; intIndex <= intLimit; intIndex++) 
 { 
 fld = rstAuthors.getFields().getItem(intIndex); 
 short intVtType = fld.getValue().getvt(); 
 String strFieldValue; 
 switch(intVtType) 
 { 
 case Variant.VariantString : 
 strFieldValue = fld.getValue().toString(); 
 break; 
 case Variant.VariantBoolean : 
 if(fld.getValue().getBoolean()) 
 strFieldValue = "True"; 
 else 
 strFieldValue = "False"; 
 break; 
 default : 
 strFieldValue = fld.getValue().toString(); 
 break; 
 } 
 System.out.println("Field " + 
 Integer.toString(intIndex) + 
 " : Name = '" + 
 fld.getName() + 
 "', value = '" + 
 strFieldValue + 
 "'"); 
 } 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 System.out.println("The Fields collection accessed by name..."); 
 rstAuthors.moveFirst(); 
 for(intIndex = 0; intIndex <= 8; intIndex++) 
 { 
 fld = rstAuthors.getFields().getItem 
 (varColumn[intIndex].toString()); 
 short intVtType = fld.getValue().getvt(); 
 String strFieldValue; 
 switch(intVtType) 
 { 
 case Variant.VariantString : 
 strFieldValue = fld.getValue().toString(); 
 break; 
 case Variant.VariantBoolean : 
 if(fld.getValue().getBoolean()) 
 strFieldValue = "True"; 
 else 
 strFieldValue = "False"; 
 break; 
 default : 
 strFieldValue = fld.getValue().toString(); 
 break; 
 } 
 System.out.println("Field " + 
 "name = '" + 
 fld.getName() + 
 "', value = '" + 
 strFieldValue + 
 "'"); 
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
// EndItemJ 
```

