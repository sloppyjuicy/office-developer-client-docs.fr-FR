---
title: TableDefs.Refresh Method (DAO)
TOCTitle: Refresh Method
ms:assetid: f76c1a3f-1561-ce1f-a535-a5a2179ea739
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836915(v=office.15)
ms:contentKeyID: 48548765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9820bf278277d3b7d021f56524fea869eebcdf41
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886066"
---
# <a name="tabledefsrefresh-method-dao"></a><span data-ttu-id="38977-102">TableDefs.Refresh Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="38977-102">TableDefs.Refresh Method (DAO)</span></span>


<span data-ttu-id="38977-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="38977-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="38977-104">Met à jour les objets de la collection spécifiée en fonction du schéma actuel de la base de données.</span><span class="sxs-lookup"><span data-stu-id="38977-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="38977-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38977-105">Syntax</span></span>

<span data-ttu-id="38977-106">*expression* . Actualiser</span><span class="sxs-lookup"><span data-stu-id="38977-106">*expression* .Refresh</span></span>

<span data-ttu-id="38977-107">*expression* Variable qui représente un objet **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="38977-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="38977-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="38977-108">Remarks</span></span>

<span data-ttu-id="38977-p101">Pour déterminer la position utilisée par le moteur de base de données Microsoft Access pour les objets **Field** dans la collection **Fields** d'un objet **QueryDef**, **Recordset** ou **TableDef**, utilisez la propriété **OrdinalPosition** de chaque objet **Field**. La modification de la propriété **OrdinalPosition** d'un objet **Field** ne peut pas modifier l'ordre des objets **Field** dans la collection tant que vous n'utilisez pas la méthode **Refresh**.</span><span class="sxs-lookup"><span data-stu-id="38977-p101">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object. Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="38977-p102">Utilisez la méthode **Refresh** dans les environnements multi-utilisateurs dans lesquels les autres utilisateurs peuvent modifier la base de données. Vous avez peut-être besoin également de l'utiliser dans des collections concernées indirectement par les modifications apportées à la base de données. Par exemple, si vous modifiez une collection **Users**, il est peut-être nécessaire d'actualiser une collection **Groups** avant d'utiliser cette collection **Groups**.</span><span class="sxs-lookup"><span data-stu-id="38977-p102">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="38977-p103">Une collection est remplie d'objets lors de son premier référencement et ne reflète pas automatiquement les modifications que les autres utilisateurs apportent par la suite. S'il est probable qu'un autre utilisateur a modifié une collection, appliquez immédiatement la méthode Refresh à la collection avant d'effectuer une tâche dans votre application qui suppose la présence ou l'absence d'un objet déterminé dans la collection. Vous serez ainsi assuré que la collection est parfaitement à jour. D'un autre côté, l'utilisation de la méthode Refresh peut inutilement ralentir les performances.</span><span class="sxs-lookup"><span data-stu-id="38977-p103">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

