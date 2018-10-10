---
title: Row, propriété - ActiveX Data Objects (ADO)
TOCTitle: Row Property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 05d97bb411c4199677f512d9412653ca5a4b4fe1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470516"
---
# <a name="row-property-ado"></a><span data-ttu-id="909e1-102">Row, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="909e1-102">Row Property (ADO)</span></span>


<span data-ttu-id="909e1-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="909e1-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="909e1-104">Extrait ou définit un objet **Row** OLE DB à partir de ou sur un objet **ADORecordConstruction**.</span><span class="sxs-lookup"><span data-stu-id="909e1-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="909e1-105">Lorsque vous utilisez **put\_ligne** pour définir un objet **Row** , une ligne est transformée en objet ADO **Record** .</span><span class="sxs-lookup"><span data-stu-id="909e1-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="909e1-106">Lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="909e1-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="909e1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="909e1-107">Syntax</span></span>

<span data-ttu-id="909e1-108">Get HRESULT\_ligne (\[out, retval\] IUnknown\* \* ppRow) ;</span><span class="sxs-lookup"><span data-stu-id="909e1-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="909e1-109">Placer HRESULT\_ligne (\[dans\] IUnknown\* pRow) ;</span><span class="sxs-lookup"><span data-stu-id="909e1-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="909e1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="909e1-110">Parameters</span></span>

  - <span data-ttu-id="909e1-111">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="909e1-111">*ppRow*</span></span>

  - <span data-ttu-id="909e1-112">Pointeur vers un objet **Row** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="909e1-112">Pointer to an OLE DB **Row** object.</span></span>

  - <span data-ttu-id="909e1-113">*PRow*</span><span class="sxs-lookup"><span data-stu-id="909e1-113">*PRow*</span></span>

  - <span data-ttu-id="909e1-114">Objet **Row** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="909e1-114">An OLE DB **Row** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="909e1-115">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="909e1-115">Return Values</span></span>

<span data-ttu-id="909e1-116">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="909e1-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="909e1-117">Champ d'application</span><span class="sxs-lookup"><span data-stu-id="909e1-117">Applies To</span></span>

[<span data-ttu-id="909e1-118">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="909e1-118">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

