---
title: RowPosition, propriété (ADO)
TOCTitle: RowPosition Property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a4512157e70f4f5a7533e2a480dd96aa3693741
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469965"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="9ed64-102">RowPosition, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="9ed64-102">RowPosition Property (ADO)</span></span>


<span data-ttu-id="9ed64-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ed64-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="9ed64-104">Récupère ou définit un objet **RowPosition** OLE DB à partir de/sur un objet **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="9ed64-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="9ed64-105">Lorsque vous utilisez **put\_RowPosition** pour définir l’objet **RowPosition** , l’objet **Recordset** résultant utilise l’objet **RowPosition** pour déterminer la ligne active.</span><span class="sxs-lookup"><span data-stu-id="9ed64-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="9ed64-106">Lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9ed64-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ed64-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ed64-107">Syntax</span></span>

<span data-ttu-id="9ed64-108">Get HRESULT\_RowPosition (\[out, retval\] IUnknown\* \* ppRowPos) ;</span><span class="sxs-lookup"><span data-stu-id="9ed64-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="9ed64-109">Placer HRESULT\_RowPosition (\[dans\] IUnknown\* pRowPos) ;</span><span class="sxs-lookup"><span data-stu-id="9ed64-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="9ed64-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ed64-110">Parameters</span></span>

  - <span data-ttu-id="9ed64-111">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="9ed64-111">*ppRowPos*</span></span>

  - <span data-ttu-id="9ed64-112">Pointeur vers un objet **RowPosition** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="9ed64-112">Pointer to an OLE DB **RowPosition** object.</span></span>

  - <span data-ttu-id="9ed64-113">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="9ed64-113">*PRowPos*</span></span>

  - <span data-ttu-id="9ed64-114">Objet **RowPosition** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="9ed64-114">An OLE DB **RowPosition** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="9ed64-115">Valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="9ed64-115">Return Values</span></span>

<span data-ttu-id="9ed64-116">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="9ed64-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ed64-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="9ed64-117">Remarks</span></span>

<span data-ttu-id="9ed64-118">Lorsque cette propriété est définie, si l’objet **Rowset** de l’objet **RowPosition** est différent de l’objet **Rowset** de l’objet **Recordset** , le premier remplace ce dernier.</span><span class="sxs-lookup"><span data-stu-id="9ed64-118">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter.</span></span> <span data-ttu-id="9ed64-119">Le même comportement s’applique au **chapitre** actif à la **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="9ed64-119">The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="9ed64-120">Champ d'application</span><span class="sxs-lookup"><span data-stu-id="9ed64-120">Applies To</span></span>

[<span data-ttu-id="9ed64-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="9ed64-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

