---
title: InheritTypeEnum (référence de base de données du bureau Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: df631319abc1eba06d7ac804b6d8dbdaf5fc9b18
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888049"
---
# <a name="inherittypeenum"></a>InheritTypeEnum

**S’applique à**: Access 2013, Office 2013

Indique comment les objets hériteront des autorisations définies à l'aide de la méthode [SetPermissions](setpermissions-method-adox.md).

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adInheritBoth</strong></p></td>
<td><p>3</p></td>
<td><p>Les objets et autres conteneurs de l'objet principal héritent de l'entrée.</p></td>
</tr>
<tr class="even">
<td><p><strong>adInheritContainers ne</strong></p></td>
<td><p>2</p></td>
<td><p>D'autres conteneurs contenus dans l'objet principal héritent de l'entrée.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adInheritNone</strong></p></td>
<td><p>0</p></td>
<td><p>Valeur par défaut. Aucun héritage ne se produit.</p></td>
</tr>
<tr class="even">
<td><p><strong>adInheritNoPropagate</strong></p></td>
<td><p>4</p></td>
<td><p>Les indicateurs <strong>adInheritObjects</strong> et <strong>adInheritContainers</strong> ne sont pas transmis à une entrée héritée.</p></td>
</tr>
<tr class="odd">
<td><p><strong>indicateurs adInheritObjects</strong></p></td>
<td><p>1</p></td>
<td><p>Les objets du conteneur qui ne sont pas du type conteneur héritent des autorisations.</p></td>
</tr>
</tbody>
</table>

