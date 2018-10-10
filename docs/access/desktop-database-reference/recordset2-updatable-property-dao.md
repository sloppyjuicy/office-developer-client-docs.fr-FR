---
title: Recordset2.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: ad8184b6-ffe3-dde6-ddee-4b23cdaa9c59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821726(v=office.15)
ms:contentKeyID: 48547041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 54ec9af0b8fa1948afe568dc57eacf9962283504
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469608"
---
# <a name="recordset2updatable-property-dao"></a><span data-ttu-id="9d3ff-102">Recordset2.Updatable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="9d3ff-102">Recordset2.Updatable Property (DAO)</span></span>


<span data-ttu-id="9d3ff-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d3ff-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9d3ff-p101">Renvoie une valeur indiquant si vous pouvez modifier un objet DAO. Type **Boolean** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d3ff-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d3ff-106">Syntax</span></span>

<span data-ttu-id="9d3ff-107">*expression* . Mise à jour</span><span class="sxs-lookup"><span data-stu-id="9d3ff-107">*expression* .Updatable</span></span>

<span data-ttu-id="9d3ff-108">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="9d3ff-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d3ff-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="9d3ff-109">Remarks</span></span>

<span data-ttu-id="9d3ff-110">Les objets Recordset et transférer-only type instantané renvoient toujours **False**.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-110">Snapshot- and forward-only–type Recordset objects always return **False**.</span></span>

<span data-ttu-id="9d3ff-p102">De nombreux types d'objets peuvent contenir des champs non modifiables. Par exemple, vous pouvez créer un objet **Recordset** de type feuille de réponse dynamique dans lequel seuls certains champs peuvent être modifiés. Il peut s'agir de champs fixes ou contenant des données incrémentées automatiquement. Il est également possible que la feuille de réponse dynamique soit le résultat d'une requête qui combine des tables modifiables et non modifiables.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-p102">Many types of objects can contain fields that can't be updated. For example, you can create a dynaset-type **Recordset** object in which only some fields can be changed. These fields can be fixed or contain data that increments automatically, or the dynaset can result from a query that combines updatable and nonupdatable tables.</span></span>

<span data-ttu-id="9d3ff-p103">Si l'objet ne contient que des champs en lecture seule, la valeur de la propriété **Updatable** est **False**. Lorsqu'un ou plusieurs champs sont modifiables, la valeur de la propriété est **True**. Vous ne pouvez mettre à jour que les champs modifiables. Une erreur piégeable se produit lorsque vous tentez d'affecter une nouvelle valeur à un champ en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-p103">If the object contains only read-only fields, the value of the **Updatable** property is **False**. When one or more fields are updatable, the property's value is **True**. You can edit only the updatable fields. A trappable error occurs if you try to assign a new value to a read-only field.</span></span>

<span data-ttu-id="9d3ff-118">Dans la mesure où un objet modifiable peut contenir des champs en lecture seule, vérifiez la propriété **DataUpdatable** de chaque champ de la collection **Fields** d'un objet **Recordset** avant de modifier un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-118">Because an updatable object can contain read-only fields, check the **DataUpdatable** property of each field in the **Fields** collection of a **Recordset** object before you edit a record.</span></span>

