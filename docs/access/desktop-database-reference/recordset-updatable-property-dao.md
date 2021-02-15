---
title: Recordset.Updatable, propriété (DAO)
TOCTitle: Updatable Property
ms:assetid: 2d4bdcef-1b10-b542-ce0f-6172c271131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192110(v=office.15)
ms:contentKeyID: 48543968
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 722ccc2334cd00ed89a1193709023db039ba9fd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307545"
---
# <a name="recordsetupdatable-property-dao"></a><span data-ttu-id="8be6c-102">Recordset.Updatable, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="8be6c-102">Recordset.Updatable property (DAO)</span></span>


<span data-ttu-id="8be6c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8be6c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8be6c-104">Renvoie une valeur qui indique si vous pouvez changer un objet DAO.</span><span class="sxs-lookup"><span data-stu-id="8be6c-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="8be6c-105">**Boolean** (en lecture seule).</span><span class="sxs-lookup"><span data-stu-id="8be6c-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8be6c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8be6c-106">Syntax</span></span>

<span data-ttu-id="8be6c-107">*.* Updatable</span><span class="sxs-lookup"><span data-stu-id="8be6c-107">*expression* .Updatable</span></span>

<span data-ttu-id="8be6c-108">*expression* Variable qui représente un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="8be6c-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8be6c-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="8be6c-109">Remarks</span></span>

<span data-ttu-id="8be6c-110">Les objets Recordset de type capture instantanée et avant uniquement retournent toujours **la forme False**.</span><span class="sxs-lookup"><span data-stu-id="8be6c-110">Snapshot- and forward-only–type Recordset objects always return **False**.</span></span>

<span data-ttu-id="8be6c-p102">De nombreux types d'objets peuvent contenir des champs non modifiables. Par exemple, vous pouvez créer un objet **Recordset** de type feuille de réponse dynamique dans lequel seuls certains champs peuvent être modifiés. Il peut s'agir de champs fixes ou contenant des données incrémentées automatiquement. Il est également possible que la feuille de réponse dynamique soit le résultat d'une requête qui combine des tables modifiables et non modifiables.</span><span class="sxs-lookup"><span data-stu-id="8be6c-p102">Many types of objects can contain fields that can't be updated. For example, you can create a dynaset-type **Recordset** object in which only some fields can be changed. These fields can be fixed or contain data that increments automatically, or the dynaset can result from a query that combines updatable and nonupdatable tables.</span></span>

<span data-ttu-id="8be6c-p103">Si l'objet ne contient que des champs en lecture seule, la valeur de la propriété **Updatable** est **False**. Lorsqu'un ou plusieurs champs sont modifiables, la valeur de la propriété est **True**. Vous ne pouvez mettre à jour que les champs modifiables. Une erreur piégeable se produit lorsque vous tentez d'affecter une nouvelle valeur à un champ en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8be6c-p103">If the object contains only read-only fields, the value of the **Updatable** property is **False**. When one or more fields are updatable, the property's value is **True**. You can edit only the updatable fields. A trappable error occurs if you try to assign a new value to a read-only field.</span></span>

<span data-ttu-id="8be6c-118">Dans la mesure où un objet modifiable peut contenir des champs en lecture seule, vérifiez la propriété **DataUpdatable** de chaque champ de la collection **Fields** d'un objet **Recordset** avant de modifier un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8be6c-118">Because an updatable object can contain read-only fields, check the **DataUpdatable** property of each field in the **Fields** collection of a **Recordset** object before you edit a record.</span></span>

