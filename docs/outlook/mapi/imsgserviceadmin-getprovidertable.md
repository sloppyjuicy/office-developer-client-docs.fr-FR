---
title: IMsgServiceAdminGetProviderTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetProviderTable
api_type:
- COM
ms.assetid: 7180bff2-91ad-4e11-923e-2a9acefa3215
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 834b010dc4810e26264bb418de9630bc83b99810
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565290"
---
# <a name="imsgserviceadmingetprovidertable"></a><span data-ttu-id="0626a-103">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="0626a-103">IMsgServiceAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="0626a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0626a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0626a-105">Permet d’accéder à la table fournisseurs, une liste des fournisseurs de services dans le profil.</span><span class="sxs-lookup"><span data-stu-id="0626a-105">Provides access to the provider table, a listing of the service providers in the profile.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="0626a-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="0626a-106">Parameters</span></span>

 <span data-ttu-id="0626a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0626a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0626a-108">[in] Toujours NULL.</span><span class="sxs-lookup"><span data-stu-id="0626a-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="0626a-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="0626a-109">_lppTable_</span></span>
  
> <span data-ttu-id="0626a-110">[out] Pointeur vers un pointeur vers la table des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="0626a-110">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0626a-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0626a-111">Return value</span></span>

<span data-ttu-id="0626a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="0626a-112">S_OK</span></span> 
  
> <span data-ttu-id="0626a-113">Le tableau fournisseur a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="0626a-113">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0626a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0626a-114">Remarks</span></span>

<span data-ttu-id="0626a-115">La méthode **IMsgServiceAdmin::GetProviderTable** permet d’accéder à la table du fournisseur MAPI, un tableau qui répertorie le carnet d’adresses, banque de messages et des fournisseurs de transport actuellement installées dans le profil.</span><span class="sxs-lookup"><span data-stu-id="0626a-115">The **IMsgServiceAdmin::GetProviderTable** method provides access to the MAPI provider table, a table that lists all the address book, message store, and transport providers currently installed in the profile.</span></span> 
  
<span data-ttu-id="0626a-116">Contrairement à la table fournisseur renvoyée par la méthode [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) , la table fournisseur renvoyée par le biais de **IMsgServiceAdmin::GetProviderTable** ne peut pas inclure d’autres lignes qui représentent les informations associées avec un ou plusieurs fournisseurs de services dans le profil.</span><span class="sxs-lookup"><span data-stu-id="0626a-116">Unlike the provider table returned through the [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) method, the provider table returned through **IMsgServiceAdmin::GetProviderTable** cannot include additional rows that represent information associated with one or more service providers in the profile.</span></span> 
  
<span data-ttu-id="0626a-117">Fournisseurs qui ont été supprimés, ou sont en cours d’utilisation, ont été marquées pour suppression, mais ne sont pas inclus dans la table fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0626a-117">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="0626a-118">Tables du fournisseur sont statiques, ce qui signifie que les compléments suivantes ou les suppressions du profil ne sont pas reflétées dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="0626a-118">Provider tables are static, meaning that subsequent additions to or deletions from the profile are not reflected in the table.</span></span> 
  
<span data-ttu-id="0626a-119">Si le profil n’a aucun fournisseur, **GetProviderTable** renvoie un tableau avec des lignes de zéro et la valeur de retour de S_OK.</span><span class="sxs-lookup"><span data-stu-id="0626a-119">If the profile has no providers, **GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="0626a-120">Pour obtenir une liste complète des colonnes de la table fournisseur, voir [Tableau de fournisseur](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="0626a-120">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0626a-121">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="0626a-121">Notes to callers</span></span>

<span data-ttu-id="0626a-122">Pour récupérer les lignes d’une table du fournisseur dans l’ordre de transport, utilisez la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="0626a-122">To retrieve the rows of a provider table in transport order, use the following procedure:</span></span>
  
1. <span data-ttu-id="0626a-123">Appelez la méthode [IMAPITable](imapitable-restrict.md) pour imposer une restriction de propriété qui correspond à la propriété **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) avec MAPI_TRANSPORT_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="0626a-123">Call the [IMAPITable::Restrict](imapitable-restrict.md) method to impose a property restriction that matches the **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) property with MAPI_TRANSPORT_PROVIDER.</span></span>
    
2. <span data-ttu-id="0626a-124">Appelez la méthode [IMAPITable::SortTable](imapitable-sorttable.md) pour trier le tableau par la colonne **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0626a-124">Call the [IMAPITable::SortTable](imapitable-sorttable.md) method to sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
    
3. <span data-ttu-id="0626a-125">Appelez la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) pour obtenir les lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="0626a-125">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to get the rows of the table.</span></span> 
    
<span data-ttu-id="0626a-126">Une alternative à ces appels est pour émettre un appel à la fonction [HrQueryAllRows](hrqueryallrows.md) avec toutes les données appropriées structures passés unique.</span><span class="sxs-lookup"><span data-stu-id="0626a-126">An alternative to these calls is to make a single call to the [HrQueryAllRows](hrqueryallrows.md) function with all of the appropriate data structures passed in.</span></span> 
  
<span data-ttu-id="0626a-127">Si vous récupérez les colonnes **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de chacune des lignes, vous pouvez utiliser ce tableau de structures **MAPIUID** pour définir l’ordre de transport dans un appel à [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span><span class="sxs-lookup"><span data-stu-id="0626a-127">If you retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) columns in each of the rows, you can use this array of **MAPIUID** structures to set the transport order in a call to [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span></span>
  
<span data-ttu-id="0626a-128">Définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0626a-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter does the following:</span></span> 
  
- <span data-ttu-id="0626a-129">Définit le type de chaîne au format Unicode pour les données renvoyées pour les colonnes actives initiales de la table fournisseur par la méthode [IMAPITable::QueryColumns](imapitable-querycolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="0626a-129">Sets the string type to Unicode for data returned for the initial active columns of the provider table by the [IMAPITable::QueryColumns](imapitable-querycolumns.md) method.</span></span> <span data-ttu-id="0626a-130">Les colonnes actives initiales pour une table fournisseur sont les colonnes de que la méthode **QueryColumns** renvoie avant que le fournisseur qui contient la table appelle la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="0626a-130">The initial active columns for a provider table are those columns the **QueryColumns** method returns before the provider that contains the table calls the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="0626a-131">Définit le type de chaîne au format Unicode pour les données renvoyées pour les lignes actives initiales de la table fournisseur par **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="0626a-131">Sets the string type to Unicode for data returned for the initial active rows of the provider table by **QueryRows**.</span></span> <span data-ttu-id="0626a-132">Les lignes actives initiales pour une table du fournisseur sont les lignes **que QueryRows** renvoie avant que le fournisseur qui contient la table appelle **SetColumns**.</span><span class="sxs-lookup"><span data-stu-id="0626a-132">The initial active rows for a provider table are those rows **QueryRows** returns before the provider that contains the table calls **SetColumns**.</span></span> 
    
- <span data-ttu-id="0626a-133">Contrôle les types de propriétés de l’ordre de tri renvoyé par la méthode [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) avant que le client qui contient la table fournisseur appelle la méthode [IMAPITable::SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="0626a-133">Controls the property types of the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method before the client that contains the provider table calls the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0626a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0626a-134">See also</span></span>



[<span data-ttu-id="0626a-135">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="0626a-135">IMsgServiceAdmin::GetMsgServiceTable</span></span>](imsgserviceadmin-getmsgservicetable.md)
  
[<span data-ttu-id="0626a-136">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="0626a-136">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="0626a-137">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="0626a-137">IProviderAdmin::GetProviderTable</span></span>](iprovideradmin-getprovidertable.md)
  
[<span data-ttu-id="0626a-138">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0626a-138">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

