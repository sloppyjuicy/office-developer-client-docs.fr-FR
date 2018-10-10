---
title: ExecuteOptionEnum (référence de base de données du bureau Access)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aeb1083c693e0848e30a0b9217ae709994daddb5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470625"
---
# <a name="executeoptionenum"></a>ExecuteOptionEnum


**S’applique à**: Access 2013 | Office 2013

Spécifie la manière dont un fournisseur doit exécuter une commande.

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
<td><p>0 x 10</p></td>
<td><p>Indique que la commande doit s’exécuter de manière asynchrone.
 Cette valeur ne peut être combinée avec la valeur <a href="commandtypeenum.md">CommandTypeEnum</a><strong>adCmdTableDirect</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAsyncFetch</strong></p></td>
<td><p>0 x 20</p></td>
<td><p>Indique que les lignes restantes après la quantité spécifiée dans la propriété <a href="cachesize-property-ado.md">CacheSize</a> doivent être extraites de manière asynchrone.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAsyncFetchNonBlocking</strong></p></td>
<td><p>0 x 40</p></td>
<td><p>Indique que le thread principal bloque jamais lors de la récupération. Si la ligne demandée n’a pas été extraite, la ligne active se déplace automatiquement à la fin du fichier. Si vous ouvrez un objet <a href="recordset-object-ado.md">Recordset</a> depuis une <a href="stream-object-ado.md">chaîne</a> contenant un objet <strong>Recordset</strong> stocké avec persistance, <strong>adAsyncFetchNonBlocking</strong> sera sans effet ; l’opération sera synchrone et bloquante. <strong>adAsynchFetchNonBlocking</strong> est sans effet lorsque l’option <a href="commandtypeenum.md">adCmdTableDirect</a> est utilisée pour ouvrir l’objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteNoRecords</strong></p></td>
<td><p>0 x 80</p></td>
<td><p>Indique que le texte de commande est une commande ou une procédure stockée qui ne retourne pas de lignes (par exemple, une commande qui insère des données uniquement). Si des lignes sont extraites, elles sont ignorées et pas retournés. <strong>adExecuteNoRecords</strong> ne peut être passé comme paramètre facultatif à la <strong>commande</strong> ou la méthode <strong>Execute</strong> de <strong>connexion</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>adExecuteStream</strong></p></td>
<td><p>0 x 400</p></td>
<td><p>Indique que le résultat de l'exécution d'une commande doit être renvoyé sous forme de chaîne.
 <strong>adExecuteStream</strong> ne peut être passé comme paramètre optionnel que pour la méthode <strong>Execute</strong> de <strong>commande</strong> .</p></td>
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


**Équivalent ADO/WFC**

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

