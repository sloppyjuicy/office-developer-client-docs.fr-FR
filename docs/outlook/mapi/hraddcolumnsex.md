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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9ca34fb2cce6e86c42e8e9525cd213f1008997d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427478"
---
# <a name="hraddcolumnsex"></a><span data-ttu-id="461dd-103">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="461dd-103">HrAddColumnsEx</span></span>

  
  
<span data-ttu-id="461dd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="461dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="461dd-105">Ajoute ou déplace des colonnes au début d’un tableau existant.</span><span class="sxs-lookup"><span data-stu-id="461dd-105">Adds or moves columns to the beginning of an existing table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="461dd-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="461dd-106">Header file:</span></span>  <br/> |<span data-ttu-id="461dd-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="461dd-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="461dd-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="461dd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="461dd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="461dd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="461dd-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="461dd-110">Called by:</span></span>  <br/> |<span data-ttu-id="461dd-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="461dd-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="461dd-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="461dd-112">Parameters</span></span>

 <span data-ttu-id="461dd-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="461dd-113">_lptbl_</span></span>
  
> <span data-ttu-id="461dd-114">[in] Pointeur vers la table MAPI affectée.</span><span class="sxs-lookup"><span data-stu-id="461dd-114">[in] Pointer to the MAPI table affected.</span></span> 
    
 <span data-ttu-id="461dd-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="461dd-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="461dd-116">[in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriétés pour les propriétés à ajouter ou déplacer au début du tableau.</span><span class="sxs-lookup"><span data-stu-id="461dd-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="461dd-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="461dd-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="461dd-118">[in] Pointeur vers la [fonction MAPIAllocateBuffer,](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="461dd-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="461dd-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="461dd-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="461dd-120">[in] Pointeur vers la [fonction MAPIFreeBuffer,](mapifreebuffer.md) à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="461dd-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="461dd-121">_lpfnFilterColumns_</span><span class="sxs-lookup"><span data-stu-id="461dd-121">_lpfnFilterColumns_</span></span>
  
> <span data-ttu-id="461dd-122">[in] Pointeur vers une fonction de rappel fournie par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="461dd-122">[in] Pointer to a callback function furnished by the caller.</span></span> <span data-ttu-id="461dd-123">Si le  _paramètre lpfnFilterColumns est_ définie sur NULL, aucun rappel n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="461dd-123">If the  _lpfnFilterColumns_ parameter is set to NULL, no callback is made.</span></span> 
    
 <span data-ttu-id="461dd-124">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="461dd-124">_ptaga_</span></span>
  
> <span data-ttu-id="461dd-125">[in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient le tableau des balises de propriétés qui existent déjà dans le tableau avant que les propriétés ne soient ajoutées ou déplacées au début.</span><span class="sxs-lookup"><span data-stu-id="461dd-125">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the array of property tags already existing in the table before properties are added or moved to the beginning.</span></span> <span data-ttu-id="461dd-126">**HrAddColumnsEx** passe ce pointeur comme paramètre à la fonction de rappel pointée par  _lpfnFilterColumns_.</span><span class="sxs-lookup"><span data-stu-id="461dd-126">**HrAddColumnsEx** passes this pointer as the parameter to the callback function pointed to by  _lpfnFilterColumns_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="461dd-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="461dd-127">Return value</span></span>

<span data-ttu-id="461dd-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="461dd-128">S_OK</span></span> 
  
> <span data-ttu-id="461dd-129">L’appel a réussi et les colonnes spécifiées ont été déplacées ou ajoutées.</span><span class="sxs-lookup"><span data-stu-id="461dd-129">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="461dd-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="461dd-130">Remarks</span></span>

<span data-ttu-id="461dd-131">Les propriétés transmises à **HrAddColumnsEx** à l’aide du paramètre _lpproptagColumnsNew_ deviennent les premières propriétés exposées lors des appels ultérieurs à la méthode [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="461dd-131">The properties passed to **HrAddColumnsEx** using the  _lpproptagColumnsNew_ parameter become the first properties exposed on subsequent calls to the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="461dd-132">Toutes les propriétés précédemment dans le tableau qui n’ont pas été spécifiées dans le  _paramètre lpproptagColumnsNew_ sont exposées après toutes les propriétés ajoutées et déplacées.</span><span class="sxs-lookup"><span data-stu-id="461dd-132">Any properties previously in the table that were not specified in the  _lpproptagColumnsNew_ parameter are exposed after all the added and moved properties.</span></span> 
  
<span data-ttu-id="461dd-133">Si des propriétés de table ne sont pas définies lors de l’appel de **QueryRows,** elles sont renvoyées avec le type de propriété PT_NULL et l’identificateur de PROP_ID_NULL.</span><span class="sxs-lookup"><span data-stu-id="461dd-133">If any table properties are undefined when **QueryRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="461dd-134">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="461dd-134">Notes to callers</span></span>

<span data-ttu-id="461dd-135">La fonction **HrAddColumnsEx** permet à l’appelant de fournir une fonction de rappel pour filtrer les colonnes déjà dans le tableau, par exemple pour convertir des chaînes du type de propriété PT_UNICODE en PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="461dd-135">The **HrAddColumnsEx** function allows the caller to furnish a callback function to filter the columns that were already in the table, for example to convert strings from property type PT_UNICODE to PT_STRING8.</span></span> <span data-ttu-id="461dd-136">**HrAddColumnsEx** passe un pointeur vers le jeu de colonnes existant précédemment en tant que paramètre de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="461dd-136">**HrAddColumnsEx** passes a pointer to the previously existing column set as the parameter to the callback function.</span></span> <span data-ttu-id="461dd-137">La fonction de rappel peut modifier les données dans le tableau de balises de propriétés, mais ne peut pas ajouter de nouvelles balises.</span><span class="sxs-lookup"><span data-stu-id="461dd-137">The callback function can change data in the property tag array but cannot add new tags.</span></span> 
  
 <span data-ttu-id="461dd-138">**HrAddColumnsEx** appelle d’abord la fonction de rappel s’il en existe une, ajoute ou déplace les colonnes spécifiées, puis appelle [IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="461dd-138">**HrAddColumnsEx** first calls the callback function if one is furnished, then adds or moves the specified columns, and finally calls [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> 
  
<span data-ttu-id="461dd-139">Les paramètres d’entrée _lpAllocateBuffer_ et _lpFreeBuffer_ pointent respectivement vers les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="461dd-139">The  _lpAllocateBuffer_ and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="461dd-140">Les valeurs exactes des pointeurs transmis à **HrAddColumnsEx** varient selon que l’appelant est une application cliente ou un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="461dd-140">The exact values of the pointers passed to **HrAddColumnsEx** depend on whether the caller is a client application or a service provider.</span></span> <span data-ttu-id="461dd-141">Un client transmet les pointeurs vers les fonctions MAPI avec les noms spécifiés.</span><span class="sxs-lookup"><span data-stu-id="461dd-141">A client passes pointers to the MAPI functions with the specified names.</span></span> <span data-ttu-id="461dd-142">Un fournisseur de services transmet les pointeurs qu’il a reçus dans son appel d’initialisation ou récupérés en appelant la méthode [IMAPISupport::GetMemAllocRoutines.](imapisupport-getmemallocroutines.md)</span><span class="sxs-lookup"><span data-stu-id="461dd-142">A service provider passes the pointers it received in its initialization call or retrieved by calling the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="461dd-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="461dd-143">See also</span></span>



[<span data-ttu-id="461dd-144">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="461dd-144">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)

