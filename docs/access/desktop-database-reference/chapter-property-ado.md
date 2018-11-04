---
title: Chapter, propriété (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d7523a930feed7431bf8be0bbb7222a4b305483
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949396"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="1a3b1-102">Chapter, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="1a3b1-102">Chapter property (ADO)</span></span>

<span data-ttu-id="1a3b1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a3b1-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="1a3b1-104">Extrait ou définit un objet **Chapter** OLE DB à partir de ou sur un objet **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="1a3b1-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="1a3b1-105">Lorsque vous utilisez **put\_chapitre** pour définir l’objet **Chapter** , un sous-ensemble de lignes est transformé en un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="1a3b1-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="1a3b1-106">Cette opération définit le chapitre actif de l'objet **Rowset**.</span><span class="sxs-lookup"><span data-stu-id="1a3b1-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="1a3b1-107">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1a3b1-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a3b1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a3b1-108">Syntax</span></span>

<span data-ttu-id="1a3b1-109">Get HRESULT\_chapitre (\[out, retval\] long\* plChapter) ;</span><span class="sxs-lookup"><span data-stu-id="1a3b1-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="1a3b1-110">Placer HRESULT\_chapitre (\[dans\] lChapter long) ;</span><span class="sxs-lookup"><span data-stu-id="1a3b1-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="1a3b1-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a3b1-111">Parameters</span></span>

|<span data-ttu-id="1a3b1-112">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1a3b1-112">Parameter</span></span>|<span data-ttu-id="1a3b1-113">Description</span><span class="sxs-lookup"><span data-stu-id="1a3b1-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1a3b1-114">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="1a3b1-114">*plChapter*</span></span> |<span data-ttu-id="1a3b1-115">Pointeur vers le descripteur d'un chapitre.</span><span class="sxs-lookup"><span data-stu-id="1a3b1-115">Pointer to the handle of a chapter.</span></span>|
|<span data-ttu-id="1a3b1-116">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="1a3b1-116">*LChapter*</span></span> |<span data-ttu-id="1a3b1-117">Descripteur d'un chapitre.</span><span class="sxs-lookup"><span data-stu-id="1a3b1-117">Handle of a chapter.</span></span>|

## <a name="return-values"></a><span data-ttu-id="1a3b1-118">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="1a3b1-118">Return values</span></span>

<span data-ttu-id="1a3b1-119">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S\_OK et E\_ÉCHOUE.</span><span class="sxs-lookup"><span data-stu-id="1a3b1-119">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1a3b1-120">Champ d'application</span><span class="sxs-lookup"><span data-stu-id="1a3b1-120">Applies To</span></span>

[<span data-ttu-id="1a3b1-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="1a3b1-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

