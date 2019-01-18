---
title: GetString, méthode (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ea28efb8fdeaa0643d1d940419b7650527ddf6e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698210"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="d029c-102">GetString, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="d029c-102">GetString method (ADO)</span></span>

<span data-ttu-id="d029c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d029c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d029c-104">Retourne l'objet [Recordset](recordset-object-ado.md) sous la forme d'une chaîne.</span><span class="sxs-lookup"><span data-stu-id="d029c-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="d029c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d029c-105">Syntax</span></span>

<span data-ttu-id="d029c-106">*Variant* = *jeu d’enregistrements*. GetString (*StringFormat*, *NumLignes*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="d029c-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="d029c-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d029c-107">Return value</span></span>

<span data-ttu-id="d029c-108">Retourne l'objet **Recordset** sous la forme d'un type **Variant** avec une valeur de chaîne (BSTR).</span><span class="sxs-lookup"><span data-stu-id="d029c-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="d029c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d029c-109">Parameters</span></span>

|<span data-ttu-id="d029c-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d029c-110">Parameter</span></span>|<span data-ttu-id="d029c-111">Description</span><span class="sxs-lookup"><span data-stu-id="d029c-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d029c-112">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="d029c-112">*StringFormat*</span></span> |<span data-ttu-id="d029c-p101">Valeur [StringFormatEnum](stringformatenum.md) qui spécifie comment l’objet **Recordset** doit être converti en chaîne. Les paramètres  *DélimiteurLigne*, *DélimiteurColonne* et *ExprNull* sont utilisés uniquement avec un paramètre \*FormatChaîne \* affecté de la valeur **adClipString**.</span><span class="sxs-lookup"><span data-stu-id="d029c-p101">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string. The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>|
|<span data-ttu-id="d029c-115">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="d029c-115">*NumRows*</span></span> |<span data-ttu-id="d029c-116">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="d029c-116">Optional.</span></span> <span data-ttu-id="d029c-117">Nombre de lignes à convertir dans l'objet **RecordSet**.</span><span class="sxs-lookup"><span data-stu-id="d029c-117">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="d029c-118">Si *NumRows* n’est pas spécifié, ou si elle est supérieure au nombre total de lignes dans le **jeu d’enregistrements**, toutes les lignes dans le **jeu d’enregistrements** sont convertis.</span><span class="sxs-lookup"><span data-stu-id="d029c-118">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>|
|<span data-ttu-id="d029c-119">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="d029c-119">*ColumnDelimiter*</span></span> |<span data-ttu-id="d029c-p103">Facultatif. Délimiteur utilisé entre les colonnes, s'il est spécifié ; sinon, le caractère de tabulation.</span><span class="sxs-lookup"><span data-stu-id="d029c-p103">Optional. A delimiter used between columns, if specified, otherwise the TAB character.</span></span>|
|<span data-ttu-id="d029c-122">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="d029c-122">*RowDelimiter*</span></span> |<span data-ttu-id="d029c-p104">Facultatif. Délimiteur utilisé entre les lignes, s'il est spécifié ; sinon, le caractère de retour chariot.</span><span class="sxs-lookup"><span data-stu-id="d029c-p104">Optional. A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>|
|<span data-ttu-id="d029c-125">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="d029c-125">*NullExpr*</span></span> |<span data-ttu-id="d029c-p105">Facultatif. Expression utilisée à la place d'une valeur NULL, si elle est spécifiée ; sinon, la chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="d029c-p105">Optional. An expression used in place of a null value, if specified, otherwise the empty string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d029c-128">Notes</span><span class="sxs-lookup"><span data-stu-id="d029c-128">Remarks</span></span>

<span data-ttu-id="d029c-p106">Les données de ligne, mais pas les données de schéma, sont enregistrées dans la chaîne. Il est donc impossible de rouvrir un objet **Recordset** à l'aide de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="d029c-p106">Row data, but no schema data, is saved to the string. Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="d029c-131">Cette méthode est équivalente à la méthode **GetClipString** RDO.</span><span class="sxs-lookup"><span data-stu-id="d029c-131">This method is equivalent to the RDO **GetClipString** method.</span></span>

