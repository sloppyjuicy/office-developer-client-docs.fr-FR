---
title: Recordset2.StillExecuting, propriété (DAO)
TOCTitle: StillExecuting Property
ms:assetid: f051c350-0451-44fe-0e47-b152bae4b481
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836546(v=office.15)
ms:contentKeyID: 48548601
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa94622374990ce48c857e9ad45c3531975bb9a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307216"
---
# <a name="recordset2stillexecuting-property-dao"></a>Recordset2.StillExecuting, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*.* StillExecuting

*expression* Variable qui représente un **objet Recordset2.**

## <a name="remarks"></a>Remarques

Utilisez la propriété **StillExecuting** pour déterminer si la dernière méthode **Execute** ou **OpenConnection** asynchrone appelée (c.-à-d. une méthode exécutée avec l'option **dbRunAsync**) est terminée. Il est impossible d'accéder à tout objet renvoyé tant que la propriété **StillExecuting** a la valeur **True**.

Dès que la propriété **StillExecuting** renvoie **False**, à la suite de l'appel de **OpenConnection** qui retourne l'objet **Connection** associé, il est possible de référencer l'objet. Tant que la propriété **StillExecuting** conserve la valeur **True**, vous ne pouvez pas faire référence à l'objet mais simplement lire la propriété **StillExecuting**.

Utilisez la méthode **[Cancel](connection-cancel-method-dao.md)** pour mettre fin à l'exécution d'une tâche en cours.

