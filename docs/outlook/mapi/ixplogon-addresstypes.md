---
title: IXPLogonAddressTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.AddressTypes
api_type:
- COM
ms.assetid: 5add1f2b-d9e6-4d78-8739-c3848f6e32a3
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ca68c604152a7a28fb6a5357aa9c012ec7466b5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435375"
---
# <a name="ixplogonaddresstypes"></a><span data-ttu-id="be9c6-103">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="be9c6-103">IXPLogon::AddressTypes</span></span>

  
  
<span data-ttu-id="be9c6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be9c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be9c6-105">Renvoie les types de destinataires gérés par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="be9c6-105">Returns the types of recipients that the transport provider handles.</span></span>
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a><span data-ttu-id="be9c6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="be9c6-106">Parameters</span></span>

 <span data-ttu-id="be9c6-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="be9c6-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="be9c6-108">[out] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="be9c6-108">[out] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="be9c6-109">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="be9c6-109">The following flag can be set:</span></span>
    
<span data-ttu-id="be9c6-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="be9c6-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="be9c6-111">Les chaînes renvoyées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="be9c6-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="be9c6-112">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="be9c6-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="be9c6-113">_lpcAdrType_</span><span class="sxs-lookup"><span data-stu-id="be9c6-113">_lpcAdrType_</span></span>
  
> <span data-ttu-id="be9c6-114">[out] Pointeur vers le nombre d’entrées du tableau pointées par le _paramètre lpppszAdrTypeArray._</span><span class="sxs-lookup"><span data-stu-id="be9c6-114">[out] A pointer to the count of entries in the array pointed to by the  _lpppszAdrTypeArray_ parameter.</span></span> 
    
 <span data-ttu-id="be9c6-115">_lpppszAdrTypeArray_</span><span class="sxs-lookup"><span data-stu-id="be9c6-115">_lpppszAdrTypeArray_</span></span>
  
> <span data-ttu-id="be9c6-116">[out] Pointeur vers un pointeur vers un tableau de chaînes qui identifient les types de destinataires.</span><span class="sxs-lookup"><span data-stu-id="be9c6-116">[out] A pointer to a pointer to an array of strings that identify recipient types.</span></span>
    
 <span data-ttu-id="be9c6-117">_lpcMAPIUID_</span><span class="sxs-lookup"><span data-stu-id="be9c6-117">_lpcMAPIUID_</span></span>
  
> <span data-ttu-id="be9c6-118">[out] Pointeur vers le nombre d’entrées du tableau pointées par le _paramètre lpppUIDArray._</span><span class="sxs-lookup"><span data-stu-id="be9c6-118">[out] A pointer to the count of entries in the array pointed to by the  _lpppUIDArray_ parameter.</span></span> 
    
 <span data-ttu-id="be9c6-119">_lpppUIDArray_</span><span class="sxs-lookup"><span data-stu-id="be9c6-119">_lpppUIDArray_</span></span>
  
> <span data-ttu-id="be9c6-120">[out] Pointeur vers un pointeur vers un tableau de pointeurs vers des structures [MAPIUID](mapiuid.md) qui identifient les types de destinataires.</span><span class="sxs-lookup"><span data-stu-id="be9c6-120">[out] A pointer to a pointer to an array of pointers to [MAPIUID](mapiuid.md) structures that identify recipient types.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="be9c6-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="be9c6-121">Return value</span></span>

<span data-ttu-id="be9c6-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="be9c6-122">S_OK</span></span> 
  
> <span data-ttu-id="be9c6-123">Le fournisseur de transport a indiqué avec succès les types de destinataires qu’il peut gérer.</span><span class="sxs-lookup"><span data-stu-id="be9c6-123">The transport provider successfully indicated the types of recipients that it can handle.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="be9c6-124">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="be9c6-124">Notes to implementers</span></span>

<span data-ttu-id="be9c6-125">Lepooler MAPI appelle la méthode **IXPLogon::AddressTypes** immédiatement après le retour d’un fournisseur de transport à partir d’un appel à la méthode [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) afin que le fournisseur de transport puisse indiquer les types de destinataires qu’il gère.</span><span class="sxs-lookup"><span data-stu-id="be9c6-125">The MAPI spooler calls the **IXPLogon::AddressTypes** method immediately after a transport provider returns from a call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method so the transport provider can indicate what types of recipients it handles.</span></span> <span data-ttu-id="be9c6-126">Pour indiquer cela, le fournisseur de transport doit transmettre dans le paramètre  _lpppszAdrTypeArray_ un pointeur vers un tableau de pointeurs vers des chaînes, ou revenir dans le paramètre  _lpppUIDArray_ un pointeur vers un tableau de pointeurs vers des structures **MAPIUID,** ou transmettre des valeurs dans les deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="be9c6-126">To indicate this, the transport provider should pass back in the  _lpppszAdrTypeArray_ parameter a pointer to an array of pointers to strings, or pass back in the  _lpppUIDArray_ parameter a pointer to an array of pointers to **MAPIUID** structures, or pass values in both parameters.</span></span> 
  
<span data-ttu-id="be9c6-127">Ces deux tableaux sont utilisés pour différents processus d’identification.</span><span class="sxs-lookup"><span data-stu-id="be9c6-127">These two arrays are used for different identification processes.</span></span> <span data-ttu-id="be9c6-128">MAPI et le spouleur MAPI utilisent les structures [MAPIUID](mapiuid.md) dans le tableau  _lpppUIDArray_ pour identifier les identificateurs d’entrée de destinataire qui sont directement gérés par le fournisseur de transport ou par le système de messagerie auquel le fournisseur de transport se connecte.</span><span class="sxs-lookup"><span data-stu-id="be9c6-128">MAPI and the MAPI spooler use the [MAPIUID](mapiuid.md) structures in the  _lpppUIDArray_ array to identify those recipient entry identifiers that are directly handled by the transport provider or by the messaging system to which the transport provider connects.</span></span> <span data-ttu-id="be9c6-129">Ni MAPI, ni le spouleur MAPI ne développe les adresses à l’aide des identificateurs d’entrée contenus dans l’une de ces structures **MAPIUID** ; Ces structures sont utilisées uniquement pour l’identification du type de destinataire.</span><span class="sxs-lookup"><span data-stu-id="be9c6-129">Neither MAPI nor the MAPI spooler expands addresses by using entry identifiers contained in any of these **MAPIUID** structures; these structures are used only for recipient type identification.</span></span> 
  
<span data-ttu-id="be9c6-130">Lepooler MAPI utilise chacune des chaînes du paramètre  _lpppszAdrTypeArray_ pour un test de comparaison lorsqu’il détermine le fournisseur de transport qui doit gérer les destinataires d’un message sortant.</span><span class="sxs-lookup"><span data-stu-id="be9c6-130">The MAPI spooler uses each of the strings in the  _lpppszAdrTypeArray_ parameter for a comparison test when it decides which transport provider should handle which recipients for an outbound message.</span></span> <span data-ttu-id="be9c6-131">Si la propriété **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) d’un destinataire de message correspond exactement à une chaîne qui identifie l’un des types d’adresse de messagerie que le fournisseur de transport fournit, le fournisseur peut remettre le message à ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="be9c6-131">If a message recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property exactly matches a string that identifies one of the messaging address types that the transport provider supplies, the provider can deliver the message to that recipient.</span></span>
  
<span data-ttu-id="be9c6-132">Si plusieurs fournisseurs de transport peuvent gérer le même type de destinataire, MAPI sélectionne un fournisseur de transport en fonction de l’ordre de priorité de transport indiqué dans le profil de l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="be9c6-132">If multiple transport providers can handle the same type of recipient, MAPI selects a transport provider based on the transport priority order indicated in the client application's profile.</span></span> <span data-ttu-id="be9c6-133">Pour déterminer le fournisseur de transport à utiliser, le spouleur MAPI analyse toutes les structures **MAPIUID** spécifiées par le fournisseur dans l’ordre de priorité, puis toutes les valeurs de type d’adresse spécifiées par le fournisseur dans l’ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="be9c6-133">To determine which transport provider to use, the MAPI spooler scans all provider-specified **MAPIUID** structures in priority order, and then all provider-specified address type values in priority order.</span></span> <span data-ttu-id="be9c6-134">Le premier fournisseur de transport à faire correspondre un destinataire particulier dans cette analyse obtient la première opportunité de gérer ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="be9c6-134">The first transport provider to match a particular recipient in this scan gets the first opportunity to handle this recipient.</span></span> <span data-ttu-id="be9c6-135">Si ce fournisseur ne gère pas le destinataire, lepooler MAPI poursuit l’analyse pour rechercher un fournisseur de transport pour un destinataire qui n’a pas encore été géré.</span><span class="sxs-lookup"><span data-stu-id="be9c6-135">If that provider does not handle the recipient, the MAPI spooler continues the scan to find a transport provider for any recipient not yet handled.</span></span> <span data-ttu-id="be9c6-136">L’analyse se poursuit jusqu’à ce qu’aucune autre correspondance ne soit trouvée, auquel moment un rapport de non-découverte est généré pour tout destinataire qui n’a pas été géré.</span><span class="sxs-lookup"><span data-stu-id="be9c6-136">The scan continues until no further matches are found, at which point a nondelivery report is generated for any recipient that was not handled.</span></span> 
  
<span data-ttu-id="be9c6-137">Si le fournisseur prend toujours en charge un ensemble particulier de types de destinataires, le type d’adresse et les tableaux **MAPIUID** transmis par le fournisseur de transport peuvent être statiques.</span><span class="sxs-lookup"><span data-stu-id="be9c6-137">If the provider always supports a particular set of recipient types, the address type and **MAPIUID** arrays that the transport provider passed can be static.</span></span> <span data-ttu-id="be9c6-138">Si le fournisseur de transport construit dynamiquement ces tableaux, il peut allouer de la mémoire à l’aide de l’objet de support qui a été passé précédemment dans l’appel à **TransportLogon,** bien que cela ne soit pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="be9c6-138">If the transport provider dynamically constructs these arrays, it can allocate memory by using the support object that was previously passed in the call to **TransportLogon**, although this is not necessary.</span></span>
  
<span data-ttu-id="be9c6-139">La mémoire utilisée pour le type d’adresse et les tableaux **MAPIUID** doit rester allouée jusqu’à l’appel final à la méthode [IXPLogon::TransportLogoff,](ixplogon-transportlogoff.md) à laquelle le fournisseur de transport peut libérer de la mémoire, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="be9c6-139">The memory used for the address type and **MAPIUID** arrays should remain allocated until the final call to the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method, at which time the transport provider can free the memory, if necessary.</span></span> <span data-ttu-id="be9c6-140">Le fournisseur de transport ne doit pas modifier le contenu de ces tableaux après son retour de **l’appel TransportLogoff.**</span><span class="sxs-lookup"><span data-stu-id="be9c6-140">The transport provider should not alter the contents of these arrays after it returns from the **TransportLogoff** call.</span></span> 
  
<span data-ttu-id="be9c6-141">Un fournisseur de transport qui peut gérer n’importe quel type de destinataire peut renvoyer la valeur NULL dans le paramètre _lpppszAdrTypeArray._</span><span class="sxs-lookup"><span data-stu-id="be9c6-141">A transport provider that can handle any type of recipient can return NULL in the  _lpppszAdrTypeArray_ parameter.</span></span> <span data-ttu-id="be9c6-142">Les fournisseurs de transport pour les systèmes de messagerie laN qui utilisent un serveur central pour remettre des messages sortants à différents systèmes de messages étrangers le font généralement.</span><span class="sxs-lookup"><span data-stu-id="be9c6-142">Transport providers for LAN-based messaging systems that use a central server to deliver outgoing messages to various foreign message systems commonly do this.</span></span> <span data-ttu-id="be9c6-143">Ce type de fournisseur de transport doit être installé en dernier dans l’ordre de priorité dupooler MAPI et MAPI des fournisseurs de transport dans le profil.</span><span class="sxs-lookup"><span data-stu-id="be9c6-143">This type of transport provider should be installed last in the MAPI and MAPI spooler priority order of transport providers in the profile.</span></span> 
  
<span data-ttu-id="be9c6-144">Un fournisseur de transport qui ne prend pas en charge les messages sortants qui lui sont envoyés en fonction du type d’adresse doit renvoyer une seule chaîne de longueur nulle dans  _lpppszAdrTypeArray_.</span><span class="sxs-lookup"><span data-stu-id="be9c6-144">A transport provider that does not support outbound messages that are dispatched to it based on address type should return a single zero-length string in  _lpppszAdrTypeArray_.</span></span> <span data-ttu-id="be9c6-145">Si un fournisseur de transport ne prend en charge aucun type de destinataire, il doit transmettre null pour la structure **MAPIUID** et une chaîne vide pour le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="be9c6-145">If a transport provider supports no recipient types, it should pass NULL for the **MAPIUID** structure and an empty string for the address type.</span></span> <span data-ttu-id="be9c6-146">Les fournisseurs de transport de ce type sont le plus couramment utilisés pour installer un préprocesseur de message.</span><span class="sxs-lookup"><span data-stu-id="be9c6-146">Transport providers of this type are most commonly used to install a message preprocessor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="be9c6-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be9c6-147">See also</span></span>



[<span data-ttu-id="be9c6-148">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="be9c6-148">IXPLogon::TransportLogoff</span></span>](ixplogon-transportlogoff.md)
  
[<span data-ttu-id="be9c6-149">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="be9c6-149">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="be9c6-150">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="be9c6-150">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="be9c6-151">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be9c6-151">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

