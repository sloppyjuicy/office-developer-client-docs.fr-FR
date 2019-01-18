---
title: Rowset, propriété (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2a4855b3411a11ddd5a76225acaa52344877a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706141"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="fcb42-102">Rowset, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="fcb42-102">Rowset property (ADO)</span></span>

<span data-ttu-id="fcb42-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fcb42-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fcb42-104">Récupère ou définit un objet **Rowset** OLE DB sur un objet **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="fcb42-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="fcb42-105">Lorsque vous utilisez put\_Rowset, l’ensemble de lignes est transformé en un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="fcb42-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="fcb42-106">Lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="fcb42-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcb42-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fcb42-107">Syntax</span></span>

<span data-ttu-id="fcb42-108">Get HRESULT\_Rowset (\[out, retval\] IUnknown\* \* ppRowset) ;</span><span class="sxs-lookup"><span data-stu-id="fcb42-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="fcb42-109">Placer HRESULT\_Rowset (\[dans\] IUnknown\* pRowset) ;</span><span class="sxs-lookup"><span data-stu-id="fcb42-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="fcb42-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="fcb42-110">Parameters</span></span>

|<span data-ttu-id="fcb42-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="fcb42-111">Parameter</span></span>|<span data-ttu-id="fcb42-112">Description</span><span class="sxs-lookup"><span data-stu-id="fcb42-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="fcb42-113">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="fcb42-113">*ppRowset*</span></span> |<span data-ttu-id="fcb42-114">Pointeur vers un objet **Rowset** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="fcb42-114">Pointer to an OLE DB **Rowset** object.</span></span>|
|<span data-ttu-id="fcb42-115">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="fcb42-115">*PRowset*</span></span> |<span data-ttu-id="fcb42-116">Objet **Rowset** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="fcb42-116">An OLE DB **Rowset** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="fcb42-117">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="fcb42-117">Return values</span></span>

<span data-ttu-id="fcb42-118">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="fcb42-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="fcb42-119">S’applique à</span><span class="sxs-lookup"><span data-stu-id="fcb42-119">Applies to</span></span>

[<span data-ttu-id="fcb42-120">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="fcb42-120">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

