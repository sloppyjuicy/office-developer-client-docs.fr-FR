---
title: RowPosition, propriété (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0adb1cdf9ce7b096d7b80b86a89a819d5789b60b
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949382"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="f3f4a-102">RowPosition, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="f3f4a-102">RowPosition property (ADO)</span></span>

<span data-ttu-id="f3f4a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3f4a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f3f4a-104">Récupère ou définit un objet **RowPosition** OLE DB à partir de/sur un objet **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="f3f4a-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="f3f4a-105">Lorsque vous utilisez **put\_RowPosition** pour définir l’objet **RowPosition** , l’objet **Recordset** résultant utilise l’objet **RowPosition** pour déterminer la ligne active.</span><span class="sxs-lookup"><span data-stu-id="f3f4a-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="f3f4a-106">Lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f3f4a-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3f4a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3f4a-107">Syntax</span></span>

<span data-ttu-id="f3f4a-108">Get HRESULT\_RowPosition (\[out, retval\] IUnknown\* \* ppRowPos) ;</span><span class="sxs-lookup"><span data-stu-id="f3f4a-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="f3f4a-109">Placer HRESULT\_RowPosition (\[dans\] IUnknown\* pRowPos) ;</span><span class="sxs-lookup"><span data-stu-id="f3f4a-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="f3f4a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3f4a-110">Parameters</span></span>

|<span data-ttu-id="f3f4a-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f3f4a-111">Parameter</span></span>|<span data-ttu-id="f3f4a-112">Description</span><span class="sxs-lookup"><span data-stu-id="f3f4a-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f3f4a-113">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="f3f4a-113">*ppRowPos*</span></span> |<span data-ttu-id="f3f4a-114">Pointeur vers un objet **RowPosition** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f3f4a-114">Pointer to an OLE DB **RowPosition** object.</span></span>|
|<span data-ttu-id="f3f4a-115">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="f3f4a-115">*PRowPos*</span></span> |<span data-ttu-id="f3f4a-116">Objet **RowPosition** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f3f4a-116">An OLE DB **RowPosition** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="f3f4a-117">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="f3f4a-117">Return values</span></span>

<span data-ttu-id="f3f4a-118">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="f3f4a-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3f4a-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="f3f4a-119">Remarks</span></span>

<span data-ttu-id="f3f4a-120">Lorsque cette propriété est définie, si l’objet **Rowset** de l’objet **RowPosition** est différent de l’objet **Rowset** de l’objet **Recordset** , le premier remplace ce dernier.</span><span class="sxs-lookup"><span data-stu-id="f3f4a-120">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter.</span></span> <span data-ttu-id="f3f4a-121">Le même comportement s’applique au **chapitre** actif à la **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="f3f4a-121">The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f3f4a-122">S’applique à</span><span class="sxs-lookup"><span data-stu-id="f3f4a-122">Applies to</span></span>

[<span data-ttu-id="f3f4a-123">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="f3f4a-123">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

