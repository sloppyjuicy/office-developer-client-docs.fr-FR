---
title: Propriété QueryDef.ReturnsRecords (DAO)
TOCTitle: ReturnsRecords Property
ms:assetid: 3d1e538b-4d60-588f-4a20-89f1e2b434e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192701(v=office.15)
ms:contentKeyID: 48544334
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053005
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 66905394b0bf7127e952c9fe17860e84a151a3b0
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937602"
---
# <a name="querydefreturnsrecords-property-dao"></a><span data-ttu-id="a6d5a-102">Propriété QueryDef.ReturnsRecords (DAO)</span><span class="sxs-lookup"><span data-stu-id="a6d5a-102">QueryDef.ReturnsRecords property (DAO)</span></span>


<span data-ttu-id="a6d5a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6d5a-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="a6d5a-104">Définit ou renvoie une valeur indiquant si une requête SQL directe sur une base de données externe renvoie des enregistrements (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="a6d5a-104">Sets or returns a value that indicates whether an SQL pass-through query to an external database returns records (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="a6d5a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6d5a-105">Syntax</span></span>

<span data-ttu-id="a6d5a-106">*expression* . ReturnsRecords</span><span class="sxs-lookup"><span data-stu-id="a6d5a-106">*expression* .ReturnsRecords</span></span>

<span data-ttu-id="a6d5a-107">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="a6d5a-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6d5a-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="a6d5a-108">Remarks</span></span>

<span data-ttu-id="a6d5a-p101">Les requêtes SQL directes envoyées à des bases de données externes ne peuvent pas toutes renvoyer des enregistrements. Par exemple, une instruction SQL UPDATE met à jour des enregistrements sans en renvoyer tandis qu'une instruction SQL SELECT en renvoie. Si la requête renvoie des enregistrements, affectez à la propriété **ReturnsRecords** la valeur **True**; dans le cas contraire, affectez à **ReturnsRecords** la valeur **False**.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-p101">Not all SQL pass-through queries to external databases return records. For example, an SQL UPDATE statement updates records without returning records, while an SQL SELECT statement does return records. If the query returns records, set the **ReturnsRecords** property to **True**; if the query doesn't return records, set the **ReturnsRecords** property to **False**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a6d5a-112">[!REMARQUE] Vous devez définir la propriété <STRONG><A href="querydef-connect-property-dao.md">Connect</A></STRONG> avant la propriété <STRONG>ReturnsRecords</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-112">You must set the <STRONG><A href="querydef-connect-property-dao.md">Connect</A></STRONG> property before you set the <STRONG>ReturnsRecords</STRONG> property.</span></span></P>



## <a name="example"></a><span data-ttu-id="a6d5a-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="a6d5a-113">Example</span></span>

<span data-ttu-id="a6d5a-p102">Cet exemple utilise les propriétés **Connect** et **ReturnsRecords** pour sélectionner les cinq titres de livre les mieux vendus dans une base de données Microsoft SQL Server en fonction des ventes de l'année réalisées jusqu'à ce jour. Dans le cas d'un résultat identique dans les chiffres de vente, l'exemple augmente la taille de la liste affichant les résultats de la requête et en explique la raison.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-p102">This example uses the **Connect** and **ReturnsRecords** properties to select the top five book titles from a Microsoft SQL Server database based on year-to-date sales amounts. In the event of an exact match in sales amounts, the example increases the size of the list displaying the results of the query and prints a message explaining why this occurred.</span></span>

```vb 
Sub ClientServerX1() 
 
 Dim dbsCurrent As Database 
 Dim qdfPassThrough As QueryDef 
 Dim qdfLocal As QueryDef 
 Dim rstTopFive As Recordset 
 Dim strMessage As String 
 
 ' Open a database from which QueryDef objects can be 
 ' created. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a pass-through query to retrieve data from 
 ' a Microsoft SQL Server database. 
 Set qdfPassThrough = _ 
 dbsCurrent.CreateQueryDef("AllTitles") 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfPassThrough.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfPassThrough.SQL = "SELECT * FROM titles " & _ 
 "ORDER BY ytd_sales DESC" 
 qdfPassThrough.ReturnsRecords = True 
 
 ' Create a temporary QueryDef object to retrieve 
 ' data from the pass-through query. 
 Set qdfLocal = dbsCurrent.CreateQueryDef("") 
 qdfLocal.SQL = "SELECT TOP 5 title FROM AllTitles" 
 
 Set rstTopFive = qdfLocal.OpenRecordset() 
 
 ' Display results of queries. 
 With rstTopFive 
 strMessage = _ 
 "Our top 5 best-selling books are:" & vbCr 
 
 Do While Not .EOF 
 strMessage = strMessage & " " & !Title & _ 
 vbCr 
 .MoveNext 
 Loop 
 
 If .RecordCount > 5 Then 
 strMessage = strMessage & _ 
 "(There was a tie, resulting in " & _ 
 vbCr & .RecordCount & _ 
 " books in the list.)" 
 End If 
 
 MsgBox strMessage 
 .Close 
 End With 
 
 ' Delete new pass-through query because this is a 
 ' demonstration. 
 dbsCurrent.QueryDefs.Delete "AllTitles" 
 dbsCurrent.Close 
 
```

<br/>

<span data-ttu-id="a6d5a-116">Cet exemple utilise la propriété **ReturnsRecords** et la propriété personnalisée **LogMessages** pour créer une requête SQL directe qui renverra les données et les messages éventuellement générés par le serveur distant.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-116">This example uses the **ReturnsRecords** property and the custom **LogMessages** property to create a pass-through query that will return data and any messages generated by the remote server.</span></span>

```vb 
Sub LogMessagesX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsCurrent As Database 
 Dim qdfTemp As QueryDef 
 Dim prpNew As Property 
 Dim rstTemp As Recordset 
 
 ' Create Microsoft Access Workspace object. 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 
 Set dbsCurrent = wrkAcc.OpenDatabase("DB1.mdb") 
 
 ' Create a QueryDef that will log any messages from the 
 ' server in temporary tables. 
 Set qdfTemp = dbsCurrent.CreateQueryDef("NewQueryDef") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfTemp.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfTemp.SQL = "SELECT * FROM stores" 
 qdfTemp.ReturnsRecords = True 
 Set prpNew = qdfTemp.CreateProperty("LogMessages", _ 
 dbBoolean, True) 
 qdfTemp.Properties.Append prpNew 
 
 ' Execute query and display results. 
 Set rstTemp = qdfTemp.OpenRecordset() 
 
 Debug.Print "Contents of recordset:" 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 ' Delete new QueryDef because this is a demonstration. 
 dbsCurrent.QueryDefs.Delete qdfTemp.Name 
 dbsCurrent.Close 
 wrkAcc.Close 
 
End Sub 
 
```

