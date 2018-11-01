---
title: Status, propriété (objet Field ADO)
TOCTitle: Status Property (ADO Field)
ms:assetid: 7a7b45e8-2934-2e8e-77fa-a4f38272548d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249507(v=office.15)
ms:contentKeyID: 48545795
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6be229e2dfd0cc8dd25fd217bdd6cb50f65cb32
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872367"
---
# <a name="status-property-ado-field"></a>Status, propriété (objet Field ADO)


**S’applique à**: Access 2013, Office 2013

Indique l'état d'un objet [Field](field-object-ado.md).

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur [FieldStatusEnum](fieldstatusenum.md). La valeur par défaut est **adFieldOK**.

## <a name="remarks"></a>Remarques

Cette propriété renvoie toujours **adFieldOK** pour les champs d'un objet [Recordset](recordset-object-ado.md).

Les additions et les suppressions effectuées sur les collections [Fields](fields-collection-ado.md) de l'objet [Record](record-object-ado.md) sont mises en cache jusqu'à ce que la méthode [Update](update-method-ado.md) soit appelée. La propriété **Status** vous permet de déterminer les champs ayant été correctement ajoutés ou supprimés.

Pour améliorer les performances, les modifications apportées au schéma sont mis en cache jusqu'à ce que la méthode **Update** est appelée, puis les modifications sont apportées à une mise à jour par lot optimiste. Si la méthode de **mise à jour** n’est pas appelée, le serveur n’est pas mis à jour. Si des mises à jour échouent ensuite une erreur est renvoyée et la propriété **Status** indique les valeurs associées de l’opération et le code d’état d’erreur. Par exemple, **adFieldPendingInsert** **ou** **adFieldPermissionDenied**. La propriété **Status** pour chaque **champ** peut être utilisée pour déterminer pourquoi le **champ** a été pas ajouté, modifié ou supprimé. **État** est exposé uniquement de manière significative sur l' **enregistrement**. Collection **Fields** et pas le **jeu d’enregistrements**. Collection de **champs** .

Deux problèmes peuvent survenir lors de l'ajout, de la modification ou de la suppression d'un objet **Field**. Si l'utilisateur supprime un objet **Field**, il est marqué pour suppression dans la collection **Fields**. Si l'appel suivant de la méthode **Update** renvoie une erreur parce que l'utilisateur a tenté de supprimer un objet **Field** sur lequel il n'avait pas les autorisations nécessaires, l'objet **Field** aura pour état **adFieldPermissionDenied** **OR** **adFieldPendingDelete**. Le fait d'appeler la méthode [CancelUpdate](cancelupdate-method-ado.md) restaure les valeurs d'origine et donne à la propriété **Status** la valeur **adFieldOK**. De même, la méthode **Update** peut renvoyer une erreur lorsqu'un nouvel objet **Field** a été ajouté et que la valeur qui lui a été attribuée est incorrecte. Dans ce cas, le nouvel objet **Field** est stocké dans la collection **Fields**; prend l'état **adFieldPendingInsert**, voire **adFieldCantCreate**. Vous pouvez donner au nouvel objet **Field** une valeur correcte et appeler à nouveau la méthode **Update**. Remarque : si vous appelez **Resync**, une requête est renvoyée au fournisseur.

