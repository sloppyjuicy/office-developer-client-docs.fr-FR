---
title: Status, propriété (champ ADO)
TOCTitle: Status property (ADO Field)
ms:assetid: 7a7b45e8-2934-2e8e-77fa-a4f38272548d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249507(v=office.15)
ms:contentKeyID: 48545795
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 877a7d17b0f5ad9d5b0c16e6ff2497083c5276a9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568382"
---
# <a name="status-property-ado-field"></a>Status, propriété (champ ADO)


**S’applique à** : Access 2013, Office 2013

Indique l'état d'un objet [Field](field-object-ado.md).

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur [FieldStatusEnum](fieldstatusenum.md). La valeur par défaut est **adFieldOK**.

## <a name="remarks"></a>Remarques

Cette propriété renvoie toujours **adFieldOK** pour les champs d’un objet [Recordset](recordset-object-ado.md).

Les additions et les suppressions effectuées sur les collections [Fields](fields-collection-ado.md) de l'objet [Record](record-object-ado.md) sont mises en cache jusqu'à ce que la méthode [Update](update-method-ado.md) soit appelée. La propriété **Status** vous permet de déterminer les champs ayant été correctement ajoutés ou supprimés.

Pour améliorer les performances, les modifications de schéma sont mises en cache jusqu’à ce que **la** mise à jour soit appelée, puis les modifications sont apportées dans une mise à jour par lot optimiste. Si la **méthode Update** n’est pas appelée, le serveur n’est pas mis à jour. Si des mises à jour échouent, une erreur est renvoyée et la propriété **Status** indique les valeurs combinées du code d’état d’opération et d’erreur. Par exemple, **adFieldPendingInsert** **OR** **adFieldPermissionDenied**. La **propriété Status** de chaque **champ** peut  être utilisée pour déterminer pourquoi le champ n’a pas été ajouté, modifié ou supprimé. **L’état** est uniquement exposé de manière significative sur **l’enregistrement**. **Fields,** collection et non **l’recordset**. **Fields,** collection.

Deux problèmes peuvent survenir lors de l'ajout, de la modification ou de la suppression d'un objet **Field**. Si l'utilisateur supprime un objet **Field**, il est marqué pour suppression dans la collection **Fields**. Si l'appel suivant de la méthode **Update** renvoie une erreur parce que l'utilisateur a tenté de supprimer un objet **Field** sur lequel il n'avait pas les autorisations nécessaires, l'objet **Field** aura pour état **adFieldPermissionDenied** **OR** **adFieldPendingDelete**. Le fait d'appeler la méthode [CancelUpdate](cancelupdate-method-ado.md) restaure les valeurs d'origine et donne à la propriété **Status** la valeur **adFieldOK**. De même, la méthode **Update** peut renvoyer une erreur lorsqu'un nouvel objet **Field** a été ajouté et que la valeur qui lui a été attribuée est incorrecte. Dans ce cas, le nouvel objet **Field** est stocké dans la collection **Fields**; prend l'état **adFieldPendingInsert**, voire **adFieldCantCreate**. Vous pouvez donner au nouvel objet **Field** une valeur correcte et appeler à nouveau la méthode **Update**. Remarque : si vous appelez **Resync**, une requête est renvoyée au fournisseur.

