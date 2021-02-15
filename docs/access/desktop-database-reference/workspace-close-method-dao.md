---
title: Workspace.Close, méthode (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0049fb335c869a050a2c20d5740c487413c76786
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305956"
---
# <a name="workspaceclose-method-dao"></a>Workspace.Close, méthode (DAO)


**S’applique à** : Access 2013, Office 2013

Ferme un objet **Workspace** ouvert.

## <a name="syntax"></a>Syntaxe

*expression* .Close

*expression* Variable qui représente un objet **Workspace**.

## <a name="remarks"></a>Remarques

Si l'objet **Workspace** est déjà fermé lorsque vous utilisez la méthode **Close**, une erreur d'exécution se produit.

Une alternative à l’utilisation de la méthode **Close** consiste à définir la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).

