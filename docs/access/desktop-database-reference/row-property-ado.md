---
title: Row, propriété - ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7578a00719946450e840080c21284784a27be170
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870946"
---
# <a name="row-property-ado"></a><span data-ttu-id="4b86c-102">Row, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="4b86c-102">Row property (ADO)</span></span>


<span data-ttu-id="4b86c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b86c-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="4b86c-104">Extrait ou définit un objet **Row** OLE DB à partir de ou sur un objet **ADORecordConstruction**.</span><span class="sxs-lookup"><span data-stu-id="4b86c-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="4b86c-105">Lorsque vous utilisez **put\_ligne** pour définir un objet **Row** , une ligne est transformée en objet ADO **Record** .</span><span class="sxs-lookup"><span data-stu-id="4b86c-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="4b86c-106">Lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4b86c-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b86c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b86c-107">Syntax</span></span>

<span data-ttu-id="4b86c-108">Get HRESULT\_ligne (\[out, retval\] IUnknown\* \* ppRow) ;</span><span class="sxs-lookup"><span data-stu-id="4b86c-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="4b86c-109">Placer HRESULT\_ligne (\[dans\] IUnknown\* pRow) ;</span><span class="sxs-lookup"><span data-stu-id="4b86c-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="4b86c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b86c-110">Parameters</span></span>

  - <span data-ttu-id="4b86c-111">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="4b86c-111">*ppRow*</span></span>

  - <span data-ttu-id="4b86c-112">Pointeur vers un objet **Row** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="4b86c-112">Pointer to an OLE DB **Row** object.</span></span>

  - <span data-ttu-id="4b86c-113">*PRow*</span><span class="sxs-lookup"><span data-stu-id="4b86c-113">*PRow*</span></span>

  - <span data-ttu-id="4b86c-114">Objet **Row** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="4b86c-114">An OLE DB **Row** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="4b86c-115">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="4b86c-115">Return values</span></span>

<span data-ttu-id="4b86c-116">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="4b86c-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="4b86c-117">Champ d'application</span><span class="sxs-lookup"><span data-stu-id="4b86c-117">Applies To</span></span>

[<span data-ttu-id="4b86c-118">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="4b86c-118">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

