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
# <a name="tabledefsrefresh-method-dao"></a><span data-ttu-id="9c40d-102">TableDefs.Refresh, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="9c40d-102">TableDefs.Refresh method (DAO)</span></span>


<span data-ttu-id="9c40d-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9c40d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9c40d-104">Met à jour les objets dans la collection spécifiée pour refléter le schéma actuel de la base de données.</span><span class="sxs-lookup"><span data-stu-id="9c40d-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c40d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c40d-105">Syntax</span></span>

<span data-ttu-id="9c40d-106">*.* Actualiser</span><span class="sxs-lookup"><span data-stu-id="9c40d-106">*expression* .Refresh</span></span>

<span data-ttu-id="9c40d-107">*expression* Variable qui représente un **objet TableDefs.**</span><span class="sxs-lookup"><span data-stu-id="9c40d-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c40d-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="9c40d-108">Remarks</span></span>

<span data-ttu-id="9c40d-p101">Pour déterminer la position utilisée par le moteur de base de données Microsoft Access pour les objets **Field** dans la collection **Fields** d'un objet **QueryDef**, **Recordset** ou **TableDef**, utilisez la propriété **OrdinalPosition** de chaque objet **Field**. La modification de la propriété **OrdinalPosition** d'un objet **Field** ne peut pas modifier l'ordre des objets **Field** dans la collection tant que vous n'utilisez pas la méthode **Refresh**.</span><span class="sxs-lookup"><span data-stu-id="9c40d-p101">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object. Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="9c40d-p102">Utilisez la méthode **Refresh** dans les environnements multi-utilisateurs dans lesquels les autres utilisateurs peuvent modifier la base de données. Vous avez peut-être besoin également de l'utiliser dans des collections concernées indirectement par les modifications apportées à la base de données. Par exemple, si vous modifiez une collection **Users**, il est peut-être nécessaire d'actualiser une collection **Groups** avant d'utiliser cette collection **Groups**.</span><span class="sxs-lookup"><span data-stu-id="9c40d-p102">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="9c40d-p103">Une collection est remplie d'objets la première fois qu'elle est nommée. Elle ne reflète pas automatiquement les modifications suivantes effectuées par d'autres utilisateurs. Si un autre utilisateur est susceptible de modifier une collection, utilisez la méthode Refresh dans la collection immédiatement avant d'effectuer une tâche dans l'application qui considère la présence ou l'absence d'un objet déterminé dans la collection. Cela permet de s'assurer que la collection est aussi à jour que possible. Par ailleurs, l'utilisation de la méthode Refresh peut ralentir inutilement les performances.</span><span class="sxs-lookup"><span data-stu-id="9c40d-p103">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

