---
title: GetRows, méthode (ADO)
TOCTitle: GetRows Method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 99988383c40b84e1993582ad0d1c07491de82933
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879878"
---
# <a name="getrows-method-ado"></a><span data-ttu-id="07307-102">GetRows, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="07307-102">GetRows Method (ADO)</span></span>


<span data-ttu-id="07307-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="07307-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="07307-104">Récupère plusieurs enregistrements d'un objet [Recordset](recordset-object-ado.md) dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="07307-104">Retrieves multiple records of a [Recordset](recordset-object-ado.md) object into an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="07307-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07307-105">Syntax</span></span>

<span data-ttu-id="07307-106">*tableau* = *jeu d’enregistrements*. GetRows (*lignes*, *Démarrez*, *champs* )</span><span class="sxs-lookup"><span data-stu-id="07307-106">*array* = *recordset*.GetRows(*Rows*, *Start*, *Fields* )</span></span>

## <a name="return-value"></a><span data-ttu-id="07307-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="07307-107">Return value</span></span>

<span data-ttu-id="07307-108">Retourne une valeur de type **Variant** qui représente un tableau à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="07307-108">Returns a **Variant** whose value is a two-dimensional array.</span></span>

## <a name="parameters"></a><span data-ttu-id="07307-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07307-109">Parameters</span></span>

  - <span data-ttu-id="07307-110">*Lignes*</span><span class="sxs-lookup"><span data-stu-id="07307-110">*Rows*</span></span>

  - <span data-ttu-id="07307-p101">Facultatif. Valeur [GetRowsOptionEnum](getrowsoptionenum.md) qui indique le nombre d'enregistrements à récupérer. La valeur par défaut est **adGetRowsRest**.</span><span class="sxs-lookup"><span data-stu-id="07307-p101">Optional. A [GetRowsOptionEnum](getrowsoptionenum.md) value that indicates the number of records to retrieve. The default is **adGetRowsRest**.</span></span>

  - <span data-ttu-id="07307-114">*Début*</span><span class="sxs-lookup"><span data-stu-id="07307-114">*Start*</span></span>

  - <span data-ttu-id="07307-p102">Facultatif. Valeur de type **String** ou **Variant** qui correspond au signet de l'enregistrement à partir duquel l'opération **GetRows** doit commencer. Vous pouvez également utiliser une valeur [BookmarkEnum](bookmarkenum.md).</span><span class="sxs-lookup"><span data-stu-id="07307-p102">Optional. A **String** value or **Variant** that evaluates to the bookmark for the record from which the **GetRows** operation should begin. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>

  - <span data-ttu-id="07307-118">*Champs*</span><span class="sxs-lookup"><span data-stu-id="07307-118">*Fields*</span></span>

  - <span data-ttu-id="07307-p103">Facultatif. **Variant** qui représente un seul nom de champ ou position ordinale, ou un tableau de noms de champs ou de positions ordinales. ADO retourne uniquement les données de ces champs.</span><span class="sxs-lookup"><span data-stu-id="07307-p103">Optional. A **Variant** that represents a single field name or ordinal position, or an array of field names or ordinal position numbers. ADO returns only the data in these fields.</span></span>

## <a name="remarks"></a><span data-ttu-id="07307-122">Notes</span><span class="sxs-lookup"><span data-stu-id="07307-122">Remarks</span></span>

<span data-ttu-id="07307-123">Utilisez la méthode **GetRows** pour copier des enregistrements d'un objet **Recordset** dans un tableau à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="07307-123">Use the **GetRows** method to copy records from a **Recordset** into a two-dimensional array.</span></span> <span data-ttu-id="07307-124">Le premier indice identifie le champ et le second le numéro d'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="07307-124">The first subscript identifies the field and the second identifies the record number.</span></span> <span data-ttu-id="07307-125">La variable du *tableau* est automatiquement dimensionnée à la taille correcte lorsque la méthode **GetRows** renvoie les données.</span><span class="sxs-lookup"><span data-stu-id="07307-125">The *array* variable is automatically dimensioned to the correct size when the **GetRows** method returns the data.</span></span>

<span data-ttu-id="07307-126">Si vous ne spécifiez pas de valeur pour l’argument *lignes* , la méthode **GetRows** récupère automatiquement tous les enregistrements dans l’objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="07307-126">If you do not specify a value for the *Rows* argument, the **GetRows** method automatically retrieves all the records in the **Recordset** object.</span></span> <span data-ttu-id="07307-127">Si vous demandez plus d'enregistrements que le nombre disponible, **GetRows** retourne uniquement le nombre d'enregistrements disponibles.</span><span class="sxs-lookup"><span data-stu-id="07307-127">If you request more records than are available, **GetRows** returns only the number of available records.</span></span>

<span data-ttu-id="07307-128">Si l’objet **Recordset** prend en charge les signets, vous pouvez spécifier à quel enregistrement la méthode **GetRows** doit commencer à extraire des données en passant la valeur de la propriété [Bookmark](bookmark-property-ado.md) de cet enregistrement dans l’argument *début* .</span><span class="sxs-lookup"><span data-stu-id="07307-128">If the **Recordset** object supports bookmarks, you can specify at which record the **GetRows** method should begin retrieving data by passing the value of that record's [Bookmark](bookmark-property-ado.md) property in the *Start* argument.</span></span>

<span data-ttu-id="07307-129">Si vous souhaitez restreindre les champs de l’appel de **GetRows** , vous pouvez passer un seul nom/numéro ou un tableau de noms/numéros de champ dans l’argument *champs* .</span><span class="sxs-lookup"><span data-stu-id="07307-129">If you want to restrict the fields that the **GetRows** call returns, you can pass either a single field name/number or an array of field names/numbers in the *Fields* argument.</span></span>

<span data-ttu-id="07307-130">Après avoir appelé **GetRows**, l'enregistrement suivant non lu devient l'enregistrement actif ou, s'il n'y a plus aucun enregistrement, la propriété [EOF](bof-eof-properties-ado.md) a la valeur **True**.</span><span class="sxs-lookup"><span data-stu-id="07307-130">After you call **GetRows**, the next unread record becomes the current record, or the [EOF](bof-eof-properties-ado.md) property is set to **True** if there are no more records.</span></span>

