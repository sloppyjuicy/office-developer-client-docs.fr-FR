---
<span data-ttu-id="0d34c-101"><<<<<<< Titre tête : TOCTitle MaxRecords, propriété-Exemple (VJ ++) : MaxRecords, propriété-Exemple (VJ ++) === titre : MaxRecords, propriété-Exemple (VJ ++) TOCTitle : MaxRecords, propriété-Exemple (VJ ++)</span><span class="sxs-lookup"><span data-stu-id="0d34c-101"><<<<<<< HEAD title: MaxRecords Property Example (VJ++) TOCTitle: MaxRecords Property Example (VJ++) ======= title: MaxRecords property example (VJ++) TOCTitle: MaxRecords property example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="0d34c-102">Master ms:assetid : db8c1187-5e15-2c8a-6308-3468c113d962 ms:mtpsurl : https://msdn.microsoft.com/library/JJ250107(v=office.15) ms:contentKeyID : ms.date 48548106 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="0d34c-102">master ms:assetid: db8c1187-5e15-2c8a-6308-3468c113d962 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250107(v=office.15) ms:contentKeyID: 48548106 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="0d34c-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="0d34c-103"><<<<<<< HEAD</span></span>
# <a name="maxrecords-property-example-vj"></a><span data-ttu-id="0d34c-104">MaxRecords, propriété - Exemple (VJ++)</span><span class="sxs-lookup"><span data-stu-id="0d34c-104">MaxRecords Property Example (VJ++)</span></span>
=======
# <a name="maxrecords-property-example-vj"></a><span data-ttu-id="0d34c-105">MaxRecords, propriété-Exemple (VJ ++)</span><span class="sxs-lookup"><span data-stu-id="0d34c-105">MaxRecords property example (VJ++)</span></span>
>>>>>>> <span data-ttu-id="0d34c-106">master</span><span class="sxs-lookup"><span data-stu-id="0d34c-106">master</span></span>


<span data-ttu-id="0d34c-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d34c-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0d34c-108">Cet exemple utilise la propriété [MaxRecords](maxrecords-property-ado.md) pour ouvrir un [Recordset](recordset-object-ado.md) contenant les 10 titres les plus coûteux de la table ***Titles***.</span><span class="sxs-lookup"><span data-stu-id="0d34c-108">This example uses the [MaxRecords](maxrecords-property-ado.md) property to open a [Recordset](recordset-object-ado.md) containing the 10 most expensive titles in the ***Titles*** table.</span></span>

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

