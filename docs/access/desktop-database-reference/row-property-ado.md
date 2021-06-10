---
title: Row, propriété - ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306481"
---
# <a name="row-property-ado"></a><span data-ttu-id="37ded-102">Row, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="37ded-102">Row property (ADO)</span></span>

<span data-ttu-id="37ded-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="37ded-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37ded-104">Extrait ou définit un objet **Row** OLE DB à partir de ou sur un objet **ADORecordConstruction**.</span><span class="sxs-lookup"><span data-stu-id="37ded-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="37ded-105">Lorsque vous utilisez **put \_ Row** pour définir un objet **Row,** une ligne est transformée en objet **Record** ADO.</span><span class="sxs-lookup"><span data-stu-id="37ded-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="37ded-106">Lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="37ded-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ded-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37ded-107">Syntax</span></span>

<span data-ttu-id="37ded-108">HRESULT get \_ Row( \[ out, retval \] IUnknown \* \* ppRow);</span><span class="sxs-lookup"><span data-stu-id="37ded-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="37ded-109">HRESULT put \_ Row( \[ in \] IUnknown \* pRow);</span><span class="sxs-lookup"><span data-stu-id="37ded-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="37ded-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37ded-110">Parameters</span></span>

|<span data-ttu-id="37ded-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="37ded-111">Parameter</span></span>|<span data-ttu-id="37ded-112">Description</span><span class="sxs-lookup"><span data-stu-id="37ded-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="37ded-113">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="37ded-113">*ppRow*</span></span> |<span data-ttu-id="37ded-114">Pointeur vers un objet **Row** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="37ded-114">Pointer to an OLE DB **Row** object.</span></span>|
|<span data-ttu-id="37ded-115">*PRow*</span><span class="sxs-lookup"><span data-stu-id="37ded-115">*PRow*</span></span> |<span data-ttu-id="37ded-116">Objet **Row** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="37ded-116">An OLE DB **Row** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="37ded-117">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="37ded-117">Return values</span></span>

<span data-ttu-id="37ded-118">Cette méthode de propriété renvoie les valeurs HRESULT standard, y compris S \_ OK et E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="37ded-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="37ded-119">S’applique à</span><span class="sxs-lookup"><span data-stu-id="37ded-119">Applies to</span></span>

[<span data-ttu-id="37ded-120">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="37ded-120">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

