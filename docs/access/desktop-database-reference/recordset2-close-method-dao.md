---
title: Recordset2. Close, méthode (DAO)
TOCTitle: Close Method
ms:assetid: ef816969-9857-37cf-9562-d5c80d2815ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836412(v=office.15)
ms:contentKeyID: 48548584
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 178dec604a185da94493e6d586249bd2a633899c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307384"
---
# <a name="recordset2close-method-dao"></a>Recordset2. Close, méthode (DAO)


**S’applique à** : Access 2013, Office 2013

Ferme un objet **Recordset** ouvert.

## <a name="syntax"></a>Syntaxe

*expression* . Proches

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Si l'objet **Recordset** est déjà fermé lorsque vous utilisez **Close**, une erreur d'exécution se produit.

If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.

Une autre solution consiste **** à définir la valeur d'une variable d'objet sur **Nothing** (Set dbsTemp = Nothing).

