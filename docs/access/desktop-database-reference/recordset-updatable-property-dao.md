---
title: Propriété Recordset.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 2d4bdcef-1b10-b542-ce0f-6172c271131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192110(v=office.15)
ms:contentKeyID: 48543968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a7f5d803c64504c598a96c244db3fcf75bf0dd5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919261"
---
# <a name="recordsetupdatable-property-dao"></a><span data-ttu-id="ebf5a-102">Propriété Recordset.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="ebf5a-102">Recordset.Updatable property (DAO)</span></span>


<span data-ttu-id="ebf5a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ebf5a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ebf5a-p101">Renvoie une valeur indiquant si vous pouvez modifier un objet DAO. Type **Boolean** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebf5a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebf5a-106">Syntax</span></span>

<span data-ttu-id="ebf5a-107">*expression* . Mise à jour</span><span class="sxs-lookup"><span data-stu-id="ebf5a-107">*expression* .Updatable</span></span>

<span data-ttu-id="ebf5a-108">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="ebf5a-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebf5a-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="ebf5a-109">Remarks</span></span>

<span data-ttu-id="ebf5a-110">Les objets Recordset et transférer-only type instantané renvoient toujours **False**.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-110">Snapshot- and forward-only–type Recordset objects always return **False**.</span></span>

<span data-ttu-id="ebf5a-p102">De nombreux types d'objets peuvent contenir des champs non modifiables. Par exemple, vous pouvez créer un objet **Recordset** de type feuille de réponse dynamique dans lequel seuls certains champs peuvent être modifiés. Il peut s'agir de champs fixes ou contenant des données incrémentées automatiquement. Il est également possible que la feuille de réponse dynamique soit le résultat d'une requête qui combine des tables modifiables et non modifiables.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-p102">Many types of objects can contain fields that can't be updated. For example, you can create a dynaset-type **Recordset** object in which only some fields can be changed. These fields can be fixed or contain data that increments automatically, or the dynaset can result from a query that combines updatable and nonupdatable tables.</span></span>

<span data-ttu-id="ebf5a-p103">Si l'objet ne contient que des champs en lecture seule, la valeur de la propriété **Updatable** est **False**. Lorsqu'un ou plusieurs champs sont modifiables, la valeur de la propriété est **True**. Vous ne pouvez mettre à jour que les champs modifiables. Une erreur piégeable se produit lorsque vous tentez d'affecter une nouvelle valeur à un champ en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-p103">If the object contains only read-only fields, the value of the **Updatable** property is **False**. When one or more fields are updatable, the property's value is **True**. You can edit only the updatable fields. A trappable error occurs if you try to assign a new value to a read-only field.</span></span>

<span data-ttu-id="ebf5a-118">Dans la mesure où un objet modifiable peut contenir des champs en lecture seule, vérifiez la propriété **DataUpdatable** de chaque champ de la collection **Fields** d'un objet **Recordset** avant de modifier un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ebf5a-118">Because an updatable object can contain read-only fields, check the **DataUpdatable** property of each field in the **Fields** collection of a **Recordset** object before you edit a record.</span></span>

