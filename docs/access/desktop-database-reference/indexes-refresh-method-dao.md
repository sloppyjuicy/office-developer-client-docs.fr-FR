---
title: Indexes.Refresh, méthode (DAO)
TOCTitle: Refresh Method
ms:assetid: ffe1bc79-5a56-2a70-c5ac-2f80b683adbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837325(v=office.15)
ms:contentKeyID: 48548973
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7e1b2a017342532f3eba1e14ce6097fea8ebffa8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291482"
---
# <a name="indexesrefresh-method-dao"></a><span data-ttu-id="cb5f7-102">Indexes.Refresh, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="cb5f7-102">Indexes.Refresh method (DAO)</span></span>


<span data-ttu-id="cb5f7-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb5f7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cb5f7-104">Met à jour les objets dans la collection spécifiée pour refléter le schéma actuel de la base de données.</span><span class="sxs-lookup"><span data-stu-id="cb5f7-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb5f7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb5f7-105">Syntax</span></span>

<span data-ttu-id="cb5f7-106">*.* Actualiser</span><span class="sxs-lookup"><span data-stu-id="cb5f7-106">*expression* .Refresh</span></span>

<span data-ttu-id="cb5f7-107">*expression* Variable qui représente un objet **Indexes.**</span><span class="sxs-lookup"><span data-stu-id="cb5f7-107">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb5f7-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="cb5f7-108">Remarks</span></span>

<span data-ttu-id="cb5f7-p101">Utilisez la méthode **Refresh** dans les environnements multi-utilisateurs dans lesquels les autres utilisateurs peuvent modifier la base de données. Vous avez peut-être besoin également de l'utiliser dans des collections concernées indirectement par les modifications apportées à la base de données. Par exemple, si vous modifiez une collection **Users**, il est peut-être nécessaire d'actualiser une collection **Groups** avant d'utiliser cette collection **Groups**.</span><span class="sxs-lookup"><span data-stu-id="cb5f7-p101">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="cb5f7-p102">Une collection est remplie d'objets la première fois qu'elle est nommée. Elle ne reflète pas automatiquement les modifications suivantes effectuées par d'autres utilisateurs. Si un autre utilisateur est susceptible de modifier une collection, utilisez la méthode Refresh dans la collection immédiatement avant d'effectuer une tâche dans l'application qui considère la présence ou l'absence d'un objet déterminé dans la collection. Cela permet de s'assurer que la collection est aussi à jour que possible. Par ailleurs, l'utilisation de la méthode Refresh peut ralentir inutilement les performances.</span><span class="sxs-lookup"><span data-stu-id="cb5f7-p102">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

