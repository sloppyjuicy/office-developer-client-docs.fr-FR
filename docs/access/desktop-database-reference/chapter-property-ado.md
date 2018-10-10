---
title: Chapter, propriété (ADO)
TOCTitle: Chapter Property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f02b20aef2b76ff00ce23b8597132dc22b414993
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471660"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="95e91-102">Chapter, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="95e91-102">Chapter Property (ADO)</span></span>


<span data-ttu-id="95e91-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="95e91-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="95e91-104">Extrait ou définit un objet **Chapter** OLE DB à partir de ou sur un objet **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="95e91-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="95e91-105">Lorsque vous utilisez **put\_chapitre** pour définir l’objet **Chapter** , un sous-ensemble de lignes est transformé en un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="95e91-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="95e91-106">Cette opération définit le chapitre actif de l'objet **Rowset**.</span><span class="sxs-lookup"><span data-stu-id="95e91-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="95e91-107">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="95e91-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e91-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95e91-108">Syntax</span></span>

<span data-ttu-id="95e91-109">Get HRESULT\_chapitre (\[out, retval\] long\* plChapter) ;</span><span class="sxs-lookup"><span data-stu-id="95e91-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="95e91-110">Placer HRESULT\_chapitre (\[dans\] lChapter long) ;</span><span class="sxs-lookup"><span data-stu-id="95e91-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="95e91-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95e91-111">Parameters</span></span>

  - <span data-ttu-id="95e91-112">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="95e91-112">*plChapter*</span></span>

  - <span data-ttu-id="95e91-113">Pointeur vers le descripteur d'un chapitre.</span><span class="sxs-lookup"><span data-stu-id="95e91-113">Pointer to the handle of a chapter.</span></span>

  - <span data-ttu-id="95e91-114">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="95e91-114">*LChapter*</span></span>

  - <span data-ttu-id="95e91-115">Descripteur d'un chapitre.</span><span class="sxs-lookup"><span data-stu-id="95e91-115">Handle of a chapter.</span></span>

## <a name="return-values"></a><span data-ttu-id="95e91-116">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="95e91-116">Return Values</span></span>

<span data-ttu-id="95e91-117">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="95e91-117">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="95e91-118">Champ d'application</span><span class="sxs-lookup"><span data-stu-id="95e91-118">Applies To</span></span>

[<span data-ttu-id="95e91-119">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="95e91-119">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

