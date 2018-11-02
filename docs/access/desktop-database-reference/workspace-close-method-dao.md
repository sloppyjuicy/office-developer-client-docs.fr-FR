---
title: Méthode Workspace.Close (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 63b935fa178eb4c55ce11724ec3fd5f62d056779
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919849"
---
# <a name="workspaceclose-method-dao"></a>Méthode Workspace.Close (DAO)


**S’applique à**: Access 2013, Office 2013

Ferme un objet **Workspace** ouvert.

## <a name="syntax"></a>Syntaxe

*expression* . Fermer

*expression* Variable qui représente un objet **Workspace** .

## <a name="remarks"></a>Remarques

Si l'objet **Workspace** est déjà fermé lorsque vous utilisez la méthode **Close**, une erreur d'exécution se produit.

Une alternative à la méthode **Close** est la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).

