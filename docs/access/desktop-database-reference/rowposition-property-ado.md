---
title: RowPosition, propriété (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f83d1b113b29be06ffded5263791d3db3068f7f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869070"
---
# <a name="rowposition-property-ado"></a><span data-ttu-id="a54ca-102">RowPosition, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="a54ca-102">RowPosition property (ADO)</span></span>


<span data-ttu-id="a54ca-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a54ca-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="a54ca-104">Récupère ou définit un objet **RowPosition** OLE DB à partir de/sur un objet **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="a54ca-104">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="a54ca-105">Lorsque vous utilisez **put\_RowPosition** pour définir l’objet **RowPosition** , l’objet **Recordset** résultant utilise l’objet **RowPosition** pour déterminer la ligne active.</span><span class="sxs-lookup"><span data-stu-id="a54ca-105">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="a54ca-106">Lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a54ca-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a54ca-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a54ca-107">Syntax</span></span>

<span data-ttu-id="a54ca-108">Get HRESULT\_RowPosition (\[out, retval\] IUnknown\* \* ppRowPos) ;</span><span class="sxs-lookup"><span data-stu-id="a54ca-108">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="a54ca-109">Placer HRESULT\_RowPosition (\[dans\] IUnknown\* pRowPos) ;</span><span class="sxs-lookup"><span data-stu-id="a54ca-109">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="a54ca-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a54ca-110">Parameters</span></span>

  - <span data-ttu-id="a54ca-111">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="a54ca-111">*ppRowPos*</span></span>

  - <span data-ttu-id="a54ca-112">Pointeur vers un objet **RowPosition** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a54ca-112">Pointer to an OLE DB **RowPosition** object.</span></span>

  - <span data-ttu-id="a54ca-113">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="a54ca-113">*PRowPos*</span></span>

  - <span data-ttu-id="a54ca-114">Objet **RowPosition** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a54ca-114">An OLE DB **RowPosition** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="a54ca-115">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="a54ca-115">Return values</span></span>

<span data-ttu-id="a54ca-116">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="a54ca-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a54ca-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="a54ca-117">Remarks</span></span>

<span data-ttu-id="a54ca-118">Lorsque cette propriété est définie, si l’objet **Rowset** de l’objet **RowPosition** est différent de l’objet **Rowset** de l’objet **Recordset** , le premier remplace ce dernier.</span><span class="sxs-lookup"><span data-stu-id="a54ca-118">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter.</span></span> <span data-ttu-id="a54ca-119">Le même comportement s’applique au **chapitre** actif à la **RowPosition** .</span><span class="sxs-lookup"><span data-stu-id="a54ca-119">The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a54ca-120">Champ d'application</span><span class="sxs-lookup"><span data-stu-id="a54ca-120">Applies To</span></span>

[<span data-ttu-id="a54ca-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="a54ca-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

