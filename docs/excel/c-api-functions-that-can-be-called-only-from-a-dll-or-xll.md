---
title: Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- fonctions [excel 2007], api c appelée à partir de dll ou xll
localization_priority: Normal
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7935d86d1c0a460bcbec85157429d99242a73620
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782020"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a><span data-ttu-id="0d815-104">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="0d815-104">C API Functions That Can Be Called Only from a DLL or XLL</span></span>

<span data-ttu-id="0d815-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0d815-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0d815-106">L’API C fournit des fonctions de rappel de Microsoft Excel 15 qui peuvent être appelées uniquement à l’aide de la **Excel4**, **Excel4v**, **Excel12**ou fonctions **Excel12v** (ou une de ces fonctions indirectement en utilisant les fonctions Framework **Excel **ou **Excel12f**).</span><span class="sxs-lookup"><span data-stu-id="0d815-106">The C API provides 15 Microsoft Excel callback functions that can only be called by using the **Excel4**, **Excel4v**, **Excel12**, or **Excel12v** functions (or by one of these functions indirectly using the Framework functions **Excel** or **Excel12f**).</span></span> <span data-ttu-id="0d815-107">Cela signifie qu’ils ne peuvent être appelées à partir d’une DLL ou XLL.</span><span class="sxs-lookup"><span data-stu-id="0d815-107">This means they can only be called from a DLL or XLL.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="0d815-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="0d815-108">In this section</span></span>

[<span data-ttu-id="0d815-109">xlAbort</span><span class="sxs-lookup"><span data-stu-id="0d815-109">xlAbort</span></span>](xlabort.md)
  
[<span data-ttu-id="0d815-110">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="0d815-110">xlAsyncReturn</span></span>](xlasyncreturn.md)
  
[<span data-ttu-id="0d815-111">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="0d815-111">xlCoerce</span></span>](xlcoerce.md)
  
[<span data-ttu-id="0d815-112">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="0d815-112">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
  
[<span data-ttu-id="0d815-113">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="0d815-113">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md)
  
[<span data-ttu-id="0d815-114">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="0d815-114">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md)
  
[<span data-ttu-id="0d815-115">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="0d815-115">xlEventRegister</span></span>](xleventregister.md)
  
[<span data-ttu-id="0d815-116">xlFree</span><span class="sxs-lookup"><span data-stu-id="0d815-116">xlFree</span></span>](xlfree.md)
  
[<span data-ttu-id="0d815-117">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="0d815-117">xlGetBinaryName</span></span>](xlgetbinaryname.md)
  
[<span data-ttu-id="0d815-118">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="0d815-118">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="0d815-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="0d815-119">xlGetInst</span></span>](xlgetinst.md)
  
[<span data-ttu-id="0d815-120">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="0d815-120">xlGetInstPtr</span></span>](xlgetinstptr.md)
  
[<span data-ttu-id="0d815-121">xlGetName</span><span class="sxs-lookup"><span data-stu-id="0d815-121">xlGetName</span></span>](xlgetname.md)
  
[<span data-ttu-id="0d815-122">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="0d815-122">xlRunningOnCluster</span></span>](xlrunningoncluster.md)
  
[<span data-ttu-id="0d815-123">xlSet</span><span class="sxs-lookup"><span data-stu-id="0d815-123">xlSet</span></span>](xlset.md)
  
[<span data-ttu-id="0d815-124">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="0d815-124">xlSheetId</span></span>](xlsheetid.md)
  
[<span data-ttu-id="0d815-125">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="0d815-125">xlSheetNm</span></span>](xlsheetnm.md)
  
[<span data-ttu-id="0d815-126">xlStack</span><span class="sxs-lookup"><span data-stu-id="0d815-126">xlStack</span></span>](xlstack.md)
  
[<span data-ttu-id="0d815-127">xlUDF</span><span class="sxs-lookup"><span data-stu-id="0d815-127">xlUDF</span></span>](xludf.md)
  
## <a name="see-also"></a><span data-ttu-id="0d815-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d815-128">See also</span></span>



[<span data-ttu-id="0d815-129">Les fonctions de rappel de l'API C Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="0d815-129">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)

