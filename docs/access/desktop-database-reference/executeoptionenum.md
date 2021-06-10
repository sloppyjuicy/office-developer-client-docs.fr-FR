---
title: ExecuteOptionEnum (référence de base de données de bureau Access)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: febeb3b52eb579647c995b01d6723a5c1f1b0c1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293244"
---
# <a name="executeoptionenum"></a>ExecuteOptionEnum

**S’applique à** : Access 2013, Office 2013

Spécifie la manière dont un fournisseur doit exécuter une commande.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adAsyncExecute</strong></p></td>
<td><p>0x10</p></td>
<td><p>Indique que la commande doit s’exécuter de manière asynchrone. Cette valeur ne peut être combinée avec la valeur <a href="commandtypeenum.md">CommandTypeEnum</a><strong>adCmdTableDirect</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAsyncFetch</strong></p></td>
<td><p>0x20</p></td>
<td><p>Indique que les lignes restantes après la quantité spécifiée dans la propriété <a href="cachesize-property-ado.md">CacheSize</a> doivent être extraites de manière asynchrone.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAsyncFetchNonBlocking</strong></p></td>
<td><p>0x40</p></td>
<td><p>Indique que le thème principal ne bloque jamais l'extraction. Si la ligne demandée n'a pas été extraite, la ligne en cours se déplace automatiquement vers la fin du fichier.
</p><p>Si vous ouvrez un objet <a href="recordset-object-ado.md">Recordset</a> depuis une <a href="stream-object-ado.md">chaîne</a> contenant un objet <strong>Recordset</strong> stocké avec persistance, <strong>adAsyncFetchNonBlocking</strong> sera sans effet ; l’opération sera synchrone et bloquante. <strong>adAsynchFetchNonBlocking</strong> est sans effet lorsque l’option <a href="commandtypeenum.md">adCmdTableDirect</a> est utilisée pour ouvrir l’objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteNoRecords</strong></p></td>
<td><p>0x80</p></td>
<td><p>Indique que le texte de la commande est une commande ou une procédure stockée qui ne renvoie pas de lignes (par exemple, une commande qui ne fait qu'insérer des données). Si des lignes sont extraites, elles sont ignorées et non renvoyées. <strong>adExecuteNoRecords peut</strong> uniquement être transmis en tant que paramètre facultatif à la <strong>méthode Command</strong> ou <strong>Connection</strong> <strong>Execute.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adExecuteStream</strong></p></td>
<td><p>0x400</p></td>
<td><p>Indique que le résultat de l'exécution d'une commande doit être renvoyé sous forme de chaîne. <strong>adExecuteStream</strong> peut uniquement être transmis en tant que paramètre facultatif à la <strong>méthode Command</strong> <strong>Execute.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteRecord</strong></p></td>
<td><p><br />
</p></td>
<td><p>Indique que <strong>CommandText</strong> est une commande ou une procédure stockée qui renvoie une seule ligne, sous la forme d'un objet <strong>Record</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOptionUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Indique que la commande n'est pas spécifiée.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Module : **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.ExecuteOption.ASYNCEXECUTE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ExecuteOption.ASYNCFETCH</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ExecuteOption.NORECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ExecuteOption.UNSPECIFIED</p></td>
</tr>
</tbody>
</table>

