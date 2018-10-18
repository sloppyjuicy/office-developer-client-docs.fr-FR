---
title: GetString, méthode (ADO)
TOCTitle: GetString Method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba235094aa7f491cbd86bf753713d50f01009d47
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605400"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="ab54b-102">GetString, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="ab54b-102">GetString Method (ADO)</span></span>


<span data-ttu-id="ab54b-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab54b-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="ab54b-104">Retourne l'objet [Recordset](recordset-object-ado.md) sous la forme d'une chaîne.</span><span class="sxs-lookup"><span data-stu-id="ab54b-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab54b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab54b-105">Syntax</span></span>

<span data-ttu-id="ab54b-106">*Variant* = *jeu d’enregistrements*. GetString (*StringFormat*, *NumLignes*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="ab54b-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

<span data-ttu-id="ab54b-107"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="ab54b-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="ab54b-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ab54b-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="ab54b-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ab54b-109">Return value</span></span>
>>>>>>> <span data-ttu-id="ab54b-110">master</span><span class="sxs-lookup"><span data-stu-id="ab54b-110">master</span></span>

<span data-ttu-id="ab54b-111">Retourne l'objet **Recordset** sous la forme d'un type **Variant** avec une valeur de chaîne (BSTR).</span><span class="sxs-lookup"><span data-stu-id="ab54b-111">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="ab54b-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab54b-112">Parameters</span></span>

  - <span data-ttu-id="ab54b-113">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="ab54b-113">*StringFormat*</span></span>

  - <span data-ttu-id="ab54b-p101">Valeur [StringFormatEnum](stringformatenum.md) qui spécifie comment l’objet **Recordset** doit être converti en chaîne. Les paramètres  *DélimiteurLigne*, *DélimiteurColonne* et *ExprNull* sont utilisés uniquement avec un paramètre \*FormatChaîne \* affecté de la valeur **adClipString**.</span><span class="sxs-lookup"><span data-stu-id="ab54b-p101">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string. The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>

  - <span data-ttu-id="ab54b-116">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="ab54b-116">*NumRows*</span></span>

  - <span data-ttu-id="ab54b-117">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="ab54b-117">Optional.</span></span> <span data-ttu-id="ab54b-118">Nombre de lignes à convertir dans l'objet **RecordSet**.</span><span class="sxs-lookup"><span data-stu-id="ab54b-118">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="ab54b-119">Si *NumRows* n’est pas spécifié, ou si elle est supérieure au nombre total de lignes dans le **jeu d’enregistrements**, toutes les lignes dans le **jeu d’enregistrements** sont convertis.</span><span class="sxs-lookup"><span data-stu-id="ab54b-119">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>

  - <span data-ttu-id="ab54b-120">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="ab54b-120">*ColumnDelimiter*</span></span>

  - <span data-ttu-id="ab54b-p103">Facultatif. Délimiteur utilisé entre les colonnes, s'il est spécifié ; sinon, le caractère de tabulation.</span><span class="sxs-lookup"><span data-stu-id="ab54b-p103">Optional. A delimiter used between columns, if specified, otherwise the TAB character.</span></span>

  - <span data-ttu-id="ab54b-123">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="ab54b-123">*RowDelimiter*</span></span>

  - <span data-ttu-id="ab54b-p104">Facultatif. Délimiteur utilisé entre les lignes, s'il est spécifié ; sinon, le caractère de retour chariot.</span><span class="sxs-lookup"><span data-stu-id="ab54b-p104">Optional. A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>

  - <span data-ttu-id="ab54b-126">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="ab54b-126">*NullExpr*</span></span>

  - <span data-ttu-id="ab54b-p105">Facultatif. Expression utilisée à la place d'une valeur NULL, si elle est spécifiée ; sinon, la chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="ab54b-p105">Optional. An expression used in place of a null value, if specified, otherwise the empty string.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab54b-129">Notes</span><span class="sxs-lookup"><span data-stu-id="ab54b-129">Remarks</span></span>

<span data-ttu-id="ab54b-p106">Les données de ligne, mais pas les données de schéma, sont enregistrées dans la chaîne. Il est donc impossible de rouvrir un objet **Recordset** à l'aide de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="ab54b-p106">Row data, but no schema data, is saved to the string. Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="ab54b-132">Cette méthode est équivalente à la méthode **GetClipString** RDO.</span><span class="sxs-lookup"><span data-stu-id="ab54b-132">This method is equivalent to the RDO **GetClipString** method.</span></span>

