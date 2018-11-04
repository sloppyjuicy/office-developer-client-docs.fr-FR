---
title: Rowset, propriété (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d5979cb42e2ed4a979dc07016a4bb02b8097994
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949788"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="1e2b5-102">Rowset, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="1e2b5-102">Rowset property (ADO)</span></span>

<span data-ttu-id="1e2b5-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e2b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1e2b5-104">Récupère ou définit un objet **Rowset** OLE DB sur un objet **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="1e2b5-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="1e2b5-105">Lorsque vous utilisez put\_Rowset, l’ensemble de lignes est transformé en un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="1e2b5-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="1e2b5-106">Lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1e2b5-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e2b5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e2b5-107">Syntax</span></span>

<span data-ttu-id="1e2b5-108">Get HRESULT\_Rowset (\[out, retval\] IUnknown\* \* ppRowset) ;</span><span class="sxs-lookup"><span data-stu-id="1e2b5-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="1e2b5-109">Placer HRESULT\_Rowset (\[dans\] IUnknown\* pRowset) ;</span><span class="sxs-lookup"><span data-stu-id="1e2b5-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="1e2b5-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e2b5-110">Parameters</span></span>

|<span data-ttu-id="1e2b5-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1e2b5-111">Parameter</span></span>|<span data-ttu-id="1e2b5-112">Description</span><span class="sxs-lookup"><span data-stu-id="1e2b5-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1e2b5-113">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="1e2b5-113">*ppRowset*</span></span> |<span data-ttu-id="1e2b5-114">Pointeur vers un objet **Rowset** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1e2b5-114">Pointer to an OLE DB **Rowset** object.</span></span>|
|<span data-ttu-id="1e2b5-115">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="1e2b5-115">*PRowset*</span></span> |<span data-ttu-id="1e2b5-116">Objet **Rowset** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1e2b5-116">An OLE DB **Rowset** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="1e2b5-117">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="1e2b5-117">Return values</span></span>

<span data-ttu-id="1e2b5-118">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="1e2b5-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1e2b5-119">S’applique à</span><span class="sxs-lookup"><span data-stu-id="1e2b5-119">Applies to</span></span>

[<span data-ttu-id="1e2b5-120">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="1e2b5-120">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

