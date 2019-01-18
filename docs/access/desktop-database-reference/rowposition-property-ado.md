---
title: RowPosition, propriété (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84d3ad7cc5b3d43b15ac1113f6fa00932678ebc3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720960"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="3bc3f-102">RowPosition, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="3bc3f-102">RowPosition property (ADO)</span></span>

<span data-ttu-id="3bc3f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3bc3f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3bc3f-104">Récupère ou définit un objet **RowPosition** OLE DB à partir de/sur un objet **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="3bc3f-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="3bc3f-105">Lorsque vous utilisez **put\_RowPosition** pour définir l’objet **RowPosition** , l’objet **Recordset** résultant utilise l’objet **RowPosition** pour déterminer la ligne active.</span><span class="sxs-lookup"><span data-stu-id="3bc3f-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="3bc3f-106">Lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="3bc3f-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bc3f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3bc3f-107">Syntax</span></span>

<span data-ttu-id="3bc3f-108">Get HRESULT\_RowPosition (\[out, retval\] IUnknown\* \* ppRowPos) ;</span><span class="sxs-lookup"><span data-stu-id="3bc3f-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="3bc3f-109">Placer HRESULT\_RowPosition (\[dans\] IUnknown\* pRowPos) ;</span><span class="sxs-lookup"><span data-stu-id="3bc3f-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="3bc3f-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="3bc3f-110">Parameters</span></span>

|<span data-ttu-id="3bc3f-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3bc3f-111">Parameter</span></span>|<span data-ttu-id="3bc3f-112">Description</span><span class="sxs-lookup"><span data-stu-id="3bc3f-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3bc3f-113">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="3bc3f-113">*ppRowPos*</span></span> |<span data-ttu-id="3bc3f-114">Pointeur vers un objet **RowPosition** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="3bc3f-114">Pointer to an OLE DB **RowPosition** object.</span></span>|
|<span data-ttu-id="3bc3f-115">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="3bc3f-115">*PRowPos*</span></span> |<span data-ttu-id="3bc3f-116">Objet **RowPosition** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="3bc3f-116">An OLE DB **RowPosition** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="3bc3f-117">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="3bc3f-117">Return values</span></span>

<span data-ttu-id="3bc3f-118">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="3bc3f-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bc3f-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="3bc3f-119">Remarks</span></span>

<span data-ttu-id="3bc3f-120">Lorsque cette propriété est définie, si l’objet **Rowset** de l’objet **RowPosition** est différent de l’objet **Rowset** de l’objet **Recordset** , le premier remplace ce dernier.</span><span class="sxs-lookup"><span data-stu-id="3bc3f-120">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter.</span></span> <span data-ttu-id="3bc3f-121">Le même comportement s’applique au **chapitre** actif à la **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="3bc3f-121">The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3bc3f-122">S’applique à</span><span class="sxs-lookup"><span data-stu-id="3bc3f-122">Applies to</span></span>

[<span data-ttu-id="3bc3f-123">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="3bc3f-123">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

