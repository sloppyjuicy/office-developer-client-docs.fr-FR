---
title: Mode immédiat (référence de base de données du bureau Access)
TOCTitle: Immediate mode
ms:assetid: 61bd3645-6e84-2e3a-7814-37d8c1247df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249362(v=office.15)
ms:contentKeyID: 48545220
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b6401e7954325eded85b70b9edb5d164e857d113
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947860"
---
# <a name="immediate-mode"></a>Mode immédiat


**S’applique à**: Access 2013, Office 2013

Le mode Immédiat est activé lorsque la propriété **LockType** est définie sur **adLockOptimistic** ou **adLockPessimistic**. Dans ce mode, les modifications apportées à un enregistrement sont répercutées dans la source de données dès que vous déclarez que le travail sur une ligne est terminé en invoquant la méthode **Update**.

## <a name="calling-update"></a>Invocation de la méthode Update

Si vous quittez l'enregistrement ajouté ou modifié avant d'appeler la méthode **Update**, ADO appelle automatiquement la méthode **Update** pour enregistrer les modifications. Vous devez appeler la méthode **CancelUpdate** avant la navigation si vous souhaitez annuler les modifications apportées à l’enregistrement actif ou ignorer un enregistrement nouvellement ajouté.

L'enregistrement actif reste actif après avoir invoqué la méthode **Update**.

## <a name="cancelupdate"></a>CancelUpdate

Utilisez la méthode **CancelUpdate** pour annuler toute modification apportée à la ligne active ou ignorer une ligne ajoutée. Vous ne pouvez plus annuler les modifications de la ligne active ou d'une nouvelle ligne après avoir invoqué la méthode **Update**, sauf si ces modifications font partie d'une transaction que vous pouvez annuler avec la méthode **RollbackTrans** ou d'une mise à jour en lots. Dans ce dernier cas, vous pouvez annuler la **mise à jour** avec la méthode **CancelUpdate** ou **CancelBatch**.

Si vous ajoutez une ligne au moment de l'invocation de la méthode **CancelUpdate**, la ligne active devient la ligne qui était active avant l'invocation de **AddNew**.

Si vous n'avez pas modifié la ligne active ou ajouté de ligne, l'invocation de la méthode **CancelUpdate** génère une erreur.

