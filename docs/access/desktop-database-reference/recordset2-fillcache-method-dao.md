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
ms.openlocfilehash: ef0f4ad298e316cbae295bcf4f6c4c5349b18655
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998531"
---
# <a name="recordset2fillcache-method-dao"></a>Méthode Recordset2.FillCache (DAO)

**S’applique à**: Access 2013, Office 2013

Remplit une partie ou l'ensemble d'un cache local pour un objet **Recordset** qui contient des données d'une source de données ODBC connectée au moteur de base de données Microsoft Access (bases de données ODBC connectées au moteur de base de données Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . FillCache (***lignes***, ***signetdébut***)

*expression* Variable qui représente un objet **Recordset2** .

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Requis/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Rows</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p><strong>Variant</strong> (sous-type <strong>Integer</strong>) qui spécifie le nombre de lignes à stocker dans le cache. Si vous omettez cet argument, la valeur est déterminée par le paramètre de la propriété <strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>Signetdébut</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p><strong>Variant</strong> (sous-type <strong>String</strong>) qui spécifie un signet. Le cache est rempli à partir de l’enregistrement indiqué par ce signet. Si vous ne spécifiez pas cet argument, le cache est rempli à partir de l’enregistrement indiqué par la propriété <strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

La mise en cache améliore les performances d'une application qui récupère des données d'un serveur distant. Un cache représente un espace dans la mémoire locale qui conserve les données les plus récentes, extraites du serveur. Il est supposé en effet que les données feront probablement l'objet d'autres demandes tant que l'application est en cours d'exécution. Lorsqu'un utilisateur demande des données, le moteur de base de données Microsoft Access recherche d'abord les données dans le cache avant de tenter de les récupérer sur le serveur, ce qui prend plus longtemps. Le cache n'enregistre pas les données qui ne proviennent pas d'une source de données ODBC.

Au lieu d'attendre que le cache se remplisse progressivement d'enregistrements au fur et à mesure de leur extraction, vous pouvez utiliser la méthode **FillCache** pour remplir explicitement le cache au moment voulu. Cette méthode offre un moyen plus rapide de remplir le cache dans la mesure où **FillCache** extrait simultanément plusieurs enregistrements et non un à la fois. Par exemple, lorsque vous consultez différents écrans d'enregistrements, votre application utilise la méthode **FillCache** pour extraire le prochain écran d'enregistrements à afficher.

Toute source de données ODBC connectée au moteur de base de données Microsoft Access à laquelle vous accédez à l'aide d'objets **Recordset** peut posséder un cache local. Pour créer le cache, ouvrez un objet **Recordset** à partir de la source de données distante puis définissez les propriétés **CacheSize** et **CacheStart** de l'objet **Recordset**.

Si les lignes et signetdébut créent une plage d’enregistrements qui sont partiellement ou entièrement en dehors de la plage spécifiée par les propriétés **CacheSize** et **CacheStart** , la partie de l’objet recordset en dehors de cette plage est ignorée et ne sera pas chargée dans le cache.

Si **FillCache** demande davantage d'enregistrements que le nombre encore présent dans la source de données distante, le moteur de base de données Microsoft Access extrait uniquement les enregistrements restants et aucune erreur n'est générée.

> [!NOTE]
> - Les enregistrements extraits du cache ne reflètent pas les modifications simultanées effectuées par d'autres utilisateurs aux données de la source.
> - **FillCache** extrait uniquement les enregistrements qui ne sont pas encore mis en cache. Pour forcer la mise à jour de toutes les données en cache, affectez la valeur 0 à la propriété **CacheSize** de l'objet **Recordset**, réinitialisez le cache à la taille initialement demandée puis utilisez la méthode **FillCache**.

## <a name="example"></a>Exemple

Cet exemple utilise les méthodes **CreateTableDef** et **FillCache** ainsi que les propriétés **CacheSize**, **CacheStart** et **SourceTableName** pour énumérer deux fois les enregistrements dans une table liée. Ensuite, il énumère également deux fois les enregistrements avec un cache de 50 enregistrements. Enfin, il affiche les statistiques de performance pour les deux exécutions, avec et sans mise en cache, dans la table liée.

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
