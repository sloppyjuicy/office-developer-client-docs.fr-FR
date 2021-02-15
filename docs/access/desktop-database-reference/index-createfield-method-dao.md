---
title: Index.CreateField, méthode (DAO)
TOCTitle: CreateField Method
ms:assetid: fc82b785-8768-b144-a2a4-c1f1798865a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837208(v=office.15)
ms:contentKeyID: 48548892
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aedda14273446ff6823776e535eb7995aa127fa5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291830"
---
# <a name="indexcreatefield-method-dao"></a>Index.CreateField, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Crée un objet **[Field](field-object-dao.md)** (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*.* CreateField(***Name***, ***Type***, ***Size***)

*expression* Variable qui représente un objet **Index.**

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
<td><p>Chaîne qui identifie de manière unique le nouvel objet <strong>Field</strong>. Reportez-vous à la propriété <strong><a href="connection-name-property-dao.md">Name</a></strong> pour plus d’informations sur les noms valides pour l’objet <strong>Field</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Argument non pris en charge pour cet objet.</p></td>
</tr>
<tr class="odd">
<td><p><em>Size</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Argument non pris en charge pour cet objet.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

Field

## <a name="remarks"></a>Remarques

Vous pouvez utiliser la méthode **CreateField** pour créer un champ, spécifier le nom, le type de données et la taille du champ. Si vous omettez une ou plusieurs des parties facultatives lorsque vous utilisez la méthode **CreateField**, vous pouvez utiliser une instruction d’affectation appropriée pour définir ou réinitialiser la propriété correspondante avant d’ajouter le nouvel objet à la collection. Une fois que vous avez ajouté le nouvel objet, vous pouvez modifier une partie de ses paramètres de propriété, mais pas tous. Pour plus d’informations, reportez-vous aux rubriques concernant cette propriété.

Les arguments de type et de taille s’appliquent uniquement aux objets **Field** dans un **objet TableDef.** Les arguments suivants sont ignorés quand un objet **Field** est associé un objet **Index** ou **Relation**.

Si le nom fait référence à un objet qui est déjà membre de la collection, une erreur d’utilisation se produit lorsque vous utilisez la **[méthode Append.](fields-append-method-dao.md)**

Pour supprimer un objet **Field** d’une collection **Fields**, utilisez la méthode **[Delete](fields-delete-method-dao.md)** dans la collection. Vous ne pouvez pas supprimer un objet **Field** dans la collection **Fields** d’un objet **TableDef** une fois que vous avez créé un index qui renvoie à ce champ.

