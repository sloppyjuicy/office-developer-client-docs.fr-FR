---
title: Mode immédiat (référence de base de données de bureau Access)
TOCTitle: Immediate mode
ms:assetid: 61bd3645-6e84-2e3a-7814-37d8c1247df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249362(v=office.15)
ms:contentKeyID: 48545220
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3abc2e8365c60987fedc0d306b274df74c7ee551
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291879"
---
# <a name="immediate-mode"></a>Mode immédiat


**S’applique à** : Access 2013, Office 2013

Le mode Immédiat est activé lorsque la propriété **LockType** est définie sur **adLockOptimistic** ou **adLockPessimistic**. Dans ce mode, les modifications apportées à un enregistrement sont répercutées dans la source de données dès que vous déclarez que le travail sur une ligne est terminé en invoquant la méthode **Update**.

## <a name="calling-update"></a>Invocation de la méthode Update

If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes. You must call the **CancelUpdate** method before navigation if you want to cancel any changes made to the current record or discard a newly added record.

L'enregistrement actif reste actif après avoir invoqué la méthode **Update**.

## <a name="cancelupdate"></a>CancelUpdate

Utilisez la méthode **CancelUpdate** pour annuler toute modification apportée à la ligne active ou ignorer une ligne ajoutée. Vous ne pouvez plus annuler les modifications de la ligne active ou d'une nouvelle ligne après avoir invoqué la méthode **Update**, sauf si ces modifications font partie d'une transaction que vous pouvez annuler avec la méthode **RollbackTrans** ou d'une mise à jour en lots. Dans ce dernier cas, vous pouvez annuler la **mise à jour** avec la méthode **CancelUpdate** ou **CancelBatch**.

Si vous ajoutez une ligne au moment de l'invocation de la méthode **CancelUpdate**, la ligne active devient la ligne qui était active avant l'invocation de **AddNew**.

Si vous n'avez pas modifié la ligne active ou ajouté de ligne, l'invocation de la méthode **CancelUpdate** génère une erreur.

