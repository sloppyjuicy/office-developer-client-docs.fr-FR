---
title: TableDefs.Refresh, méthode (DAO)
TOCTitle: Refresh Method
ms:assetid: f76c1a3f-1561-ce1f-a535-a5a2179ea739
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836915(v=office.15)
ms:contentKeyID: 48548765
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6050e2d0b97421bda7a2914f068db4019459ee7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306313"
---
# <a name="tabledefsrefresh-method-dao"></a>TableDefs.Refresh, méthode (DAO)


**S’applique à** : Access 2013, Office 2013

Met à jour les objets dans la collection spécifiée pour refléter le schéma actuel de la base de données.

## <a name="syntax"></a>Syntaxe

*.* Actualiser

*expression* Variable qui représente un **objet TableDefs.**

## <a name="remarks"></a>Remarques

Pour déterminer la position utilisée par le moteur de base de données Microsoft Access pour les objets **Field** dans la collection **Fields** d'un objet **QueryDef**, **Recordset** ou **TableDef**, utilisez la propriété **OrdinalPosition** de chaque objet **Field**. La modification de la propriété **OrdinalPosition** d'un objet **Field** ne peut pas modifier l'ordre des objets **Field** dans la collection tant que vous n'utilisez pas la méthode **Refresh**.

Utilisez la méthode **Refresh** dans les environnements multi-utilisateurs dans lesquels les autres utilisateurs peuvent modifier la base de données. Vous avez peut-être besoin également de l'utiliser dans des collections concernées indirectement par les modifications apportées à la base de données. Par exemple, si vous modifiez une collection **Users**, il est peut-être nécessaire d'actualiser une collection **Groups** avant d'utiliser cette collection **Groups**.

Une collection est remplie d'objets la première fois qu'elle est nommée. Elle ne reflète pas automatiquement les modifications suivantes effectuées par d'autres utilisateurs. Si un autre utilisateur est susceptible de modifier une collection, utilisez la méthode Refresh dans la collection immédiatement avant d'effectuer une tâche dans l'application qui considère la présence ou l'absence d'un objet déterminé dans la collection. Cela permet de s'assurer que la collection est aussi à jour que possible. Par ailleurs, l'utilisation de la méthode Refresh peut ralentir inutilement les performances.

