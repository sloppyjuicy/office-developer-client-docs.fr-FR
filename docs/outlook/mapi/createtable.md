---
title: Create table
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateTable
api_type:
- HeaderDef
ms.assetid: 106ce3d8-d0bf-4a0e-9a15-dc8988d0eb58
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5f42e1eb0d120d2fbb785e63b451acdd2d5a91f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783120"
---
# <a name="createtable"></a><span data-ttu-id="dd6d7-103">Create table</span><span class="sxs-lookup"><span data-stu-id="dd6d7-103">CreateTable</span></span>

  
  
<span data-ttu-id="dd6d7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dd6d7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dd6d7-105">Crée des structures et un handle d’objet pour un objet [ITableData](itabledataiunknown.md) qui peut être utilisé pour créer le contenu du tableau.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-105">Creates structures and an object handle for an [ITableData](itabledataiunknown.md) object which can be used to create table contents.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd6d7-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="dd6d7-106">Header file:</span></span>  <br/> |<span data-ttu-id="dd6d7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="dd6d7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dd6d7-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="dd6d7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dd6d7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dd6d7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dd6d7-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="dd6d7-110">Called by:</span></span>  <br/> |<span data-ttu-id="dd6d7-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="dd6d7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE CreateTable(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  ULONG ulTableType,
  ULONG ulPropTagIndexColumn,
  LPSPropTagArray lpSPropTagArrayColumns,
  LPTABLEDATA FAR * lppTableData
);
```

## <a name="parameters"></a><span data-ttu-id="dd6d7-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd6d7-112">Parameters</span></span>

 <span data-ttu-id="dd6d7-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="dd6d7-113">_lpInterface_</span></span>
  
> <span data-ttu-id="dd6d7-114">[in] Pointeur vers un identificateur d’interface (IID) pour l’objet de données de table.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-114">[in] Pointer to an interface identifier (IID) for the table data object.</span></span> <span data-ttu-id="dd6d7-115">L’identificateur d’interface valide est IID_IMAPITableData.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-115">The valid interface identifier is IID_IMAPITableData.</span></span> <span data-ttu-id="dd6d7-116">Passage de NULL dans le paramètre _lpInterface_ entraîne également l’objet de données de table retournée dans le paramètre _lppTableData_ pour effectuer un cast à l’interface standard pour un objet de données de table.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-116">Passing NULL in the  _lpInterface_ parameter also causes the table data object returned in the  _lppTableData_ parameter to be cast to the standard interface for a table data object.</span></span> 
    
 <span data-ttu-id="dd6d7-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="dd6d7-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="dd6d7-118">[in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="dd6d7-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="dd6d7-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="dd6d7-120">[in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) , à utiliser pour allouer plus de mémoire.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="dd6d7-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="dd6d7-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="dd6d7-122">[in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="dd6d7-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="dd6d7-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="dd6d7-124">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="dd6d7-125">_ulTableType_</span><span class="sxs-lookup"><span data-stu-id="dd6d7-125">_ulTableType_</span></span>
  
> <span data-ttu-id="dd6d7-126">[in] Type de table qui est disponible pour une application cliente ou d’un fournisseur de services dans le cadre des données de retour [IMAPITable::GetStatus](imapitable-getstatus.md) sur son point de vue table.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-126">[in] A table type that is available to a client application or service provider as part of the [IMAPITable::GetStatus](imapitable-getstatus.md) return data on its table views.</span></span> <span data-ttu-id="dd6d7-127">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dd6d7-127">Possible values are:</span></span> 
    
<span data-ttu-id="dd6d7-128">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="dd6d7-128">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="dd6d7-129">Contenu de la table est dynamique et peut changer en tant que les modifications de données sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-129">The table's contents are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="dd6d7-130">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="dd6d7-130">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="dd6d7-131">Les lignes dans le tableau sont fixe, mais les valeurs dans les lignes sont dynamiques et peuvent changer lorsque les modifications de données sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-131">The rows in the table are fixed, but the values in these rows are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="dd6d7-132">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="dd6d7-132">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="dd6d7-133">Le tableau est statique et le contenu n’est pas modifié lorsque les données sous-jacentes changent.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-133">The table is static and the contents do not change when the underlying data changes.</span></span> 
    
 <span data-ttu-id="dd6d7-134">_ulPropTagIndexColumn_</span><span class="sxs-lookup"><span data-stu-id="dd6d7-134">_ulPropTagIndexColumn_</span></span>
  
> <span data-ttu-id="dd6d7-135">[in] Numéro d’index de la colonne à utiliser lors de la modification des données de la table.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-135">[in] Index number of the column for use when changing table data.</span></span> 
    
 <span data-ttu-id="dd6d7-136">_lpSPropTagArrayColumns_</span><span class="sxs-lookup"><span data-stu-id="dd6d7-136">_lpSPropTagArrayColumns_</span></span>
  
> <span data-ttu-id="dd6d7-137">[in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété indiquant les propriétés requises dans la table pour laquelle l’objet contient des données.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-137">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties required in the table for which the object holds data.</span></span> 
    
 <span data-ttu-id="dd6d7-138">_lppTableData_</span><span class="sxs-lookup"><span data-stu-id="dd6d7-138">_lppTableData_</span></span>
  
> <span data-ttu-id="dd6d7-139">[out] Pointeur vers un pointeur vers l’objet de données de table renvoyée.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-139">[out] Pointer to a pointer to the returned table data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dd6d7-140">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="dd6d7-140">Return value</span></span>

<span data-ttu-id="dd6d7-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="dd6d7-141">S_OK</span></span> 
  
> <span data-ttu-id="dd6d7-142">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-142">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dd6d7-143">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd6d7-143">Remarks</span></span>

<span data-ttu-id="dd6d7-144">Les paramètres d’entrée _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ point [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), les fonctions [MAPIFreeBuffer](mapifreebuffer.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="dd6d7-144">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="dd6d7-145">Une application cliente appelant **Create table** passe pointeurs aux fonctions MAPI nommées uniquement ; un fournisseur de services transmet les pointeurs vers ces fonctions qu’il a reçu dans son appel d’initialisation ou récupérés par un appel à la méthode [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="dd6d7-145">A client application calling **CreateTable** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions that it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dd6d7-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd6d7-146">See also</span></span>



[<span data-ttu-id="dd6d7-147">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dd6d7-147">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

