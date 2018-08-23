---
title: HrAddColumnsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrAddColumnsEx
api_type:
- COM
ms.assetid: c0a65d2b-a9b8-4477-a1c7-18c8478126f6
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 566a9d23c46ec717eb5eed711fff801b15d49fc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564233"
---
# <a name="hraddcolumnsex"></a><span data-ttu-id="54ee7-103">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="54ee7-103">HrAddColumnsEx</span></span>

  
  
<span data-ttu-id="54ee7-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54ee7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54ee7-105">Ajoute ou déplacer des colonnes au début d’une table existante.</span><span class="sxs-lookup"><span data-stu-id="54ee7-105">Adds or moves columns to the beginning of an existing table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54ee7-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="54ee7-106">Header file:</span></span>  <br/> |<span data-ttu-id="54ee7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="54ee7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="54ee7-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="54ee7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="54ee7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="54ee7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="54ee7-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="54ee7-110">Called by:</span></span>  <br/> |<span data-ttu-id="54ee7-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="54ee7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumnsEx(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  void (FAR * lpfnFilterColumns)(
  LPSPropTagArray ptaga)
);
```

## <a name="parameters"></a><span data-ttu-id="54ee7-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54ee7-112">Parameters</span></span>

 <span data-ttu-id="54ee7-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="54ee7-113">_lptbl_</span></span>
  
> <span data-ttu-id="54ee7-114">[in] Pointeur vers le tableau MAPI affecté.</span><span class="sxs-lookup"><span data-stu-id="54ee7-114">[in] Pointer to the MAPI table affected.</span></span> 
    
 <span data-ttu-id="54ee7-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="54ee7-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="54ee7-116">[in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété pour les propriétés à ajouter ou déplacées vers le début de la table.</span><span class="sxs-lookup"><span data-stu-id="54ee7-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="54ee7-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="54ee7-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="54ee7-118">[in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="54ee7-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="54ee7-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="54ee7-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="54ee7-120">[in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="54ee7-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="54ee7-121">_lpfnFilterColumns_</span><span class="sxs-lookup"><span data-stu-id="54ee7-121">_lpfnFilterColumns_</span></span>
  
> <span data-ttu-id="54ee7-122">[in] Pointeur vers une fonction de rappel fournie par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="54ee7-122">[in] Pointer to a callback function furnished by the caller.</span></span> <span data-ttu-id="54ee7-123">Si le paramètre _lpfnFilterColumns_ est défini sur NULL, aucun rappel n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="54ee7-123">If the  _lpfnFilterColumns_ parameter is set to NULL, no callback is made.</span></span> 
    
 <span data-ttu-id="54ee7-124">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="54ee7-124">_ptaga_</span></span>
  
> <span data-ttu-id="54ee7-125">[in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient le tableau des balises de propriété existant déjà dans la table avant de propriétés sont ajoutées ou déplacées vers le début.</span><span class="sxs-lookup"><span data-stu-id="54ee7-125">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the array of property tags already existing in the table before properties are added or moved to the beginning.</span></span> <span data-ttu-id="54ee7-126">Passe **HrAddColumnsEx** ce pointeur en tant que paramètre à la fonction de rappel désigné par _lpfnFilterColumns_.</span><span class="sxs-lookup"><span data-stu-id="54ee7-126">**HrAddColumnsEx** passes this pointer as the parameter to the callback function pointed to by  _lpfnFilterColumns_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="54ee7-127">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="54ee7-127">Return value</span></span>

<span data-ttu-id="54ee7-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="54ee7-128">S_OK</span></span> 
  
> <span data-ttu-id="54ee7-129">L’appel a réussi et les colonnes spécifiées ont été déplacés ou ajoutés.</span><span class="sxs-lookup"><span data-stu-id="54ee7-129">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="54ee7-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="54ee7-130">Remarks</span></span>

<span data-ttu-id="54ee7-131">Les propriétés transmises à **HrAddColumnsEx** en utilisant le paramètre _lpproptagColumnsNew_ deviennent les propriétés de premières exposées sur les appels suivants à la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="54ee7-131">The properties passed to **HrAddColumnsEx** using the  _lpproptagColumnsNew_ parameter become the first properties exposed on subsequent calls to the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="54ee7-132">Toutes les propriétés précédemment dans le tableau qui n’est pas spécifiées dans le paramètre _lpproptagColumnsNew_ sont exposées après toutes les propriétés ajoutées et déplacées.</span><span class="sxs-lookup"><span data-stu-id="54ee7-132">Any properties previously in the table that were not specified in the  _lpproptagColumnsNew_ parameter are exposed after all the added and moved properties.</span></span> 
  
<span data-ttu-id="54ee7-133">Si les propriétés du tableau ne sont pas définies lorsque **QueryRows** est appelée, ils sont retournées avec le type de la propriété PT_NULL et l’identificateur de la propriété PROP_ID_NULL.</span><span class="sxs-lookup"><span data-stu-id="54ee7-133">If any table properties are undefined when **QueryRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="54ee7-134">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="54ee7-134">Notes to callers</span></span>

<span data-ttu-id="54ee7-135">La fonction **HrAddColumnsEx** permet à l’appelant de fournir une fonction de rappel pour filtrer les colonnes qui étaient déjà dans le tableau, par exemple pour convertir des chaînes en type de propriété PT_UNICODE PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="54ee7-135">The **HrAddColumnsEx** function allows the caller to furnish a callback function to filter the columns that were already in the table, for example to convert strings from property type PT_UNICODE to PT_STRING8.</span></span> <span data-ttu-id="54ee7-136">**HrAddColumnsEx** passe un pointeur vers la colonne existaient précédemment défini en tant que paramètre à la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="54ee7-136">**HrAddColumnsEx** passes a pointer to the previously existing column set as the parameter to the callback function.</span></span> <span data-ttu-id="54ee7-137">La fonction de rappel peut modifier des données dans le tableau de la propriété tag, mais ne peut pas ajouter de nouvelles balises.</span><span class="sxs-lookup"><span data-stu-id="54ee7-137">The callback function can change data in the property tag array but cannot add new tags.</span></span> 
  
 <span data-ttu-id="54ee7-138">**HrAddColumnsEx** appelle d’abord la fonction de rappel s’il est fourni, puis ajoute ou déplace les colonnes spécifiées et enfin appelle [IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="54ee7-138">**HrAddColumnsEx** first calls the callback function if one is furnished, then adds or moves the specified columns, and finally calls [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> 
  
<span data-ttu-id="54ee7-139">Les paramètres d’entrée _lpAllocateBuffer_ et _lpFreeBuffer_ pointent vers les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIFreeBuffer](mapifreebuffer.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="54ee7-139">The  _lpAllocateBuffer_ and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="54ee7-140">Les valeurs exactes des pointeurs transmis à **HrAddColumnsEx** dépendent si l’appelant est une application cliente ou un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="54ee7-140">The exact values of the pointers passed to **HrAddColumnsEx** depend on whether the caller is a client application or a service provider.</span></span> <span data-ttu-id="54ee7-141">Un client transmet des pointeurs vers les fonctions MAPI portant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="54ee7-141">A client passes pointers to the MAPI functions with the specified names.</span></span> <span data-ttu-id="54ee7-142">Un fournisseur de services transmet les pointeurs qu’elle reçue dans son appel d’initialisation ou récupéré en appelant la méthode [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="54ee7-142">A service provider passes the pointers it received in its initialization call or retrieved by calling the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54ee7-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54ee7-143">See also</span></span>



[<span data-ttu-id="54ee7-144">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="54ee7-144">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)

