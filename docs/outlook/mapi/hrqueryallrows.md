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
ms.openlocfilehash: 5c62e5919c6e605aa4b60f48072996ed1fd4c355
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783563"
---
# <a name="hrqueryallrows"></a><span data-ttu-id="b782b-103">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="b782b-103">HrQueryAllRows</span></span>

  
  
<span data-ttu-id="b782b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b782b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b782b-105">Récupère toutes les lignes d’une table.</span><span class="sxs-lookup"><span data-stu-id="b782b-105">Retrieves all rows of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b782b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b782b-106">Header file:</span></span>  <br/> |<span data-ttu-id="b782b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b782b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b782b-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="b782b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b782b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b782b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b782b-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="b782b-110">Called by:</span></span>  <br/> |<span data-ttu-id="b782b-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="b782b-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="b782b-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b782b-112">Parameters</span></span>

 <span data-ttu-id="b782b-113">_pTable_</span><span class="sxs-lookup"><span data-stu-id="b782b-113">_ptable_</span></span>
  
> <span data-ttu-id="b782b-114">[in] Pointeur vers le tableau MAPI à partir de laquelle les lignes sont extraites.</span><span class="sxs-lookup"><span data-stu-id="b782b-114">[in] Pointer to the MAPI table from which rows are retrieved.</span></span> 
    
 <span data-ttu-id="b782b-115">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="b782b-115">_ptaga_</span></span>
  
> <span data-ttu-id="b782b-116">[in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de propriété balises indiquant des colonnes de tableau.</span><span class="sxs-lookup"><span data-stu-id="b782b-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating table columns.</span></span> <span data-ttu-id="b782b-117">Ces balises sont utilisées pour sélectionner les colonnes spécifiques à récupérer.</span><span class="sxs-lookup"><span data-stu-id="b782b-117">These tags are used to select the specific columns to be retrieved.</span></span> <span data-ttu-id="b782b-118">Si le paramètre _ptaga_ est NULL, **HrQueryAllRows** récupère l’ensemble de la colonne entière de l’affichage tableau actuel passé dans le paramètre _ptable_ .</span><span class="sxs-lookup"><span data-stu-id="b782b-118">If the  _ptaga_ parameter is NULL, **HrQueryAllRows** retrieves the entire column set of the current table view passed in the  _ptable_ parameter.</span></span> 
    
 <span data-ttu-id="b782b-119">_Appuyez_</span><span class="sxs-lookup"><span data-stu-id="b782b-119">_pres_</span></span>
  
> <span data-ttu-id="b782b-120">[in] Pointeur vers une structure [SRestriction](srestriction.md) qui contient les restrictions de récupération.</span><span class="sxs-lookup"><span data-stu-id="b782b-120">[in] Pointer to an [SRestriction](srestriction.md) structure that contains retrieval restrictions.</span></span> <span data-ttu-id="b782b-121">Si le paramètre _Appuyez_ est NULL, **HrQueryAllRows** n’apporte aucune restriction.</span><span class="sxs-lookup"><span data-stu-id="b782b-121">If the  _pres_ parameter is NULL, **HrQueryAllRows** makes no restrictions.</span></span> 
    
 <span data-ttu-id="b782b-122">_PSO_</span><span class="sxs-lookup"><span data-stu-id="b782b-122">_psos_</span></span>
  
> <span data-ttu-id="b782b-123">[in] Pointeur vers une structure [SSortOrderSet](ssortorderset.md) qui identifie l’ordre de tri des colonnes à récupérer.</span><span class="sxs-lookup"><span data-stu-id="b782b-123">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order of the columns to be retrieved.</span></span> <span data-ttu-id="b782b-124">Si le paramètre _PSO_ est NULL, l’ordre de tri par défaut pour la table est utilisée.</span><span class="sxs-lookup"><span data-stu-id="b782b-124">If the  _psos_ parameter is NULL, the default sort order for the table is used.</span></span> 
    
 <span data-ttu-id="b782b-125">_crowsMax_</span><span class="sxs-lookup"><span data-stu-id="b782b-125">_crowsMax_</span></span>
  
> <span data-ttu-id="b782b-126">[in] Nombre maximal de lignes à récupérer.</span><span class="sxs-lookup"><span data-stu-id="b782b-126">[in] Maximum number of rows to be retrieved.</span></span> <span data-ttu-id="b782b-127">Si la valeur du paramètre _crowsMax_ est égale à zéro, aucune limite sur le nombre de lignes extraites n’est définie.</span><span class="sxs-lookup"><span data-stu-id="b782b-127">If the value of the  _crowsMax_ parameter is zero, no limit on the number of rows retrieved is set.</span></span> 
    
 <span data-ttu-id="b782b-128">_ppRows_</span><span class="sxs-lookup"><span data-stu-id="b782b-128">_pprows_</span></span>
  
> <span data-ttu-id="b782b-129">[out] Pointeur vers un pointeur vers la structure [SRowSet](srowset.md) retournée qui contient un tableau de pointeurs vers les lignes du tableau récupéré.</span><span class="sxs-lookup"><span data-stu-id="b782b-129">[out] Pointer to a pointer to the returned [SRowSet](srowset.md) structure that contains an array of pointers to the retrieved table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b782b-130">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="b782b-130">Return value</span></span>

<span data-ttu-id="b782b-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="b782b-131">S_OK</span></span> 
  
> <span data-ttu-id="b782b-132">L’appel extraire les lignes d’un tableau attendus.</span><span class="sxs-lookup"><span data-stu-id="b782b-132">The call retrieved the expected rows of a table.</span></span> 
    
<span data-ttu-id="b782b-133">MAPI_E_TABLE_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="b782b-133">MAPI_E_TABLE_TOO_BIG</span></span> 
  
> <span data-ttu-id="b782b-134">Le nombre de lignes dans le tableau est supérieur à la valeur transmise au paramètre _crowsMax_ .</span><span class="sxs-lookup"><span data-stu-id="b782b-134">The number of rows in the table is larger than the number passed for the  _crowsMax_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b782b-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="b782b-135">Remarks</span></span>

<span data-ttu-id="b782b-136">Une application cliente ou un fournisseur de services ne contrôle pas le nombre de lignes **que HrQueryAllRows** tente de récupérer, autres qu’en imposant une restriction vers laquelle pointe le paramètre _Appuyez_ .</span><span class="sxs-lookup"><span data-stu-id="b782b-136">A client application or service provider has no control over the number of rows **HrQueryAllRows** attempts to retrieve, other than by imposing a restriction pointed to by the  _pres_ parameter.</span></span> <span data-ttu-id="b782b-137">Le paramètre _crowsMax_ ne limite pas la récupération à un certain nombre de lignes du tableau, mais plutôt définit une quantité maximale de mémoire disponible pour contenir les lignes récupérées toutes les.</span><span class="sxs-lookup"><span data-stu-id="b782b-137">The  _crowsMax_ parameter does not limit the retrieval to a certain number of table rows, but rather defines a maximum amount of memory available to hold all retrieved rows.</span></span> <span data-ttu-id="b782b-138">La seule protection contre le dépassement de capacité de mémoire RAM très importante est la fonctionnalité provisoires fournie par le paramètre _crowsMax_.</span><span class="sxs-lookup"><span data-stu-id="b782b-138">The only protection against massive memory overflow is the stopgap feature provided by setting  _crowsMax_.</span></span> <span data-ttu-id="b782b-139">L’erreur renvoyée MAPI_E_TABLE_TOO_BIG signifie que le tableau contient trop de lignes pour qu’il ait en une seule fois dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="b782b-139">The error return MAPI_E_TABLE_TOO_BIG means the table contains too many rows to be held all at once in memory.</span></span> 
  
<span data-ttu-id="b782b-140">Tables qui sont généralement petites, par exemple un magasin de la table message ou un fournisseur généralement peuvent être en toute sécurité récupérés par **HrQueryAllRows**.</span><span class="sxs-lookup"><span data-stu-id="b782b-140">Tables that are typically small, such as a message store table or a provider table, usually can be safely retrieved with **HrQueryAllRows**.</span></span> <span data-ttu-id="b782b-141">Tables risque d’être très volumineuses, par exemple une table des matières ou même une table de destinataires, doivent être parcourues dans les sous-sections à l’aide de la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="b782b-141">Tables at risk of being very large, such as a contents table or even a recipients table, should be traversed in subsections using the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> 
  
<span data-ttu-id="b782b-142">Si les propriétés du tableau ne sont pas définies lorsque **HrQueryAllRows** est appelée, ils sont retournées avec le type de la propriété PT_NULL et l’identificateur de la propriété PROP_ID_NULL</span><span class="sxs-lookup"><span data-stu-id="b782b-142">If any table properties are undefined when **HrQueryAllRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL</span></span> 
  

