---
title: Connection.CreateQueryDef, méthode (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 254fe81a-9b45-e8e7-108d-503c1c1c0fcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191860(v=office.15)
ms:contentKeyID: 48543781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053067
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: e1cbf52de80118280b57e5ca971a213afc90c48f
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63628961"
---
# <a name="connectioncreatequerydef-method-dao"></a>Connection.CreateQueryDef, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Crée un objet **[QueryDef](querydef-object-dao.md)**.

## <a name="syntax"></a>Syntaxe

*expression* .CreateQueryDef(***Name** _, _*_SQLText_**)

*expression* Variable qui représente un objet **Connection**.

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
<td><p><strong>Variant</strong> (sous-type <strong>String</strong>) qui identifie par un nom unique le nouvel objet <strong>QueryDef</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>SQLText</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (sous-type <strong>String</strong>) qui représente une instruction SQL définissant l’objet <strong>QueryDef</strong>. Si vous ne spécifiez pas cet argument, vous pouvez définir l’objet <strong>QueryDef</strong> en paramétrant sa propriété <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> avant ou après son ajout à une collection.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

QueryDef

## <a name="remarks"></a>Remarques

Dans un espace de travail Microsoft Access, si vous spécifiez autre chose qu’une chaîne de longueur nulle pour le nom lorsque vous créez un objet **QueryDef**, l’objet **QueryDef** résultant est automatiquement ajouté à la collection **[QueryDefs](querydefs-collection-dao.md)**.

Si l’objet spécifié par le nom est déjà membre de la collection **QueryDefs**, une erreur d’exécution se produit. Vous pouvez créer un fichier temporaire **QueryDef** en utilisant une chaîne nulle pour l’argument nom lorsque vous exécutez la méthode **CreateQueryDef**. Vous obtenez un résultat identique en affectant à la propriété **[Name](connection-name-property-dao.md)** d'un nouvel objet **QueryDef** une chaîne nulle (""). Les objets **QueryDef** temporaires sont utiles si vous souhaitez utiliser à plusieurs reprises des instructions SQL dynamiques sans créer de nouveaux objets permanents dans la collection **QueryDefs**. Vous ne pouvez pas ajouter d'objet **QueryDef** temporaire à une collection car une chaîne nulle ne constitue pas un nom valide pour un objet **QueryDef** permanent. Vous avez toujours la possibilité de définir les propriétés **Name** et **SQL** du nouvel objet **QueryDef** et ajouter par la suite l'objet **QueryDef** à la collection **QueryDefs**.

Pour exécuter l’instruction SQL dans un objet **QueryDef**, utilisez la méthode **[Execute](connection-execute-method-dao.md)** ou **[OpenRecordset](connection-openrecordset-method-dao.md)**.

Le recours à un objet **QueryDef** est la méthode généralement utilisée pour exécuter des requêtes SQL directes avec des bases de données ODBC.

Pour supprimer un objet **QueryDef** d’une collection **QueryDefs** dans une base de données de moteur de base de données Microsoft Access, appelez la méthode **[Delete](fields-delete-method-dao.md)** sur la collection.

