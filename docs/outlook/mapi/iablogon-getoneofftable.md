---
title: IABLogonGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetOneOffTable
api_type:
- COM
ms.assetid: 7ac2a8d4-6890-4346-a6b6-34deca9dab50
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3732d8cbfaf9a6a10c62eae9e7a12b04de8a80ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583679"
---
# <a name="iablogongetoneofftable"></a><span data-ttu-id="89b41-103">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="89b41-103">IABLogon::GetOneOffTable</span></span>

  
  
<span data-ttu-id="89b41-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89b41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89b41-105">Renvoie un tableau des modèles uniques pour la création de destinataires à ajouter à la liste des destinataires d’un message sortant.</span><span class="sxs-lookup"><span data-stu-id="89b41-105">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="89b41-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="89b41-106">Parameters</span></span>

 <span data-ttu-id="89b41-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="89b41-107">_ulFlags_</span></span>
  
> <span data-ttu-id="89b41-108">[in] Masque de bits d’indicateurs qui contrôle le type des colonnes de chaîne inclus dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="89b41-108">[in] A bitmask of flags that controls the type of string columns included in the table.</span></span> <span data-ttu-id="89b41-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="89b41-109">The following flag can be set:</span></span>
    
<span data-ttu-id="89b41-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="89b41-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="89b41-111">Les colonnes de type chaîne sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="89b41-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="89b41-112">Si l’indicateur MAPI_UNICODE n’est pas définie, les colonnes de type chaîne sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="89b41-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="89b41-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="89b41-113">_lppTable_</span></span>
  
> <span data-ttu-id="89b41-114">[out] Pointeur vers un pointeur vers la table unique.</span><span class="sxs-lookup"><span data-stu-id="89b41-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="89b41-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="89b41-115">Return value</span></span>

<span data-ttu-id="89b41-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="89b41-116">S_OK</span></span> 
  
> <span data-ttu-id="89b41-117">Le tableau unique a été récupéré correctement.</span><span class="sxs-lookup"><span data-stu-id="89b41-117">The one-off table was successfully retrieved.</span></span>
    
<span data-ttu-id="89b41-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="89b41-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="89b41-119">Soit l’indicateur MAPI_UNICODE a été défini et le fournisseur de carnet d’adresses ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et le fournisseur de carnet d’adresses prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="89b41-119">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
<span data-ttu-id="89b41-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="89b41-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="89b41-121">Le fournisseur de carnet d’adresses ne fournit pas de modèles uniques.</span><span class="sxs-lookup"><span data-stu-id="89b41-121">The address book provider does not supply any one-off templates.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="89b41-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="89b41-122">Remarks</span></span>

<span data-ttu-id="89b41-123">MAPI appelle la méthode **GetOneOffTable** pour rendre des modèles uniques disponibles pour créer des destinataires.</span><span class="sxs-lookup"><span data-stu-id="89b41-123">MAPI calls the **GetOneOffTable** method to make available one-off templates to create recipients.</span></span> <span data-ttu-id="89b41-124">Les nouveaux destinataires sont ajoutés à la liste des destinataires d’un message sortant.</span><span class="sxs-lookup"><span data-stu-id="89b41-124">The new recipients are added to the recipient list of an outgoing message.</span></span> <span data-ttu-id="89b41-125">Fournisseurs de carnet d’adresses doivent prendre en charge la notification sur leur table unique pour informer les MAPI de modifications du modèle.</span><span class="sxs-lookup"><span data-stu-id="89b41-125">Address book providers should support notification on their one-off table to inform MAPI of template modifications.</span></span> <span data-ttu-id="89b41-126">MAPI tenir à jour la table unique open pour activer la mise à jour dynamique.</span><span class="sxs-lookup"><span data-stu-id="89b41-126">MAPI keeps the one-off table open to enable dynamic updating.</span></span> 
  
<span data-ttu-id="89b41-127">Fournisseurs de carnet d’adresses peuvent également en charge une table unique pour chacune de leurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="89b41-127">Address book providers can also support a one-off table for each of their containers.</span></span> <span data-ttu-id="89b41-128">Les appelants récupérer ce tableau unique à l’appel de méthode [d’IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur et demande la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="89b41-128">Callers retrieve this one-off table by calling the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="89b41-129">Les modèles disponibles par le biais de cette table sont utilisés pour ajouter des destinataires dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="89b41-129">The templates available through this table are used to add recipients to the container.</span></span> <span data-ttu-id="89b41-130">Pour une description des différences entre les deux types de tables uniques, voir [Implémentation de Tables uniques](implementing-one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="89b41-130">For a discussion of the differences between the two types of one-off tables, see [Implementing One-Off Tables](implementing-one-off-tables.md).</span></span>
  
<span data-ttu-id="89b41-131">Pour obtenir la liste des colonnes requises dans la table uniques d’un fournisseur de carnet d’adresses, voir [Les Tables uniques](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="89b41-131">For a list of the required columns in an address book provider's one-off table, see [One-Off Tables](one-off-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="89b41-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89b41-132">See also</span></span>



[<span data-ttu-id="89b41-133">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="89b41-133">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="89b41-134">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="89b41-134">IAddrBook::NewEntry</span></span>](iaddrbook-newentry.md)
  
[<span data-ttu-id="89b41-135">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="89b41-135">IMAPISupport::GetOneOffTable</span></span>](imapisupport-getoneofftable.md)
  
[<span data-ttu-id="89b41-136">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="89b41-136">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

