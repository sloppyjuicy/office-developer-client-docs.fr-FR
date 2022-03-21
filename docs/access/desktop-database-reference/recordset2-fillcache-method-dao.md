---
title: Recordset2.FillCache, méthode (DAO)
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
ms.localizationpriority: medium
ms.openlocfilehash: d7852d1732f84642edc9a457e7be9c30c70b9903
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63629782"
---
# <a name="recordset2fillcache-method-dao"></a>Recordset2.FillCache, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Remplit tout ou partie d'un cache local pour un objet **Recordset** contenant les données d'une source de données ODBC connectée au moteur de base de données Microsoft Access (bases de données ODBC connectées au moteur de base de données Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*.* FillCache(***Rows** _, _*_StartBookmark_**)

*expression* Variable qui représente un **objet Recordset2** .

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Rows</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (sous-type <strong>Integer</strong>) qui spécifie le nombre de lignes à stocker dans le cache. Si vous omettez cet argument, la valeur est déterminée par le paramètre de la propriété <strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>StartBookmark</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (sous-type <strong>String</strong>) qui spécifie un signet. Le cache est rempli à partir de l’enregistrement indiqué par ce signet. Si vous ne spécifiez pas cet argument, le cache est rempli à partir de l’enregistrement indiqué par la propriété <strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

La mise en cache améliore les performances des applications qui extraient les données d'un serveur distant. Le cache est un espace au niveau de la mémoire locale qui conserve les dernières données à avoir été extraites du serveur, en partant du postulat que les données seront probablement redemandées pendant l'exécution de l'application. Lorsqu'un utilisateur demande des données, le moteur de base de données Microsoft Access vérifie d'abord si ces données se trouvent dans le cache avant de les extraire directement du serveur, ce qui prend plus de temps. Le cache stocke uniquement les données issues d'une source de données ODBC.

Au lieu d'attendre que le cache ne se remplisse d'enregistrements à mesure de leur extraction, vous pouvez utiliser la méthode **FillCache** pour remplir à tout moment le cache de façon explicite. Cela permet de remplir le cache plus rapidement dans la mesure où **FillCache** extrait plusieurs enregistrements à la fois, et non un seul. Par exemple, lorsque vous consultez chaque page-écran d'enregistrements, votre application utilise **FillCache** pour extraire la prochaine page-écran d'enregistrements à consulter.

Les sources de données ODBC connectées au moteur de base de données Microsoft Access auxquelles vous accédez et qui comportent des objets **Recordset** peuvent disposer d'un cache local. Pour créer le cache, ouvrez un objet **Recordset** de la source de données distante, puis définissez les propriétés **CacheSize** et **CacheStart** de l'objet **Recordset**.

Si des lignes et un startbookmark créent une plage d’enregistrements partiellement ou entièrement en dehors de la plage d’enregistrements spécifiée par les propriétés **CacheSize** et **CacheStart** , la partie du jeu d’enregistrements en dehors de cette plage est ignorée et ne sera pas chargée dans le cache.

Si **FillCache** demande plus d'enregistrements qu'il n'en reste dans la source de données distante, le moteur de base de données Microsoft Access n'extrait que les enregistrements restants, et aucune erreur ne se produit.

> [!NOTE]
> - Les enregistrements extraits du cache ne reflètent pas les modifications concomitantes que d'autres utilisateurs ont éventuellement apportées à la source de données.
> - **FillCache** extrait uniquement les enregistrements qui ne sont pas déjà en cache. Pour forcer une mise à jour de toutes les données mises en cache, définissez la valeur de la propriété **CacheSize** de l'objet **Recordset** à 0, redéfinissez-la en lui attribuant la taille du cache que vous avez demandée initialement, puis utilisez **FillCache**.

## <a name="example"></a>Exemple

Cet exemple utilise les méthodes **CreateTableDef** et **FillCache** ainsi que les propriétés **CacheSize**, **CacheStart** et **SourceTableName** pour énumérer deux fois les enregistrements dans une table liée. Ensuite, il énumère également deux fois les enregistrements avec un cache de 50 enregistrements. Enfin, il affiche les statistiques de performance pour les deux exécutions, avec et sans mise en cache, dans la table liée.

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
