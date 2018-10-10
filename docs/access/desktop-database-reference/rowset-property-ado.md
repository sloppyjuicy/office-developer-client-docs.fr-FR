---
title: Rowset, propriété (ADO)
TOCTitle: Rowset Property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95a33fb3d24e5cdbf608d268781be0dd536fa315
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470798"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="31c45-102">Rowset, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="31c45-102">Rowset Property (ADO)</span></span>


<span data-ttu-id="31c45-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="31c45-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="31c45-104">Récupère ou définit un objet **Rowset** OLE DB sur un objet **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="31c45-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="31c45-105">Lorsque vous utilisez put\_Rowset, l’ensemble de lignes est transformé en un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="31c45-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="31c45-106">Lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="31c45-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="31c45-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31c45-107">Syntax</span></span>

<span data-ttu-id="31c45-108">Get HRESULT\_Rowset (\[out, retval\] IUnknown\* \* ppRowset) ;</span><span class="sxs-lookup"><span data-stu-id="31c45-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="31c45-109">Placer HRESULT\_Rowset (\[dans\] IUnknown\* pRowset) ;</span><span class="sxs-lookup"><span data-stu-id="31c45-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="31c45-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31c45-110">Parameters</span></span>

  - <span data-ttu-id="31c45-111">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="31c45-111">*ppRowset*</span></span>

  - <span data-ttu-id="31c45-112">Pointeur vers un objet **Rowset** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="31c45-112">Pointer to an OLE DB **Rowset** object.</span></span>

  - <span data-ttu-id="31c45-113">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="31c45-113">*PRowset*</span></span>

  - <span data-ttu-id="31c45-114">Objet **Rowset** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="31c45-114">An OLE DB **Rowset** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="31c45-115">Valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="31c45-115">Return Values</span></span>

<span data-ttu-id="31c45-116">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="31c45-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="31c45-117">Champ d'application</span><span class="sxs-lookup"><span data-stu-id="31c45-117">Applies To</span></span>

[<span data-ttu-id="31c45-118">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="31c45-118">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

