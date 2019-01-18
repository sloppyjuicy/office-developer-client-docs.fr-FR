---
title: CursorOptionEnum (référence de base de données du bureau Access)
TOCTitle: CursorOptionEnum
ms:assetid: 3c118c08-02f2-5290-1cef-29e97c35fddc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249155(v=office.15)
ms:contentKeyID: 48544303
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7443e0cb29954fae9dfc193ffc6aa8dee9886089
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701066"
---
# <a name="cursoroptionenum"></a>CursorOptionEnum

**S’applique à**: Access 2013, Office 2013

Spécifie la fonctionnalité que la méthode [Supports](supports-method-ado.md) doit tester.

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
<td><p><strong>adAddNew</strong></p></td>
<td><p>0x1000400</p></td>
<td><p>Prend en charge la méthode <a href="addnew-method-ado.md">AddNew</a> pour l’ajout de nouveaux enregistrements.</p></td>
</tr>
<tr class="even">
<td><p><strong>adApproxPosition</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Prend en charge les propriétés <a href="absoluteposition-property-ado.md">AbsolutePosition</a> et <a href="absolutepage-property-ado.md">AbsolutePage</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adBookmark</strong></p></td>
<td><p>0 x 2000</p></td>
<td><p>Prendre en charge la propriété <a href="bookmark-property-ado.md">Bookmark</a> pour l’accès à des enregistrements spécifiques.</p></td>
</tr>
<tr class="even">
<td><p><strong>adDelete</strong></p></td>
<td><p>0x1000800</p></td>
<td><p>Prend en charge la méthode <a href="delete-method-ado-recordset.md">Delete</a> pour la suppression d’enregistrements.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFind</strong></p></td>
<td><p>0 x 80000</p></td>
<td><p>Prend en charge la méthode <a href="find-method-ado.md">Find</a> pour localiser une ligne dans un <a href="recordset-object-ado.md">Recordset</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adHoldRecords</strong></p></td>
<td><p>0 x 100</p></td>
<td><p>Recherche d'autres enregistrements ou modifie la position suivante sans valider les modifications en attente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIndex</strong></p></td>
<td><p>0 x 100000</p></td>
<td><p>Prend en charge la propriété <a href="index-property-ado.md">Index</a> pour nommer un index.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMovePrevious</strong></p></td>
<td><p>0 x 200</p></td>
<td><p>Prend en charge les méthodes <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> et <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a>, ainsi que les méthodes <a href="move-method-ado.md">Move</a> ou <a href="getrows-method-ado.md">GetRows</a> pour faire reculer la position de l’enregistrement en cours sans nécessiter de signets.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adNotify</strong></p></td>
<td><p>0 x 40000</p></td>
<td><p>Indique que le fournissseur de données sous-jacentes prend en charge les notifications (ce qui détermine la prise en charge des événements <strong>Recordset</strong>).</p></td>
</tr>
<tr class="even">
<td><p><strong>adResync</strong></p></td>
<td><p>0 x 20000</p></td>
<td><p>Prend en charge la méthode <a href="resync-method-ado.md">Resync</a> pour mettre à jour le curseur avec les données visibles dans la base de données sous-jacente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSeek</strong></p></td>
<td><p>0x200000</p></td>
<td><p>Prend en charge la méthode <a href="seek-method-ado.md">Seek</a> pour localiser une ligne dans <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adUpdate</strong></p></td>
<td><p>0x1008000</p></td>
<td><p>Prend en charge la méthode <a href="update-method-ado.md">Update</a> pour modifier des données existantes.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUpdateBatch</strong></p></td>
<td><p>0 x 10000</p></td>
<td><p>Prend en charge la mise à jour par lots (méthodes <a href="updatebatch-method-ado.md">UpdateBatch</a> et <a href="cancelbatch-method-ado.md">CancelBatch</a>) pour transmettre des groupes de modifications au fournisseur.</p></td>
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
<td><p>AdoEnums.CursorOption.ADDNEW</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.APPROXPOSITION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.BOOKMARK</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.DELETE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.FIND</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.HOLDRECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.INDEX</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.MOVEPREVIOUS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.NOTIFY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.RESYNC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.SEEK</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.UPDATE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.UPDATEBATCH</p></td>
</tr>
</tbody>
</table>

