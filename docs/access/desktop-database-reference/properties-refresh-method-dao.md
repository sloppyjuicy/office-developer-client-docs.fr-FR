---
title: Properties.Refresh, méthode (DAO)
TOCTitle: Refresh Method
ms:assetid: 71ba18fb-55a5-6a5f-3631-1c81c20f3369
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195805(v=office.15)
ms:contentKeyID: 48545593
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9d6b248bc4b8d9c1a9e01db0231bf58b16c36dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301196"
---
# <a name="propertiesrefresh-method-dao"></a><span data-ttu-id="7528a-102">Properties.Refresh, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="7528a-102">Properties.Refresh method (DAO)</span></span>


<span data-ttu-id="7528a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7528a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7528a-104">Met à jour les objets dans la collection spécifiée pour refléter le schéma actuel de la base de données.</span><span class="sxs-lookup"><span data-stu-id="7528a-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="7528a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7528a-105">Syntax</span></span>

<span data-ttu-id="7528a-106">*.* Actualiser</span><span class="sxs-lookup"><span data-stu-id="7528a-106">*expression* .Refresh</span></span>

<span data-ttu-id="7528a-107">*expression* Variable qui représente un objet **Properties.**</span><span class="sxs-lookup"><span data-stu-id="7528a-107">*expression* A variable that represents a **Properties** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7528a-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="7528a-108">Remarks</span></span>

<span data-ttu-id="7528a-p101">Utilisez la méthode **Refresh** dans les environnements multi-utilisateurs dans lesquels les autres utilisateurs peuvent modifier la base de données. Vous avez peut-être besoin également de l'utiliser dans des collections concernées indirectement par les modifications apportées à la base de données. Par exemple, si vous modifiez une collection **Users**, il est peut-être nécessaire d'actualiser une collection **Groups** avant d'utiliser cette collection **Groups**.</span><span class="sxs-lookup"><span data-stu-id="7528a-p101">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="7528a-p102">Une collection est remplie d'objets la première fois qu'elle est nommée. Elle ne reflète pas automatiquement les modifications suivantes effectuées par d'autres utilisateurs. Si un autre utilisateur est susceptible de modifier une collection, utilisez la méthode Refresh dans la collection immédiatement avant d'effectuer une tâche dans l'application qui considère la présence ou l'absence d'un objet déterminé dans la collection. Cela permet de s'assurer que la collection est aussi à jour que possible. Par ailleurs, l'utilisation de la méthode Refresh peut ralentir inutilement les performances.</span><span class="sxs-lookup"><span data-stu-id="7528a-p102">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

