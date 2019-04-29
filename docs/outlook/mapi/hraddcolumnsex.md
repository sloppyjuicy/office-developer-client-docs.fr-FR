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
# <a name="hraddcolumnsex"></a><span data-ttu-id="bbc84-103">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="bbc84-103">HrAddColumnsEx</span></span>

  
  
<span data-ttu-id="bbc84-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbc84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbc84-105">Ajoute ou déplace des colonnes au début d'une table existante.</span><span class="sxs-lookup"><span data-stu-id="bbc84-105">Adds or moves columns to the beginning of an existing table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bbc84-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bbc84-106">Header file:</span></span>  <br/> |<span data-ttu-id="bbc84-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="bbc84-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="bbc84-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="bbc84-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bbc84-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bbc84-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bbc84-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="bbc84-110">Called by:</span></span>  <br/> |<span data-ttu-id="bbc84-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="bbc84-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="bbc84-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bbc84-112">Parameters</span></span>

 <span data-ttu-id="bbc84-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="bbc84-113">_lptbl_</span></span>
  
> <span data-ttu-id="bbc84-114">dans Pointeur vers le tableau MAPI affecté.</span><span class="sxs-lookup"><span data-stu-id="bbc84-114">[in] Pointer to the MAPI table affected.</span></span> 
    
 <span data-ttu-id="bbc84-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="bbc84-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="bbc84-116">dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété pour les propriétés à ajouter ou déplacer au début du tableau.</span><span class="sxs-lookup"><span data-stu-id="bbc84-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="bbc84-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="bbc84-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="bbc84-118">dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="bbc84-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="bbc84-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="bbc84-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="bbc84-120">dans Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="bbc84-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="bbc84-121">_lpfnFilterColumns_</span><span class="sxs-lookup"><span data-stu-id="bbc84-121">_lpfnFilterColumns_</span></span>
  
> <span data-ttu-id="bbc84-122">dans Pointeur vers une fonction de rappel fournie par l'appelant.</span><span class="sxs-lookup"><span data-stu-id="bbc84-122">[in] Pointer to a callback function furnished by the caller.</span></span> <span data-ttu-id="bbc84-123">Si le paramètre _lpfnFilterColumns_ est défini sur null, aucun rappel n'est effectué.</span><span class="sxs-lookup"><span data-stu-id="bbc84-123">If the  _lpfnFilterColumns_ parameter is set to NULL, no callback is made.</span></span> 
    
 <span data-ttu-id="bbc84-124">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="bbc84-124">_ptaga_</span></span>
  
> <span data-ttu-id="bbc84-125">dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient le tableau de balises de propriété déjà présentes dans le tableau avant l'ajout ou le déplacement des propriétés vers le début.</span><span class="sxs-lookup"><span data-stu-id="bbc84-125">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the array of property tags already existing in the table before properties are added or moved to the beginning.</span></span> <span data-ttu-id="bbc84-126">**HrAddColumnsEx** transmet ce pointeur en tant que paramètre à la fonction de rappel pointée par _lpfnFilterColumns_.</span><span class="sxs-lookup"><span data-stu-id="bbc84-126">**HrAddColumnsEx** passes this pointer as the parameter to the callback function pointed to by  _lpfnFilterColumns_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bbc84-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bbc84-127">Return value</span></span>

<span data-ttu-id="bbc84-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="bbc84-128">S_OK</span></span> 
  
> <span data-ttu-id="bbc84-129">L'appel a réussi et les colonnes spécifiées ont été déplacées ou ajoutées.</span><span class="sxs-lookup"><span data-stu-id="bbc84-129">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bbc84-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="bbc84-130">Remarks</span></span>

<span data-ttu-id="bbc84-131">Les propriétés transmises à **HrAddColumnsEx** à l'aide du paramètre _lpproptagColumnsNew_ deviennent les premières propriétés exposées lors des appels suivants de la méthode [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="bbc84-131">The properties passed to **HrAddColumnsEx** using the  _lpproptagColumnsNew_ parameter become the first properties exposed on subsequent calls to the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="bbc84-132">Les propriétés précédemment répertoriées dans le tableau qui n'ont pas été spécifiées dans le paramètre _lpproptagColumnsNew_ sont exposées après toutes les propriétés ajoutées et déplacées.</span><span class="sxs-lookup"><span data-stu-id="bbc84-132">Any properties previously in the table that were not specified in the  _lpproptagColumnsNew_ parameter are exposed after all the added and moved properties.</span></span> 
  
<span data-ttu-id="bbc84-133">Si les propriétés d'une table ne sont pas définies lors de l'appel de **QueryRows** , elles sont renvoyées avec le type de propriété PT_NULL et l'identificateur de propriété PROP_ID_NULL.</span><span class="sxs-lookup"><span data-stu-id="bbc84-133">If any table properties are undefined when **QueryRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bbc84-134">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="bbc84-134">Notes to callers</span></span>

<span data-ttu-id="bbc84-135">La fonction **HrAddColumnsEx** permet à l'appelant de fournir une fonction de rappel pour filtrer les colonnes qui se trouvaient déjà dans la table, par exemple pour convertir les chaînes de type PT_UNICODE en PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="bbc84-135">The **HrAddColumnsEx** function allows the caller to furnish a callback function to filter the columns that were already in the table, for example to convert strings from property type PT_UNICODE to PT_STRING8.</span></span> <span data-ttu-id="bbc84-136">**HrAddColumnsEx** transmet un pointeur vers le jeu de colonnes précédemment existant en tant que paramètre de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="bbc84-136">**HrAddColumnsEx** passes a pointer to the previously existing column set as the parameter to the callback function.</span></span> <span data-ttu-id="bbc84-137">La fonction de rappel peut modifier des données dans le tableau de balises de propriété, mais ne peut pas ajouter de nouvelles balises.</span><span class="sxs-lookup"><span data-stu-id="bbc84-137">The callback function can change data in the property tag array but cannot add new tags.</span></span> 
  
 <span data-ttu-id="bbc84-138">**HrAddColumnsEx** appelle d'abord la fonction de rappel si elle est fournie, puis ajoute ou déplace les colonnes spécifiées, et enfin, il appelle la méthode [IMAPITable:: SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="bbc84-138">**HrAddColumnsEx** first calls the callback function if one is furnished, then adds or moves the specified columns, and finally calls [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> 
  
<span data-ttu-id="bbc84-139">Les paramètres d'entrée _lpAllocateBuffer_ et _lpFreeBuffer_ pointent vers les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIFreeBuffer](mapifreebuffer.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="bbc84-139">The  _lpAllocateBuffer_ and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="bbc84-140">Les valeurs exactes des pointeurs transmis à **HrAddColumnsEx** varient selon que l'appelant est une application cliente ou un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="bbc84-140">The exact values of the pointers passed to **HrAddColumnsEx** depend on whether the caller is a client application or a service provider.</span></span> <span data-ttu-id="bbc84-141">Un client passe des pointeurs aux fonctions MAPI avec les noms spécifiés.</span><span class="sxs-lookup"><span data-stu-id="bbc84-141">A client passes pointers to the MAPI functions with the specified names.</span></span> <span data-ttu-id="bbc84-142">Un fournisseur de services transmet les pointeurs reçus dans son appel d'initialisation ou les récupère en appelant la méthode [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="bbc84-142">A service provider passes the pointers it received in its initialization call or retrieved by calling the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bbc84-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbc84-143">See also</span></span>



[<span data-ttu-id="bbc84-144">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="bbc84-144">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)

