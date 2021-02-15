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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306740"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="9c7cc-102">Rowset, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="9c7cc-102">Rowset property (ADO)</span></span>

<span data-ttu-id="9c7cc-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9c7cc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9c7cc-104">Récupère ou définit un objet **Rowset** OLE DB sur un objet **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="9c7cc-105">Lorsque vous utilisez la mise en jeu de lignes, le jeu de \_ lignes est transformé en objet **Recordset** ADO.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="9c7cc-106">Lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c7cc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c7cc-107">Syntax</span></span>

<span data-ttu-id="9c7cc-108">HRESULT get \_ Rowset( \[ out, retval \] IUnknown \* \* ppRowset);</span><span class="sxs-lookup"><span data-stu-id="9c7cc-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="9c7cc-109">HRESULT put \_ Rowset( \[ in \] IUnknown \* pRowset);</span><span class="sxs-lookup"><span data-stu-id="9c7cc-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="9c7cc-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c7cc-110">Parameters</span></span>

|<span data-ttu-id="9c7cc-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="9c7cc-111">Parameter</span></span>|<span data-ttu-id="9c7cc-112">Description</span><span class="sxs-lookup"><span data-stu-id="9c7cc-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="9c7cc-113">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="9c7cc-113">*ppRowset*</span></span> |<span data-ttu-id="9c7cc-114">Pointeur vers un objet **Rowset** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-114">Pointer to an OLE DB **Rowset** object.</span></span>|
|<span data-ttu-id="9c7cc-115">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="9c7cc-115">*PRowset*</span></span> |<span data-ttu-id="9c7cc-116">Objet **Rowset** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-116">An OLE DB **Rowset** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="9c7cc-117">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="9c7cc-117">Return values</span></span>

<span data-ttu-id="9c7cc-118">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S \_ OK et E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="9c7cc-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="9c7cc-119">S’applique à</span><span class="sxs-lookup"><span data-stu-id="9c7cc-119">Applies to</span></span>

[<span data-ttu-id="9c7cc-120">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="9c7cc-120">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

