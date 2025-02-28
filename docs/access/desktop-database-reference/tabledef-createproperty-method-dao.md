---
title: TableDef.CreateProperty, méthode (DAO)
TOCTitle: CreateProperty Method
ms:assetid: 8a92cc64-414e-f33c-1c3e-d1b62c1688c2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197102(v=office.15)
ms:contentKeyID: 48546197
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4a6e274718442bcbce0906cba9690d56b4556efc
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63633273"
---
# <a name="tabledefcreateproperty-method-dao"></a>TableDef.CreateProperty, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Crée un objet utilisateur **[Property](property-object-dao.md)** (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*.* CreateProperty(***Name** _, _*_Type_*_, _*_Value_*_, _*_DDL_**)

*expression* Variable représentant un objet **TableDef**.

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
<td><p><em>Name</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Valeur de type <strong>String</strong> qui nomme de façon unique le nouvel objet <strong>Property</strong>. Voir la propriété <strong>Name</strong> pour plus d'informations sur les noms <strong>Property</strong> valides.</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante qui définit le type de données du nouvel objet <strong>Property</strong>. Pour connaître les types de données valides, reportez-vous à la propriété <strong><a href="field-type-property-dao.md">Type</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><em>Value</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> contenant la valeur initiale de la propriété. Pour plus d’informations, reportez-vous à la méthode <strong><a href="field-value-property-dao.md">Value</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>DDL</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Valeur de type <strong>Variant</strong> (sous-type <strong>Boolean</strong>) indiquant si l'objet <strong>Property</strong> est ou non un objet DDL. La valeur par défaut est <strong>False</strong>. Si DDL a la valeur <strong>True</strong>, les utilisateurs ne peuvent pas modifier ou supprimer cet objet <strong>Property</strong> sauf s'ils détiennent une autorisation <strong>dbSecWriteDef</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

Propriété

## <a name="remarks"></a>Remarques

Vous pouvez créer un objet utilisateur **Property** uniquement dans la collection **[Properties](properties-collection-dao.md)** d'un objet qui est persistant.

Si vous omettez une ou plusieurs parties facultatives lorsque vous utilisez **CreateProperty**, vous pouvez utiliser une instruction d'affectation appropriée pour définir ou réinitialiser la propriété correspondante avant d'ajouter le nouvel objet à une collection. Une fois que vous ajoutez l'objet, vous pouvez modifier certains de ses paramètres de propriété mais pas tous. Pour plus d'informations, reportez-vous aux rubriques des propriétés **Name**, **Type** et **Value**.

Si le nom fait référence à un objet qui est déjà membre de la collection, une erreur d’utilisation se produit lorsque vous utilisez **[la méthode Append](fields-append-method-dao.md)** .

Pour supprimer un objet utilisateur **Property** de la collection, utilisez la méthode **[Delete](fields-delete-method-dao.md)** de la collection **[Properties](properties-collection-dao.md)**. Vous ne pouvez pas supprimer de propriétés intégrées.

> [!NOTE]
> Si vous omettez l'argument DDL, sa valeur par défaut est False (non DDL). Étant donné qu’aucune propriété DDL correspondante n’est exposée, vous devez supprimer et re-créer un objet **Property** que vous souhaitez remplacer de DDL par un objet non DDL.


