---
title: Méthode Recordset2.FillCache (DAO)
TOCTitle: FillCache Method
ms:assetid: 28a70997-a8d4-73e6-171a-61286e3d3485
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192007(v=office.15)
ms:contentKeyID: 48543864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052942
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d83fea9f8c4e464c0df5f783ca2ab29a8a8e588b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926338"
---
# <a name="recordset2fillcache-method-dao"></a><span data-ttu-id="8041d-102">Méthode Recordset2.FillCache (DAO)</span><span class="sxs-lookup"><span data-stu-id="8041d-102">Recordset2.FillCache method (DAO)</span></span>


<span data-ttu-id="8041d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8041d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8041d-104">Remplit une partie ou l'ensemble d'un cache local pour un objet **Recordset** qui contient des données d'une source de données ODBC connectée au moteur de base de données Microsoft Access (bases de données ODBC connectées au moteur de base de données Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="8041d-104">Fills all or a part of a local cache for a **Recordset** object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span>

## <a name="syntax"></a><span data-ttu-id="8041d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8041d-105">Syntax</span></span>

<span data-ttu-id="8041d-106">*expression* . FillCache (***lignes***, ***signetdébut***)</span><span class="sxs-lookup"><span data-stu-id="8041d-106">*expression* .FillCache(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="8041d-107">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="8041d-107">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="8041d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8041d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8041d-109">Name</span><span class="sxs-lookup"><span data-stu-id="8041d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="8041d-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="8041d-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="8041d-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="8041d-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="8041d-112">Description</span><span class="sxs-lookup"><span data-stu-id="8041d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8041d-113">Lignes</span><span class="sxs-lookup"><span data-stu-id="8041d-113">Rows</span></span></p></td>
<td><p><span data-ttu-id="8041d-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="8041d-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="8041d-115"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="8041d-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8041d-p101"><strong>Variant</strong> (sous-type <strong>Integer</strong>) qui spécifie le nombre de lignes à stocker dans le cache. Si vous omettez cet argument, la valeur est déterminée par le paramètre de la propriété <strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="8041d-p101">A <strong>Variant</strong> (<strong>Integer</strong> subtype) that specifies the number of rows to store in the cache. If you omit this argument, the value is determined by the <strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong> property setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8041d-118">Signetdébut</span><span class="sxs-lookup"><span data-stu-id="8041d-118">StartBookmark</span></span></p></td>
<td><p><span data-ttu-id="8041d-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="8041d-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="8041d-120"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="8041d-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8041d-p102"><strong>Variant</strong> (sous-type <strong>String</strong>) qui spécifie un signet. Le cache est rempli à partir de l’enregistrement indiqué par ce signet. Si vous ne spécifiez pas cet argument, le cache est rempli à partir de l’enregistrement indiqué par la propriété <strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="8041d-p102">A <strong>Variant</strong> (<strong>String</strong> subtype) that specifies a bookmark. The cache is filled starting from the record indicated by this bookmark. If you omit this argument, the cache is filled starting from the record indicated by the <strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8041d-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="8041d-124">Remarks</span></span>

<span data-ttu-id="8041d-p103">La mise en cache améliore les performances d'une application qui récupère des données d'un serveur distant. Un cache représente un espace dans la mémoire locale qui conserve les données les plus récentes, extraites du serveur. Il est supposé en effet que les données feront probablement l'objet d'autres demandes tant que l'application est en cours d'exécution. Lorsqu'un utilisateur demande des données, le moteur de base de données Microsoft Access recherche d'abord les données dans le cache avant de tenter de les récupérer sur le serveur, ce qui prend plus longtemps. Le cache n'enregistre pas les données qui ne proviennent pas d'une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="8041d-p103">Caching improves the performance of an application that retrieves data from a remote server. A cache is space in local memory that holds the data most recently retrieved from the server; this assumes that the data will probably be requested again while the application is running. When a user requests data, the Microsoft Access database engine checks the cache for the data first rather than retrieving it from the server, which takes more time. The cache doesn't save data that doesn't come from an ODBC data source.</span></span>

<span data-ttu-id="8041d-p104">Au lieu d'attendre que le cache se remplisse progressivement d'enregistrements au fur et à mesure de leur extraction, vous pouvez utiliser la méthode **FillCache** pour remplir explicitement le cache au moment voulu. Cette méthode offre un moyen plus rapide de remplir le cache dans la mesure où **FillCache** extrait simultanément plusieurs enregistrements et non un à la fois. Par exemple, lorsque vous consultez différents écrans d'enregistrements, votre application utilise la méthode **FillCache** pour extraire le prochain écran d'enregistrements à afficher.</span><span class="sxs-lookup"><span data-stu-id="8041d-p104">Rather than waiting for the cache to be filled with records as they are retrieved, you can use the **FillCache** method to explicitly fill the cache at any time. This is a faster way to fill the cache because **FillCache** retrieves several records at once instead of one at a time. For example, while you view each screenful of records, your application uses **FillCache** to retrieve the next screenful of records for viewing.</span></span>

<span data-ttu-id="8041d-p105">Toute source de données ODBC connectée au moteur de base de données Microsoft Access à laquelle vous accédez à l'aide d'objets **Recordset** peut posséder un cache local. Pour créer le cache, ouvrez un objet **Recordset** à partir de la source de données distante puis définissez les propriétés **CacheSize** et **CacheStart** de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="8041d-p105">Any Microsoft Access database engine-connected ODBC data source that you access with **Recordset** objects can have a local cache. To create the cache, open a **Recordset** object from the remote data source, and then set the **CacheSize** and **CacheStart** properties of the **Recordset**.</span></span>

<span data-ttu-id="8041d-134">Si les lignes et signetdébut créent une plage d’enregistrements qui sont partiellement ou entièrement en dehors de la plage spécifiée par les propriétés **CacheSize** et **CacheStart** , la partie de l’objet recordset en dehors de cette plage est ignorée et ne sera pas chargée dans le cache.</span><span class="sxs-lookup"><span data-stu-id="8041d-134">If rows and startbookmark create a range of records that is partially or entirely outside the range of records specified by the **CacheSize** and **CacheStart** properties, the portion of the recordset outside this range is ignored and will not be loaded into the cache.</span></span>

<span data-ttu-id="8041d-135">Si **FillCache** demande davantage d'enregistrements que le nombre encore présent dans la source de données distante, le moteur de base de données Microsoft Access extrait uniquement les enregistrements restants et aucune erreur n'est générée.</span><span class="sxs-lookup"><span data-stu-id="8041d-135">If **FillCache** requests more records than the number remaining in the remote data source, the Microsoft Access database engine retrieves only the remaining records, and no error occurs.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="8041d-136">Les enregistrements extraits du cache ne reflètent pas les modifications simultanées effectuées par d'autres utilisateurs aux données de la source.</span><span class="sxs-lookup"><span data-stu-id="8041d-136">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span></P>
> <LI>
> <P><span data-ttu-id="8041d-p106"><STRONG>FillCache</STRONG> extrait uniquement les enregistrements qui ne sont pas encore mis en cache. Pour forcer la mise à jour de toutes les données en cache, affectez la valeur 0 à la propriété <STRONG>CacheSize</STRONG> de l'objet <STRONG>Recordset</STRONG>, réinitialisez le cache à la taille initialement demandée puis utilisez la méthode <STRONG>FillCache</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="8041d-p106"><STRONG>FillCache</STRONG> only retrieves records not already cached. To force an update of all the cached data, set the <STRONG>CacheSize</STRONG> property of the <STRONG>Recordset</STRONG> to 0, reset it to the size of the cache you originally requested, and then use <STRONG>FillCache</STRONG>.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="8041d-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="8041d-139">Example</span></span>

<span data-ttu-id="8041d-p107">Cet exemple utilise les méthodes **CreateTableDef** et **FillCache** ainsi que les propriétés **CacheSize**, **CacheStart** et **SourceTableName** pour énumérer deux fois les enregistrements dans une table liée. Ensuite, il énumère également deux fois les enregistrements avec un cache de 50 enregistrements. Enfin, il affiche les statistiques de performance pour les deux exécutions, avec et sans mise en cache, dans la table liée.</span><span class="sxs-lookup"><span data-stu-id="8041d-p107">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

```vb
    Sub ClientServerX3() 
     
       Dim dbsCurrent As Database 
       Dim tdfRoyalties As TableDef 
       Dim rstRemote As Recordset2 
       Dim sngStart As Single 
       Dim sngEnd As Single 
       Dim sngNoCache As Single 
       Dim sngCache As Single 
       Dim intLoop As Integer 
       Dim strTemp As String 
       Dim intRecords As Integer 
     
       ' Open a database to which a linked table can be  
       ' appended. 
       Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
       ' Create a linked table that connects to a Microsoft SQL 
       ' Server database. 
       Set tdfRoyalties = _ 
          dbsCurrent.CreateTableDef("Royalties") 
       ' Note: The DSN referenced below must be set to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
       tdfRoyalties.Connect = _ 
          "ODBC;DATABASE=pubs;DSN=Publishers" 
       tdfRoyalties.SourceTableName = "roysched" 
       dbsCurrent.TableDefs.Append tdfRoyalties 
       Set rstRemote = _ 
          dbsCurrent.OpenRecordset("Royalties") 
     
       With rstRemote 
          ' Enumerate the Recordset object twice and record 
          ' the elapsed time. 
          sngStart = Timer 
     
          For intLoop = 1 To 2 
             .MoveFirst 
             Do While Not .EOF 
                ' Execute a simple operation for the 
                ' performance test. 
                strTemp = !title_id 
                .MoveNext 
             Loop 
          Next intLoop 
     
          sngEnd = Timer 
          sngNoCache = sngEnd - sngStart 
     
          ' Cache the first 50 records. 
          .MoveFirst 
          .CacheSize = 50 
          .FillCache 
          sngStart = Timer 
     
          ' Enumerate the Recordset object twice and record 
          ' the elapsed time. 
          For intLoop = 1 To 2 
             intRecords = 0 
             .MoveFirst 
             Do While Not .EOF 
                ' Execute a simple operation for the 
                ' performance test. 
                strTemp = !title_id 
                ' Count the records. If the end of the 
                ' cache is reached, reset the cache to the 
                ' next 50 records. 
                intRecords = intRecords + 1 
                .MoveNext 
                If intRecords Mod 50 = 0 Then 
                   .CacheStart = .Bookmark 
                   .FillCache 
                End If 
             Loop 
          Next intLoop 
     
          sngEnd = Timer 
          sngCache = sngEnd - sngStart 
     
          ' Display performance results. 
          MsgBox "Caching Performance Results:" & vbCr & _ 
             "  No cache: " & Format(sngNoCache, _ 
             "##0.000") & " seconds" & vbCr & _ 
             "  50-record cache: " & Format(sngCache, _ 
             "##0.000") & " seconds" 
          .Close 
       End With 
     
       ' Delete linked table because this is a demonstration. 
       dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
       dbsCurrent.Close 
     
    End Sub
```
