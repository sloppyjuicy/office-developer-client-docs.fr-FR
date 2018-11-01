---
title: Workspace.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 38f1a7a525a2cf57a98ee3fa015ce29b368aab9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884127"
---
# <a name="workspaceclose-method-dao"></a>Workspace.Close Method (DAO)


**S’applique à**: Access 2013, Office 2013

Ferme un objet **Workspace** ouvert.

## <a name="syntax"></a>Syntaxe

*expression* . Fermer

*expression* Variable qui représente un objet **Workspace** .

## <a name="remarks"></a>Remarques

Si l'objet **Workspace** est déjà fermé lorsque vous utilisez la méthode **Close**, une erreur d'exécution se produit.

Une alternative à la méthode **Close** est la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).

