---
title: Recordset. FillCache, méthode (DAO)
TOCTitle: FillCache Method
ms:assetid: d171b939-b904-c6bd-6217-68bc2814e282
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834751(v=office.15)
ms:contentKeyID: 48547861
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ef268a821d65732e0a54776872387f62c67e999
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300517"
---
# <a name="recordsetfillcache-method-dao"></a><span data-ttu-id="3faa1-102">Recordset. FillCache, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="3faa1-102">Recordset.FillCache method (DAO)</span></span>

<span data-ttu-id="3faa1-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3faa1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3faa1-104">Remplit tout ou partie d'un cache local pour un objet **Recordset** contenant les données d'une source de données ODBC connectée au moteur de base de données Microsoft Access (bases de données ODBC connectées au moteur de base de données Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="3faa1-104">Fills all or a part of a local cache for a **Recordset** object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span>

## <a name="syntax"></a><span data-ttu-id="3faa1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3faa1-105">Syntax</span></span>

<span data-ttu-id="3faa1-106">*expression* . FillCache (***Rows***, ***signetdébut***)</span><span class="sxs-lookup"><span data-stu-id="3faa1-106">*expression* .FillCache(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="3faa1-107">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="3faa1-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="3faa1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3faa1-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3faa1-109">Nom</span><span class="sxs-lookup"><span data-stu-id="3faa1-109">Name</span></span></p></th>
<th><p><span data-ttu-id="3faa1-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="3faa1-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="3faa1-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="3faa1-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="3faa1-112">Description</span><span class="sxs-lookup"><span data-stu-id="3faa1-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3faa1-113"><em>Rows</em></span><span class="sxs-lookup"><span data-stu-id="3faa1-113"><em>Rows</em></span></span></p></td>
<td><p><span data-ttu-id="3faa1-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="3faa1-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="3faa1-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3faa1-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3faa1-116"><strong>Variant</strong> (sous-type <strong>Integer</strong>) qui spécifie le nombre de lignes à stocker dans le cache.</span><span class="sxs-lookup"><span data-stu-id="3faa1-116">A <strong>Variant</strong> (<strong>Integer</strong> subtype) that specifies the number of rows to store in the cache.</span></span> <span data-ttu-id="3faa1-117">Si vous omettez cet argument, la valeur est déterminée par le paramètre de la propriété <strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="3faa1-117">If you omit this argument, the value is determined by the <strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong> property setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3faa1-118"><em>Signetdébut</em></span><span class="sxs-lookup"><span data-stu-id="3faa1-118"><em>StartBookmark</em></span></span></p></td>
<td><p><span data-ttu-id="3faa1-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="3faa1-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="3faa1-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3faa1-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3faa1-121"><strong>Variant</strong> (sous-type <strong>String</strong>) qui spécifie un signet.</span><span class="sxs-lookup"><span data-stu-id="3faa1-121">A <strong>Variant</strong> (<strong>String</strong> subtype) that specifies a bookmark.</span></span> <span data-ttu-id="3faa1-122">Le cache est rempli à partir de l’enregistrement indiqué par ce signet.</span><span class="sxs-lookup"><span data-stu-id="3faa1-122">The cache is filled starting from the record indicated by this bookmark.</span></span> <span data-ttu-id="3faa1-123">Si vous omettez cet argument, le cache est rempli à partir de l'enregistrement indiqué par la propriété <strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="3faa1-123">If you omit this argument, the cache is filled starting from the record indicated by the <strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3faa1-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="3faa1-124">Remarks</span></span>

<span data-ttu-id="3faa1-p103">La mise en cache améliore les performances des applications qui extraient les données d'un serveur distant. Le cache est un espace au niveau de la mémoire locale qui conserve les dernières données à avoir été extraites du serveur, en partant du postulat que les données seront probablement redemandées pendant l'exécution de l'application. Lorsqu'un utilisateur demande des données, le moteur de base de données Microsoft Access vérifie d'abord si ces données se trouvent dans le cache avant de les extraire directement du serveur, ce qui prend plus de temps. Le cache stocke uniquement les données issues d'une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="3faa1-p103">Caching improves the performance of an application that retrieves data from a remote server. A cache is space in local memory that holds the data most recently retrieved from the server; this assumes that the data will probably be requested again while the application is running. When a user requests data, the Microsoft Access database engine checks the cache for the data first rather than retrieving it from the server, which takes more time. The cache doesn't save data that doesn't come from an ODBC data source.</span></span>

<span data-ttu-id="3faa1-p104">Au lieu d'attendre que le cache ne se remplisse d'enregistrements à mesure de leur extraction, vous pouvez utiliser la méthode **FillCache** pour remplir à tout moment le cache de façon explicite. Cela permet de remplir le cache plus rapidement dans la mesure où **FillCache** extrait plusieurs enregistrements à la fois, et non un seul. Par exemple, lorsque vous consultez chaque page-écran d'enregistrements, votre application utilise **FillCache** pour extraire la prochaine page-écran d'enregistrements à consulter.</span><span class="sxs-lookup"><span data-stu-id="3faa1-p104">Rather than waiting for the cache to be filled with records as they are retrieved, you can use the **FillCache** method to explicitly fill the cache at any time. This is a faster way to fill the cache because **FillCache** retrieves several records at once instead of one at a time. For example, while you view each screenful of records, your application uses **FillCache** to retrieve the next screenful of records for viewing.</span></span>

<span data-ttu-id="3faa1-p105">Les sources de données ODBC connectées au moteur de base de données Microsoft Access auxquelles vous accédez et qui comportent des objets **Recordset** peuvent disposer d'un cache local. Pour créer le cache, ouvrez un objet **Recordset** de la source de données distante, puis définissez les propriétés **CacheSize** et **CacheStart** de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3faa1-p105">Any Microsoft Access database engine-connected ODBC data source that you access with **Recordset** objects can have a local cache. To create the cache, open a **Recordset** object from the remote data source, and then set the **CacheSize** and **CacheStart** properties of the **Recordset**.</span></span>

<span data-ttu-id="3faa1-134">Si les propriétés Rows et signetdébut créent une plage d'enregistrements entièrement ou partiellement en dehors de la plage d'enregistrements spécifiée par les propriétés **CacheSize** et **CacheStart** , la partie de l'objet Recordset en dehors de cette plage n'est pas prise en compte et ne sera pas chargée. dans le cache.</span><span class="sxs-lookup"><span data-stu-id="3faa1-134">If rows and startbookmark create a range of records that is partially or entirely outside the range of records specified by the **CacheSize** and **CacheStart** properties, the portion of the recordset outside this range is ignored and will not be loaded into the cache.</span></span>

<span data-ttu-id="3faa1-135">Si **FillCache** demande plus d'enregistrements qu'il n'en reste dans la source de données distante, le moteur de base de données Microsoft Access n'extrait que les enregistrements restants, et aucune erreur ne se produit.</span><span class="sxs-lookup"><span data-stu-id="3faa1-135">If **FillCache** requests more records than the number remaining in the remote data source, the Microsoft Access database engine retrieves only the remaining records, and no error occurs.</span></span>

> [!NOTE]
> - <span data-ttu-id="3faa1-136">Les enregistrements extraits du cache ne reflètent pas les modifications concomitantes que d'autres utilisateurs ont éventuellement apportées à la source de données.</span><span class="sxs-lookup"><span data-stu-id="3faa1-136">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>
> - <span data-ttu-id="3faa1-p106">**FillCache** extrait uniquement les enregistrements qui ne sont pas déjà en cache. Pour forcer une mise à jour de toutes les données mises en cache, définissez la valeur de la propriété **CacheSize** de l'objet **Recordset** à 0, redéfinissez-la en lui attribuant la taille du cache que vous avez demandée initialement, puis utilisez **FillCache**.</span><span class="sxs-lookup"><span data-stu-id="3faa1-p106">**FillCache** only retrieves records not already cached. To force an update of all the cached data, set the **CacheSize** property of the **Recordset** to 0, reset it to the size of the cache you originally requested, and then use **FillCache**.</span></span>

## <a name="example"></a><span data-ttu-id="3faa1-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="3faa1-139">Example</span></span>

<span data-ttu-id="3faa1-p107">Cet exemple de code montre comment utiliser les méthodes **CreateTableDef** et **FillCache** et les propriétés **CacheSize** **CacheStart** et **SourceTableName** pour énumérer deux fois les enregistrements d'une table liée. Les enregistrements sont ensuite énumérés deux fois avec un cache constitué de 50 enregistrements. Enfin, les statistiques de performance sont affichées pour les exécutions au niveau de la table liée, sans et avec cache.</span><span class="sxs-lookup"><span data-stu-id="3faa1-p107">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

```vb
    Sub ClientServerX3() 
     
       Dim dbsCurrent As Database 
       Dim tdfRoyalties As TableDef 
       Dim rstRemote As Recordset 
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
