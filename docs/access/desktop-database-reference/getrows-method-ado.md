---
title: GetRows, méthode (ADO)
TOCTitle: GetRows method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 853f971f68bb0ec4069ba58e04b7cf9d231c6467
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949858"
---
# <a name="getrows-method-ado"></a><span data-ttu-id="2a5ea-102">GetRows, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="2a5ea-102">GetRows method (ADO)</span></span>

<span data-ttu-id="2a5ea-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a5ea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2a5ea-104">Récupère plusieurs enregistrements d'un objet [Recordset](recordset-object-ado.md) dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="2a5ea-104">Retrieves multiple records of a [Recordset](recordset-object-ado.md) object into an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a5ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a5ea-105">Syntax</span></span>

<span data-ttu-id="2a5ea-106">*tableau* = *jeu d’enregistrements*. GetRows (*lignes*, *Démarrez*, *champs* )</span><span class="sxs-lookup"><span data-stu-id="2a5ea-106">*array* = *recordset*.GetRows(*Rows*, *Start*, *Fields* )</span></span>

## <a name="return-value"></a><span data-ttu-id="2a5ea-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2a5ea-107">Return value</span></span>

<span data-ttu-id="2a5ea-108">Retourne une valeur de type **Variant** qui représente un tableau à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="2a5ea-108">Returns a **Variant** whose value is a two-dimensional array.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a5ea-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a5ea-109">Parameters</span></span>

|<span data-ttu-id="2a5ea-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="2a5ea-110">Parameter</span></span>|<span data-ttu-id="2a5ea-111">Description</span><span class="sxs-lookup"><span data-stu-id="2a5ea-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2a5ea-112">*Lignes*</span><span class="sxs-lookup"><span data-stu-id="2a5ea-112">*Rows*</span></span> |<span data-ttu-id="2a5ea-p101">Facultatif. Valeur [GetRowsOptionEnum](getrowsoptionenum.md) qui indique le nombre d'enregistrements à récupérer. La valeur par défaut est **adGetRowsRest**.</span><span class="sxs-lookup"><span data-stu-id="2a5ea-p101">Optional. A [GetRowsOptionEnum](getrowsoptionenum.md) value that indicates the number of records to retrieve. The default is **adGetRowsRest**.</span></span>|
|<span data-ttu-id="2a5ea-116">*Début*</span><span class="sxs-lookup"><span data-stu-id="2a5ea-116">*Start*</span></span> |<span data-ttu-id="2a5ea-p102">Facultatif. Valeur de type **String** ou **Variant** qui correspond au signet de l'enregistrement à partir duquel l'opération **GetRows** doit commencer. Vous pouvez également utiliser une valeur [BookmarkEnum](bookmarkenum.md).</span><span class="sxs-lookup"><span data-stu-id="2a5ea-p102">Optional. A **String** value or **Variant** that evaluates to the bookmark for the record from which the **GetRows** operation should begin. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>|
|<span data-ttu-id="2a5ea-120">*Champs*</span><span class="sxs-lookup"><span data-stu-id="2a5ea-120">*Fields*</span></span> |<span data-ttu-id="2a5ea-p103">Facultatif. **Variant** qui représente un seul nom de champ ou position ordinale, ou un tableau de noms de champs ou de positions ordinales. ADO retourne uniquement les données de ces champs.</span><span class="sxs-lookup"><span data-stu-id="2a5ea-p103">Optional. A **Variant** that represents a single field name or ordinal position, or an array of field names or ordinal position numbers. ADO returns only the data in these fields.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2a5ea-124">Notes</span><span class="sxs-lookup"><span data-stu-id="2a5ea-124">Remarks</span></span>

<span data-ttu-id="2a5ea-125">Utilisez la méthode **GetRows** pour copier des enregistrements d'un objet **Recordset** dans un tableau à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="2a5ea-125">Use the **GetRows** method to copy records from a **Recordset** into a two-dimensional array.</span></span> <span data-ttu-id="2a5ea-126">Le premier indice identifie le champ et le second le numéro d'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2a5ea-126">The first subscript identifies the field and the second identifies the record number.</span></span> <span data-ttu-id="2a5ea-127">La variable du *tableau* est automatiquement dimensionnée à la taille correcte lorsque la méthode **GetRows** renvoie les données.</span><span class="sxs-lookup"><span data-stu-id="2a5ea-127">The *array* variable is automatically dimensioned to the correct size when the **GetRows** method returns the data.</span></span>

<span data-ttu-id="2a5ea-128">Si vous ne spécifiez pas de valeur pour l’argument *lignes* , la méthode **GetRows** récupère automatiquement tous les enregistrements dans l’objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="2a5ea-128">If you do not specify a value for the *Rows* argument, the **GetRows** method automatically retrieves all the records in the **Recordset** object.</span></span> <span data-ttu-id="2a5ea-129">Si vous demandez plus d'enregistrements que le nombre disponible, **GetRows** retourne uniquement le nombre d'enregistrements disponibles.</span><span class="sxs-lookup"><span data-stu-id="2a5ea-129">If you request more records than are available, **GetRows** returns only the number of available records.</span></span>

<span data-ttu-id="2a5ea-130">Si l’objet **Recordset** prend en charge les signets, vous pouvez spécifier à quel enregistrement la méthode **GetRows** doit commencer à extraire des données en passant la valeur de la propriété [Bookmark](bookmark-property-ado.md) de cet enregistrement dans l’argument *début* .</span><span class="sxs-lookup"><span data-stu-id="2a5ea-130">If the **Recordset** object supports bookmarks, you can specify at which record the **GetRows** method should begin retrieving data by passing the value of that record's [Bookmark](bookmark-property-ado.md) property in the *Start* argument.</span></span>

<span data-ttu-id="2a5ea-131">Si vous souhaitez restreindre les champs de l’appel de **GetRows** , vous pouvez passer un seul nom/numéro ou un tableau de noms/numéros de champ dans l’argument *champs* .</span><span class="sxs-lookup"><span data-stu-id="2a5ea-131">If you want to restrict the fields that the **GetRows** call returns, you can pass either a single field name/number or an array of field names/numbers in the *Fields* argument.</span></span>

<span data-ttu-id="2a5ea-132">Après avoir appelé **GetRows**, l'enregistrement suivant non lu devient l'enregistrement actif ou, s'il n'y a plus aucun enregistrement, la propriété [EOF](bof-eof-properties-ado.md) a la valeur **True**.</span><span class="sxs-lookup"><span data-stu-id="2a5ea-132">After you call **GetRows**, the next unread record becomes the current record, or the [EOF](bof-eof-properties-ado.md) property is set to **True** if there are no more records.</span></span>

