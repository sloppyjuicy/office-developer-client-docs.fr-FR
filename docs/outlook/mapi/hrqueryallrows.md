---
title: HrQueryAllRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrQueryAllRows
api_type:
- HeaderDef
ms.assetid: b08fadcf-cdf3-48b7-9489-d7f745266482
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0f09304f21180d9ebc2a1e1dcc54ebadd3622804
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348243"
---
# <a name="hrqueryallrows"></a><span data-ttu-id="0d8a4-103">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="0d8a4-103">HrQueryAllRows</span></span>

  
  
<span data-ttu-id="0d8a4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d8a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d8a4-105">Récupère toutes les lignes d'un tableau.</span><span class="sxs-lookup"><span data-stu-id="0d8a4-105">Retrieves all rows of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d8a4-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="0d8a4-106">Header file:</span></span>  <br/> |<span data-ttu-id="0d8a4-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="0d8a4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0d8a4-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="0d8a4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0d8a4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0d8a4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0d8a4-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="0d8a4-110">Called by:</span></span>  <br/> |<span data-ttu-id="0d8a4-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="0d8a4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrQueryAllRows(
  LPMAPITABLE ptable,
  LPSPropTagArray ptaga,
  LPSRestriction pres,
  LPSSortOrderSet psos,
  LONG crowsMax,
  LPSRowSet FAR * pprows
);
```

## <a name="parameters"></a><span data-ttu-id="0d8a4-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d8a4-112">Parameters</span></span>

 <span data-ttu-id="0d8a4-113">_pTable_</span><span class="sxs-lookup"><span data-stu-id="0d8a4-113">_ptable_</span></span>
  
> <span data-ttu-id="0d8a4-114">dans Pointeur vers la table MAPI à partir de laquelle les lignes sont extraites.</span><span class="sxs-lookup"><span data-stu-id="0d8a4-114">[in] Pointer to the MAPI table from which rows are retrieved.</span></span> 
    
 <span data-ttu-id="0d8a4-115">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="0d8a4-115">_ptaga_</span></span>
  
> <span data-ttu-id="0d8a4-116">dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété indiquant des colonnes de tableau.</span><span class="sxs-lookup"><span data-stu-id="0d8a4-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating table columns.</span></span> <span data-ttu-id="0d8a4-117">Ces balises sont utilisées pour sélectionner les colonnes spécifiques à récupérer.</span><span class="sxs-lookup"><span data-stu-id="0d8a4-117">These tags are used to select the specific columns to be retrieved.</span></span> <span data-ttu-id="0d8a4-118">Si le paramètre _ptaga_ est null, **HrQueryAllRows** récupère le jeu de colonnes entier de la vue de table actuelle passée dans le paramètre _pTable_ .</span><span class="sxs-lookup"><span data-stu-id="0d8a4-118">If the  _ptaga_ parameter is NULL, **HrQueryAllRows** retrieves the entire column set of the current table view passed in the  _ptable_ parameter.</span></span> 
    
 <span data-ttu-id="0d8a4-119">_avance_</span><span class="sxs-lookup"><span data-stu-id="0d8a4-119">_pres_</span></span>
  
> <span data-ttu-id="0d8a4-120">dans Pointeur vers une structure [SRestriction](srestriction.md) qui contient des restrictions de récupération.</span><span class="sxs-lookup"><span data-stu-id="0d8a4-120">[in] Pointer to an [SRestriction](srestriction.md) structure that contains retrieval restrictions.</span></span> <span data-ttu-id="0d8a4-121">Si le paramètre _pres_ est null, **HrQueryAllRows** n'impose aucune restriction.</span><span class="sxs-lookup"><span data-stu-id="0d8a4-121">If the  _pres_ parameter is NULL, **HrQueryAllRows** makes no restrictions.</span></span> 
    
 <span data-ttu-id="0d8a4-122">_PSOS_</span><span class="sxs-lookup"><span data-stu-id="0d8a4-122">_psos_</span></span>
  
> <span data-ttu-id="0d8a4-123">dans Pointeur vers une structure [SSortOrderSet](ssortorderset.md) identifiant l'ordre de tri des colonnes à récupérer.</span><span class="sxs-lookup"><span data-stu-id="0d8a4-123">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order of the columns to be retrieved.</span></span> <span data-ttu-id="0d8a4-124">Si le paramètre _PSOS_ est null, l'ordre de tri par défaut de la table est utilisé.</span><span class="sxs-lookup"><span data-stu-id="0d8a4-124">If the  _psos_ parameter is NULL, the default sort order for the table is used.</span></span> 
    
 <span data-ttu-id="0d8a4-125">_crowsMax_</span><span class="sxs-lookup"><span data-stu-id="0d8a4-125">_crowsMax_</span></span>
  
> <span data-ttu-id="0d8a4-126">dans Nombre maximal de lignes à récupérer.</span><span class="sxs-lookup"><span data-stu-id="0d8a4-126">[in] Maximum number of rows to be retrieved.</span></span> <span data-ttu-id="0d8a4-127">Si la valeur du paramètre _crowsMax_ est égale à zéro, aucune limite n'est définie pour le nombre de lignes extraites.</span><span class="sxs-lookup"><span data-stu-id="0d8a4-127">If the value of the  _crowsMax_ parameter is zero, no limit on the number of rows retrieved is set.</span></span> 
    
 <span data-ttu-id="0d8a4-128">_ppRows_</span><span class="sxs-lookup"><span data-stu-id="0d8a4-128">_pprows_</span></span>
  
> <span data-ttu-id="0d8a4-129">remarquer Pointeur vers un pointeur vers la structure [SRowSet](srowset.md) renvoyée qui contient un tableau de pointeurs vers les lignes de tableau récupérées.</span><span class="sxs-lookup"><span data-stu-id="0d8a4-129">[out] Pointer to a pointer to the returned [SRowSet](srowset.md) structure that contains an array of pointers to the retrieved table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0d8a4-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0d8a4-130">Return value</span></span>

<span data-ttu-id="0d8a4-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d8a4-131">S_OK</span></span> 
  
> <span data-ttu-id="0d8a4-132">L'appel a extrait les lignes attendues d'un tableau.</span><span class="sxs-lookup"><span data-stu-id="0d8a4-132">The call retrieved the expected rows of a table.</span></span> 
    
<span data-ttu-id="0d8a4-133">MAPI_E_TABLE_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="0d8a4-133">MAPI_E_TABLE_TOO_BIG</span></span> 
  
> <span data-ttu-id="0d8a4-134">Le nombre de lignes dans le tableau est supérieur au nombre passé pour le paramètre _crowsMax_ .</span><span class="sxs-lookup"><span data-stu-id="0d8a4-134">The number of rows in the table is larger than the number passed for the  _crowsMax_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0d8a4-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="0d8a4-135">Remarks</span></span>

<span data-ttu-id="0d8a4-136">Une application cliente ou un fournisseur de services ne contrôle pas le nombre de lignes **HrQueryAllRows** tente de récupérer, à l'exception du fait qu'il impose une restriction vers laquelle pointe le paramètre _pres_ .</span><span class="sxs-lookup"><span data-stu-id="0d8a4-136">A client application or service provider has no control over the number of rows **HrQueryAllRows** attempts to retrieve, other than by imposing a restriction pointed to by the  _pres_ parameter.</span></span> <span data-ttu-id="0d8a4-137">Le paramètre _crowsMax_ ne limite pas la récupération à un certain nombre de lignes de tableau, mais définit plutôt une quantité maximale de mémoire disponible pour contenir toutes les lignes extraites.</span><span class="sxs-lookup"><span data-stu-id="0d8a4-137">The  _crowsMax_ parameter does not limit the retrieval to a certain number of table rows, but rather defines a maximum amount of memory available to hold all retrieved rows.</span></span> <span data-ttu-id="0d8a4-138">La seule protection contre le débordement de mémoire massive est la fonctionnalité stopgap fournie par la définition de _crowsMax_.</span><span class="sxs-lookup"><span data-stu-id="0d8a4-138">The only protection against massive memory overflow is the stopgap feature provided by setting  _crowsMax_.</span></span> <span data-ttu-id="0d8a4-139">L'erreur Return MAPI_E_TABLE_TOO_BIG signifie que le tableau contient trop de lignes à conserver en une seule fois dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="0d8a4-139">The error return MAPI_E_TABLE_TOO_BIG means the table contains too many rows to be held all at once in memory.</span></span> 
  
<span data-ttu-id="0d8a4-140">Les tables généralement petites, comme une table de banque de messages ou une table de fournisseurs, peuvent généralement être récupérées en toute sécurité avec **HrQueryAllRows**.</span><span class="sxs-lookup"><span data-stu-id="0d8a4-140">Tables that are typically small, such as a message store table or a provider table, usually can be safely retrieved with **HrQueryAllRows**.</span></span> <span data-ttu-id="0d8a4-141">Les tables susceptibles d'être très volumineuses, telles qu'une table des matières ou même une table de destinataires, doivent être parcourues dans des sous-sections à l'aide de la méthode [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="0d8a4-141">Tables at risk of being very large, such as a contents table or even a recipients table, should be traversed in subsections using the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> 
  
<span data-ttu-id="0d8a4-142">Si les propriétés d'une table ne sont pas définies lors de l'appel de **HrQueryAllRows** , elles sont renvoyées avec le type de propriété PT_NULL et l'identificateur de propriété PROP_ID_NULL</span><span class="sxs-lookup"><span data-stu-id="0d8a4-142">If any table properties are undefined when **HrQueryAllRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL</span></span> 
  

