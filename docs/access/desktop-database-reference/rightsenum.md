---
title: RightsEnum (référence de base de données du bureau Access)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7bf2f88632265cda7537215f2ea3c68507f16f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706603"
---
# <a name="rightsenum"></a>RightsEnum

**S’applique à**: Access 2013, Office 2013

Spécifie les droits ou autorisations d'un groupe ou d'un utilisateur sur un objet.

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
<td><p><strong>adRightCreate</strong></p></td>
<td><p>16384<br />
(&amp;H4000)</p></td>
<td><p>L'utilisateur ou le groupe a l'autorisation de créer de nouveaux objets de ce type.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightDelete</strong></p></td>
<td><p>65536<br />
(&amp;H10000)</p></td>
<td><p>L'utilisateur ou le groupe a l'autorisation de supprimer des données d'un objet. Pour des objets de type <strong>Table</strong> par exemple, l'utilisateur a l'autorisation de supprimer des valeurs de données dans des enregistrements.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightDrop</strong></p></td>
<td><p>256<br />
(&amp;H100)</p></td>
<td><p>L'utilisateur ou le groupe a l'autorisation de supprimer des objets du catalogue. Par exemple, il peut supprimer un objet <strong>Table</strong> à l'aide de la commande DROP TABLE SQL.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightExclusive</strong></p></td>
<td><p>512<br />
(&amp;H200)</p></td>
<td><p>L'utilisateur ou le groupe a l'autorisation d'accéder à l'objet en mode exclusif.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightExecute</strong></p></td>
<td><p>536870912<br />
(&amp;H20000000)</p></td>
<td><p>L'utilisateur ou le groupe a l'autorisation d'exécuter l'objet.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightFull</strong></p></td>
<td><p>268435456<br />
(&amp;H10000000)</p></td>
<td><p>L'utilisateur ou le groupe dispose d'autorisations complètes sur l'objet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightInsert</strong></p></td>
<td><p>32768<br />
(&amp;H8000)</p></td>
<td><p>L'utilisateur ou le groupe a l'autorisation d'insérer l'objet. Pour des objets de type <strong>Table</strong>, l'utilisateur a l'autorisation d'insérer des données dans la table.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightMaximumAllowed</strong></p></td>
<td><p>33554432 (&amp;H2000000)</p></td>
<td><p>L'utilisateur ou le groupe dispose du nombre maximal d'autorisations admises par le fournisseur. Les autorisations spécifiques dépendent du fournisseur.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightNone</strong></p></td>
<td><p>0</p></td>
<td><p>L'utilisateur ou le groupe n'a aucune autorisation pour l'objet.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightRead</strong></p></td>
<td><p>-2147483648<br />
(&amp;H80000000)</p></td>
<td><p>L’utilisateur ou le groupe a l’autorisation de lire l’objet. Pour des objets de type <a href="table-object-adox.md">Table</a>, l’utilisateur est autorisé à lire les données de la table.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightReadDesign</strong></p></td>
<td><p>1024<br />
(&amp;H400)</p></td>
<td><p>L'utilisateur ou le groupe a l'autorisation de lire la conception de l'objet.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightReadPermissions</strong></p></td>
<td><p>131072<br />
(&amp;H20000)</p></td>
<td><p>L'utilisateur ou le groupe peut afficher mais non modifier les autorisations spécifiques liées à un objet dans le catalogue.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightReference</strong></p></td>
<td><p>8192<br />
(&amp;H2000)</p></td>
<td><p>L'utilisateur ou le groupe a l'autorisation de faire référence à l'objet.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightUpdate</strong></p></td>
<td><p>1073741824<br />
(&amp;H40000000)</p></td>
<td><p>L'utilisateur ou le groupe a l'autorisation de mettre à jour l'objet. Pour des objets de type <strong>Table</strong>, l'utilisateur est autorisé à mettre à jour les données de la table.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightWithGrant</strong></p></td>
<td><p>4096<br />
(&amp;H1000)</p></td>
<td><p>L'utilisateur ou le groupe est autorisé à octroyer des autorisations sur l'objet.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightWriteDesign</strong></p></td>
<td><p>2048<br />
(&amp;H800)</p></td>
<td><p>L'utilisateur ou le groupe a l'autorisation de modifier la conception de l'objet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRightWriteOwner</strong></p></td>
<td><p>524288<br />
(&amp;H80000)</p></td>
<td><p>L'utilisateur ou le groupe a l'autorisation de modifier le propriétaire de l'objet.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRightWritePermissions</strong></p></td>
<td><p>262144<br />
(&amp;H40000)</p></td>
<td><p>L'utilisateur ou le groupe peut modifier les autorisations spécifiques liées à un objet dans le catalogue.</p></td>
</tr>
</tbody>
</table>

