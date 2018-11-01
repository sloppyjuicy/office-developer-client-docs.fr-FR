---
title: Chapter, propriété (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5eeb3c6e2e8c7b7f1c0f6e733c1b86545a5e954f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887823"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="4c25d-102">Chapter, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="4c25d-102">Chapter property (ADO)</span></span>


<span data-ttu-id="4c25d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c25d-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="4c25d-104">Extrait ou définit un objet **Chapter** OLE DB à partir de ou sur un objet **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="4c25d-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="4c25d-105">Lorsque vous utilisez **put\_chapitre** pour définir l’objet **Chapter** , un sous-ensemble de lignes est transformé en un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="4c25d-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="4c25d-106">Cette opération définit le chapitre actif de l'objet **Rowset**.</span><span class="sxs-lookup"><span data-stu-id="4c25d-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="4c25d-107">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4c25d-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c25d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c25d-108">Syntax</span></span>

<span data-ttu-id="4c25d-109">Get HRESULT\_chapitre (\[out, retval\] long\* plChapter) ;</span><span class="sxs-lookup"><span data-stu-id="4c25d-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="4c25d-110">Placer HRESULT\_chapitre (\[dans\] lChapter long) ;</span><span class="sxs-lookup"><span data-stu-id="4c25d-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="4c25d-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c25d-111">Parameters</span></span>

  - <span data-ttu-id="4c25d-112">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="4c25d-112">*plChapter*</span></span>

  - <span data-ttu-id="4c25d-113">Pointeur vers le descripteur d'un chapitre.</span><span class="sxs-lookup"><span data-stu-id="4c25d-113">Pointer to the handle of a chapter.</span></span>

  - <span data-ttu-id="4c25d-114">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="4c25d-114">*LChapter*</span></span>

  - <span data-ttu-id="4c25d-115">Descripteur d'un chapitre.</span><span class="sxs-lookup"><span data-stu-id="4c25d-115">Handle of a chapter.</span></span>

## <a name="return-values"></a><span data-ttu-id="4c25d-116">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="4c25d-116">Return values</span></span>

<span data-ttu-id="4c25d-117">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="4c25d-117">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="4c25d-118">Champ d'application</span><span class="sxs-lookup"><span data-stu-id="4c25d-118">Applies To</span></span>

[<span data-ttu-id="4c25d-119">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="4c25d-119">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

