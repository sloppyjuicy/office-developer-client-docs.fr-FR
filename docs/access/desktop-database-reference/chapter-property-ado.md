---
title: Chapter, propriété (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4f4efc2ffab9f7996b2d805658b985badbaf87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296394"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="85f62-102">Chapter, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="85f62-102">Chapter property (ADO)</span></span>

<span data-ttu-id="85f62-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85f62-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="85f62-104">Extrait ou définit un objet **Chapter** OLE DB à partir de ou sur un objet **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="85f62-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="85f62-105">Lorsque vous utilisez **la section \_ « Chapter** » pour définir l’objet **Chapter,** un sous-ensemble de lignes est transformé en objet **Recordset** ADO.</span><span class="sxs-lookup"><span data-stu-id="85f62-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="85f62-106">Cette opération définit le chapitre actif de l'objet **Rowset**.</span><span class="sxs-lookup"><span data-stu-id="85f62-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="85f62-107">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="85f62-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="85f62-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85f62-108">Syntax</span></span>

<span data-ttu-id="85f62-109">HRESULT get \_ Chapter( \[ out, retval \] long \* plChapter);</span><span class="sxs-lookup"><span data-stu-id="85f62-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="85f62-110">HRESULT put \_ Chapter( \[ in long \] lChapter);</span><span class="sxs-lookup"><span data-stu-id="85f62-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="85f62-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85f62-111">Parameters</span></span>

|<span data-ttu-id="85f62-112">Paramètre</span><span class="sxs-lookup"><span data-stu-id="85f62-112">Parameter</span></span>|<span data-ttu-id="85f62-113">Description</span><span class="sxs-lookup"><span data-stu-id="85f62-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="85f62-114">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="85f62-114">*plChapter*</span></span> |<span data-ttu-id="85f62-115">Pointeur vers le descripteur d'un chapitre.</span><span class="sxs-lookup"><span data-stu-id="85f62-115">Pointer to the handle of a chapter.</span></span>|
|<span data-ttu-id="85f62-116">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="85f62-116">*LChapter*</span></span> |<span data-ttu-id="85f62-117">Descripteur d'un chapitre.</span><span class="sxs-lookup"><span data-stu-id="85f62-117">Handle of a chapter.</span></span>|

## <a name="return-values"></a><span data-ttu-id="85f62-118">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="85f62-118">Return values</span></span>

<span data-ttu-id="85f62-119">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S \_ OK et E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="85f62-119">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="85f62-120">Champ d'application</span><span class="sxs-lookup"><span data-stu-id="85f62-120">Applies To</span></span>

[<span data-ttu-id="85f62-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="85f62-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

