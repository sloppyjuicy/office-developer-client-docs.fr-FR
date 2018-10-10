---
title: WillChangeField et FieldChangeComplete, événements (ADO)
TOCTitle: WillChangeField and FieldChangeComplete Events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 40e9572988ca3335ef93ecf46d00a716ba29c595
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471276"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a><span data-ttu-id="a159d-102">WillChangeField et FieldChangeComplete, événements (ADO)</span><span class="sxs-lookup"><span data-stu-id="a159d-102">WillChangeField and FieldChangeComplete Events (ADO)</span></span>


<span data-ttu-id="a159d-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a159d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a159d-p101">L'événement **WillChangeField** est appelé avant qu'une opération en attente modifie la valeur d'objets [Field](field-object-ado.md) dans l'objet [Recordset](recordset-object-ado.md). Quant à l'événement **FieldChangeComplete**, il est appelé après la modification de la valeur d'un ou plusieurs objets **Field**.</span><span class="sxs-lookup"><span data-stu-id="a159d-p101">The **WillChangeField** event is called before a pending operation changes the value of one or more [Field](field-object-ado.md) objects in the [Recordset](recordset-object-ado.md). The **FieldChangeComplete** event is called after the value of one or more **Field** objects has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a159d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a159d-106">Syntax</span></span>

<span data-ttu-id="a159d-107">WillChangeField*cFields*, *champs*, *adStatus*, *Connection*</span><span class="sxs-lookup"><span data-stu-id="a159d-107">WillChangeField*cFields*, *Fields*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="a159d-108">FieldChangeComplete*cFields*, *champs*, *pError*, *adStatus*, *Connection*</span><span class="sxs-lookup"><span data-stu-id="a159d-108">FieldChangeComplete*cFields*, *Fields*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="a159d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a159d-109">Parameters</span></span>

  - <span data-ttu-id="a159d-110">*cFields*</span><span class="sxs-lookup"><span data-stu-id="a159d-110">*cFields*</span></span>

  - <span data-ttu-id="a159d-111">Valeur de type **Long** indiquant le nombre d'objets **Field** inclus dans *Fields*.</span><span class="sxs-lookup"><span data-stu-id="a159d-111">A **Long** that indicates the number of **Field** objects in *Fields*.</span></span>

  - <span data-ttu-id="a159d-112">Collection *Fields*</span><span class="sxs-lookup"><span data-stu-id="a159d-112">*Fields*</span></span>

  - <span data-ttu-id="a159d-113">Pour **WillChangeField**, le paramètre *Fields* est un tableau de **variantes** qui contient des objets **Field** avec les valeurs d’origine.</span><span class="sxs-lookup"><span data-stu-id="a159d-113">For **WillChangeField**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the original values.</span></span>  
      
    <span data-ttu-id="a159d-114">Pour **FieldChangeComplete**, le paramètre *Fields* est un tableau de **variantes** qui contient des objets **Field** avec les valeurs modifiées.</span><span class="sxs-lookup"><span data-stu-id="a159d-114">For **FieldChangeComplete**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the changed values.</span></span>

  - <span data-ttu-id="a159d-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="a159d-115">*pError*</span></span>

  - <span data-ttu-id="a159d-p102">Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si *adStatus* a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="a159d-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="a159d-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="a159d-118">*adStatus*</span></span>

  - [<span data-ttu-id="a159d-119">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="a159d-119">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="a159d-p103">Lorsque **WillChangeField** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement. Il est défini à **adStatusCantDeny** si cet événement ne peut pas demander l'annulation de l'opération en attente.</span><span class="sxs-lookup"><span data-stu-id="a159d-p103">When **WillChangeField** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="a159d-122">Lorsque **FieldChangeComplete** est appelé, ce paramètre a la valeur **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement ou **adStatusErrorsOccurred** si cette dernière a échoué.</span><span class="sxs-lookup"><span data-stu-id="a159d-122">When **FieldChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span>
    
    <span data-ttu-id="a159d-123">Avant que **WillChangeField** ne soit retourné, affectez la valeur **adStatusCancel** à ce paramètre pour demander l'annulation de l'opération en attente.</span><span class="sxs-lookup"><span data-stu-id="a159d-123">Before **WillChangeField** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="a159d-124">Avant que **FieldChangeComplete** ne soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre afin d'empêcher toute notification ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a159d-124">Before **FieldChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="a159d-125">*Connection*</span><span class="sxs-lookup"><span data-stu-id="a159d-125">*pRecordset*</span></span>

  - <span data-ttu-id="a159d-126">Objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="a159d-126">A **Recordset** object.</span></span> <span data-ttu-id="a159d-127">Le **jeu d’enregistrements** pour laquelle cet événement se produit.</span><span class="sxs-lookup"><span data-stu-id="a159d-127">The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="a159d-128">Notes</span><span class="sxs-lookup"><span data-stu-id="a159d-128">Remarks</span></span>

<span data-ttu-id="a159d-129">Un événement **WillChangeField** ou **FieldChangeComplete** est parfois généré lorsque vous définissez la propriété [Value](value-property-ado.md) et que vous appelez la méthode [Update](update-method-ado.md) à l'aide des paramètres de tableau de champs et de valeurs.</span><span class="sxs-lookup"><span data-stu-id="a159d-129">A **WillChangeField** or **FieldChangeComplete** event may occur when setting the [Value](value-property-ado.md) property and calling the [Update](update-method-ado.md) method with field and value array parameters.</span></span>

