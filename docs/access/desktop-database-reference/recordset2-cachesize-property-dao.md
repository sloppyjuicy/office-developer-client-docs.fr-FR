---
title: Recordset2.CacheSize, propriété (DAO)
TOCTitle: CacheSize Property
ms:assetid: d8d195cc-6696-0583-31eb-b9988f8b7c6f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835090(v=office.15)
ms:contentKeyID: 48548042
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052927
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: a200c9ecab66b40ff6d9ac8fc474734702d5bdf9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611762"
---
# <a name="recordset2cachesize-property-dao"></a>Recordset2.CacheSize, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie le nombre d'enregistrements extraits d'une source de données ODBC qui seront placés dans le cache local. Valeur **Long** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*.* CacheSize

*expression* Variable qui représente un **objet Recordset2.**

## <a name="remarks"></a>Remarques

La valeur de la propriété **CacheSize** doit être comprise entre 5 et 1200 mais ne peut pas être supérieure à ce que la mémoire disponible autorise. 100 est une valeur communément utilisée. Si la propriété a la valeur 0, la mise en cache est désactivée.

La mise en cache des données améliore les performances si vous utilisez des objets **Recordset** pour extraire des données d'un serveur distant. Un cache est un espace de la mémoire locale qui conserve les données récemment extraites du serveur. La mise en cache est utile si les utilisateurs demandent à nouveau les données au cours de la même session d'application. En cas de demande des données, le moteur de base de données Microsoft Access vérifie si les données demandées figurent dans le cache avant de tenter de les récupérer auprès du serveur, ce qui prend plus longtemps. Le cache enregistre uniquement des données issues d'une source de données ODBC.

N'importe quelle source de données ODBC connectée au moteur de base de données Microsoft Access, telle qu'une table liée, peut posséder un cache local. Pour créer le cache, ouvrez un objet **Recordset** à partir de la source de données distante, définissez les propriétés **CacheSize** et **[CacheStart](recordset2-cachestart-property-dao.md)** puis utilisez la méthode **[FillCache](recordset2-fillcache-method-dao.md)** ou parcourez les enregistrements à l'aide des méthodes **Move**.

Vous pouvez définir le paramètre de la propriété **CacheSize** sur la base du nombre d'enregistrements que votre application est capable de traiter simultanément. Si, par exemple, vous utilisez un objet **Recordset** comme source des données à afficher à l'écran, vous pouvez attribuer à la propriété **CacheSize** la valeur 20 afin d'afficher 20 enregistrements à la fois.

Le moteur de base de données Microsoft Access demande au cache les enregistrements compris dans la plage du cache et demande au serveur les enregistrements hors cache.

Les enregistrements extraits du cache ne reflètent pas les modifications concomitantes apportées par d'autres utilisateurs à la source de données.

Pour forcer une mise à jour de toutes les données mises en cache, affectez à la propriété **CacheSize** de l'objet **Recordset** la valeur 0, réaffectez-lui une valeur correspondant à la taille du cache initialement demandé puis utilisez la méthode **FillCache**.

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
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
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
     " No cache: " & Format(sngNoCache, _ 
     "##0.000") & " seconds" & vbCr & _ 
     " 50-record cache: " & Format(sngCache, _ 
     "##0.000") & " seconds" 
     .Close 
     End With 
     
     ' Delete linked table because this is a demonstration. 
     dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
     dbsCurrent.Close 
     
    End Sub
```
