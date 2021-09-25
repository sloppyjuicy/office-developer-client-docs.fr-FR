---
title: Workspace.Close, méthode (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ee787917a95e3716e629f87512caca1f408a6213
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617347"
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

