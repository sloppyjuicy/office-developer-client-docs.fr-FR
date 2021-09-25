---
title: Properties.Append, méthode (DAO)
TOCTitle: Append Method
ms:assetid: 47f1e24f-975c-3fdc-5c3c-8c91f2920c81
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193232(v=office.15)
ms:contentKeyID: 48544609
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d90f62f96fb4526e878ead051260b71914a74aa9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602086"
---
# <a name="propertiesappend-method-dao"></a>Properties.Append, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Ajoute un nouvel objet **Property** à la collection **Properties**.

## <a name="syntax"></a>Syntaxe

*expression* .Append(***Object***)

*expression* Variable qui représente un objet **Properties.**

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
<td><p><em>Object</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Object</strong></p></td>
<td><p>Variable d'objet représentant le champ qui est ajouté à la collection.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L'objet ajouté devient un objet persistant, stocké sur le disque, tant que vous ne le supprimez pas à l'aide de la méthode **Delete**.

L'ajout d'un nouvel objet a lieu immédiatement, mais vous devez utiliser la méthode **Refresh** dans toutes les autres collections qui peuvent être affectées par les modifications apportées à la structure de la base de données.

Si l'objet que vous ajoutez n'est pas complet (par exemple, si vous n'avez pas ajouté d'objets **Field** à une collection **Fields** d'un objet **Index** avant qu'il soit ajouté à une collection **Indexes**) ou si les propriétés définies dans un ou plusieurs objets subordonnés sont incorrectes, l'utilisation de la méthode **Append** entraîne une erreur. Par exemple, si vous n'avez pas spécifié un type de champ et que vous tentez d'ajouter l'objet **Field** à la collection **Fields** dans un objet **TableDef** à l'aide de la méthode **Append**, une erreur d'exécution est générée.

