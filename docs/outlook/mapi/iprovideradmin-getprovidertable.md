---
title: IProviderAdminGetProviderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetProviderTable
api_type:
- COM
ms.assetid: e9deaa7c-430b-4e97-8ed6-f7c615956e0f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 843a61696def4398c22a244a7f3f66d7e5dc75ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279527"
---
# <a name="iprovideradmingetprovidertable"></a><span data-ttu-id="ece25-103">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="ece25-103">IProviderAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="ece25-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ece25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ece25-105">Fournit l'accès à la table du fournisseur du service de messagerie, une liste des fournisseurs de services dans le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="ece25-105">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="ece25-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ece25-106">Parameters</span></span>

 <span data-ttu-id="ece25-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ece25-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ece25-108">dans Masque de des indicateurs qui contrôle le type des chaînes renvoyées dans les colonnes de la table du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ece25-108">[in] A bitmask of flags that controls the type of the strings returned in the provider table's columns.</span></span> <span data-ttu-id="ece25-109">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="ece25-109">The following flag can be set:</span></span>
    
<span data-ttu-id="ece25-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ece25-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ece25-111">Les colonnes de chaîne sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="ece25-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="ece25-112">Si l'indicateur MAPI_UNICODE n'est pas défini, les colonnes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="ece25-112">If the MAPI_UNICODE flag is not set, the columns are in ANSI format.</span></span>
    
 <span data-ttu-id="ece25-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="ece25-113">_lppTable_</span></span>
  
> <span data-ttu-id="ece25-114">remarquer Pointeur vers un pointeur vers la table des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="ece25-114">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ece25-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ece25-115">Return value</span></span>

<span data-ttu-id="ece25-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ece25-116">S_OK</span></span> 
  
> <span data-ttu-id="ece25-117">La table du fournisseur a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="ece25-117">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ece25-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="ece25-118">Remarks</span></span>

<span data-ttu-id="ece25-119">La méthode **IProviderAdmin:: GetProviderTable** extrait un pointeur vers la table du fournisseur du service de messagerie, une table gérée par MAPI, qui contient des informations sur chaque fournisseur de services dans le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="ece25-119">The **IProviderAdmin::GetProviderTable** method retrieves a pointer to the message service's provider table, a table that MAPI maintains that contains information about each service provider in the message service.</span></span> 
  
<span data-ttu-id="ece25-120">Contrairement à la table du fournisseur renvoyée par la méthode [IMsgServiceAdmin:: GetProviderTable](imsgserviceadmin-getprovidertable.md) , la table du fournisseur renvoyée par **IProviderAdmin:: GetProviderTable** peut inclure des lignes supplémentaires qui représentent les informations associées à une ou plusieurs des les fournisseurs de services dans le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="ece25-120">Unlike the provider table returned by the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, the provider table returned by **IProviderAdmin::GetProviderTable** may include additional rows that represent information associated with one or more of the service providers in the message service.</span></span> <span data-ttu-id="ece25-121">Ces informations supplémentaires sont ajoutées au profil avec le mot clé «sections» du fichier MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="ece25-121">This extra information is added to the profile with the "Sections" keyword of the Mapisvc.inf file.</span></span> <span data-ttu-id="ece25-122">Lorsqu'un fournisseur dispose de sections de profil supplémentaires, il stocke les structures **MAPIUID** pour ces sections dans la propriété **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ece25-122">When a provider has extra profile sections, it stores the **MAPIUID** structures for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="ece25-123">**PR_SERVICE_EXTRA_UIDS** est enregistré dans la section du profil de service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="ece25-123">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="ece25-124">Les fournisseurs qui ont été supprimés ou qui sont en cours d'utilisation, mais qui ont été marqués pour suppression, ne sont pas inclus dans la table des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="ece25-124">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="ece25-125">Les tables de fournisseurs sont statiques, ce qui signifie que les ajouts ou suppressions ultérieurs du service de messagerie ne sont pas répercutés dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="ece25-125">Provider tables are static, meaning that subsequent additions to or deletions from the message service are not reflected in the table.</span></span> 
  
<span data-ttu-id="ece25-126">Si le service de messagerie n'a pas de fournisseur, **IProviderAdmin:: GetProviderTable** renvoie une table avec zéro ligne et la valeur de retour S_OK.</span><span class="sxs-lookup"><span data-stu-id="ece25-126">If the message service has no providers, **IProviderAdmin::GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="ece25-127">La définition de l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte le format des colonnes renvoyées par les méthodes [IMAPITable:: QueryColumns](imapitable-querycolumns.md) et [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="ece25-127">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> 
  
<span data-ttu-id="ece25-128">Cet indicateur contrôle également les types de propriétés dans l'ordre de tri retourné par la méthode [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="ece25-128">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="ece25-129">Pour obtenir la liste complète des colonnes de la table des fournisseurs, voir [Provider table](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ece25-129">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ece25-130">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="ece25-130">Notes to callers</span></span>

<span data-ttu-id="ece25-131">Pour récupérer les lignes d'une table de fournisseur dans l'ordre de transport, triez la table à l'aide de la colonne **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ece25-131">To retrieve the rows of a provider table in transport order, sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
  
<span data-ttu-id="ece25-132">Pour récupérer uniquement les lignes qui représentent les fournisseurs de services (sans inclure de lignes supplémentaires), limitez votre récupération aux lignes ayant une valeur PT_ERROR dans leur colonne **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ece25-132">To retrieve only those rows that represent service providers (without including any extra rows), limit your retrieval to the rows that have a value of PT_ERROR in their **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ece25-133">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ece25-133">MFCMAPI reference</span></span>

<span data-ttu-id="ece25-134">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ece25-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ece25-135">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="ece25-135">**File**</span></span>|<span data-ttu-id="ece25-136">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="ece25-136">**Function**</span></span>|<span data-ttu-id="ece25-137">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="ece25-137">**Comment**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ece25-138">MsgServiceTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="ece25-138">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="ece25-139">CMsgServiceTableDlg:: OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="ece25-139">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="ece25-140">MFCMAPI utilise la méthode **IProviderAdmin:: GetProviderTable** pour obtenir la table des fournisseurs à afficher dans une nouvelle boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ece25-140">MFCMAPI uses the **IProviderAdmin::GetProviderTable** method to get the table of providers to render in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ece25-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ece25-141">See also</span></span>



[<span data-ttu-id="ece25-142">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="ece25-142">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="ece25-143">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="ece25-143">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="ece25-144">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="ece25-144">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="ece25-145">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="ece25-145">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="ece25-146">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="ece25-146">IMsgServiceAdmin::GetProviderTable</span></span>](imsgserviceadmin-getprovidertable.md)
  
[<span data-ttu-id="ece25-147">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ece25-147">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="ece25-148">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="ece25-148">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

