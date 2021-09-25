---
title: Recordset.StillExecuting, propriété (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 0e53c98f-17ac-3569-d780-540a6932013e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845245(v=office.15)
ms:contentKeyID: 48543245
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: bc5f1c8b708e442aa1b547844cd30c31df9fb6e7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585360"
---
# <a name="recordsetstillexecuting-property-dao"></a>Recordset.StillExecuting, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*.* StillExecuting

*expression* Variable qui représente un objet **Recordset**.

## <a name="remarks"></a>Remarques

Utilisez la propriété **StillExecuting** pour déterminer si la dernière méthode **Execute** ou **OpenConnection** asynchrone appelée (c.-à-d. une méthode exécutée avec l'option **dbRunAsync**) est terminée. Il est impossible d'accéder à tout objet renvoyé tant que la propriété **StillExecuting** a la valeur **True**.

Dès que la propriété **StillExecuting** renvoie **False**, à la suite de l'appel de **OpenConnection** qui retourne l'objet **Connection** associé, il est possible de référencer l'objet. Tant que la propriété **StillExecuting** conserve la valeur **True**, vous ne pouvez pas faire référence à l'objet mais simplement lire la propriété **StillExecuting**.

Utilisez la méthode **[Cancel](connection-cancel-method-dao.md)** pour mettre fin à l'exécution d'une tâche en cours.

