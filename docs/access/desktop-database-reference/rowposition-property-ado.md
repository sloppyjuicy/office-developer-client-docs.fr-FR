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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306859"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="dcb42-102">RowPosition, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="dcb42-102">RowPosition property (ADO)</span></span>

<span data-ttu-id="dcb42-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dcb42-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dcb42-104">Récupère ou définit un objet **RowPosition** OLE DB à partir de/sur un objet **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="dcb42-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="dcb42-105">Lorsque vous utilisez **la valeur \_ RowPosition** pour définir l’objet **RowPosition,** l’objet **Recordset** qui en résulte utilise l’objet **RowPosition** pour déterminer la ligne en cours.</span><span class="sxs-lookup"><span data-stu-id="dcb42-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="dcb42-106">Lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="dcb42-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcb42-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcb42-107">Syntax</span></span>

<span data-ttu-id="dcb42-108">HRESULT get \_ RowPosition( \[ out, retval \] IUnknown \* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="dcb42-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="dcb42-109">HRESULT put \_ RowPosition( \[ in \] IUnknown \* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="dcb42-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="dcb42-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dcb42-110">Parameters</span></span>

|<span data-ttu-id="dcb42-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="dcb42-111">Parameter</span></span>|<span data-ttu-id="dcb42-112">Description</span><span class="sxs-lookup"><span data-stu-id="dcb42-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="dcb42-113">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="dcb42-113">*ppRowPos*</span></span> |<span data-ttu-id="dcb42-114">Pointeur vers un objet **RowPosition** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="dcb42-114">Pointer to an OLE DB **RowPosition** object.</span></span>|
|<span data-ttu-id="dcb42-115">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="dcb42-115">*PRowPos*</span></span> |<span data-ttu-id="dcb42-116">Objet **RowPosition** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="dcb42-116">An OLE DB **RowPosition** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="dcb42-117">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="dcb42-117">Return values</span></span>

<span data-ttu-id="dcb42-118">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S \_ OK et E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="dcb42-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcb42-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="dcb42-119">Remarks</span></span>

<span data-ttu-id="dcb42-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span><span class="sxs-lookup"><span data-stu-id="dcb42-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="dcb42-122">S’applique à</span><span class="sxs-lookup"><span data-stu-id="dcb42-122">Applies to</span></span>

[<span data-ttu-id="dcb42-123">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="dcb42-123">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

