---
title: Méthode TableDefs.Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: f76c1a3f-1561-ce1f-a535-a5a2179ea739
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836915(v=office.15)
ms:contentKeyID: 48548765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 53a632999f1b60b078e9365c9f99e52ddec284e9
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927878"
---
# <a name="tabledefsrefresh-method-dao"></a>Méthode TableDefs.Refresh (DAO)


**S’applique à**: Access 2013, Office 2013

Met à jour les objets de la collection spécifiée en fonction du schéma actuel de la base de données.

## <a name="syntax"></a>Syntaxe

*expression* . Actualiser

*expression* Variable qui représente un objet **TableDef** .

## <a name="remarks"></a>Remarques

Pour déterminer la position utilisée par le moteur de base de données Microsoft Access pour les objets **Field** dans la collection **Fields** d'un objet **QueryDef**, **Recordset** ou **TableDef**, utilisez la propriété **OrdinalPosition** de chaque objet **Field**. La modification de la propriété **OrdinalPosition** d'un objet **Field** ne peut pas modifier l'ordre des objets **Field** dans la collection tant que vous n'utilisez pas la méthode **Refresh**.

Utilisez la méthode **Refresh** dans les environnements multi-utilisateurs dans lesquels les autres utilisateurs peuvent modifier la base de données. Vous avez peut-être besoin également de l'utiliser dans des collections concernées indirectement par les modifications apportées à la base de données. Par exemple, si vous modifiez une collection **Users**, il est peut-être nécessaire d'actualiser une collection **Groups** avant d'utiliser cette collection **Groups**.

Une collection est remplie d'objets lors de son premier référencement et ne reflète pas automatiquement les modifications que les autres utilisateurs apportent par la suite. S'il est probable qu'un autre utilisateur a modifié une collection, appliquez immédiatement la méthode Refresh à la collection avant d'effectuer une tâche dans votre application qui suppose la présence ou l'absence d'un objet déterminé dans la collection. Vous serez ainsi assuré que la collection est parfaitement à jour. D'un autre côté, l'utilisation de la méthode Refresh peut inutilement ralentir les performances.

