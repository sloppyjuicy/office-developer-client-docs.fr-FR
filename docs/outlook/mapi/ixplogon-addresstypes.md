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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: ca68c604152a7a28fb6a5357aa9c012ec7466b5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357210"
---
# <a name="ixplogonaddresstypes"></a><span data-ttu-id="ff5bd-103">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="ff5bd-103">IXPLogon::AddressTypes</span></span>

  
  
<span data-ttu-id="ff5bd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff5bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff5bd-105">Renvoie les types de destinataire gérés par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-105">Returns the types of recipients that the transport provider handles.</span></span>
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a><span data-ttu-id="ff5bd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff5bd-106">Parameters</span></span>

 <span data-ttu-id="ff5bd-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="ff5bd-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="ff5bd-108">remarquer Masque de des indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-108">[out] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="ff5bd-109">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="ff5bd-109">The following flag can be set:</span></span>
    
<span data-ttu-id="ff5bd-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ff5bd-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ff5bd-111">Les chaînes renvoyées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="ff5bd-112">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ff5bd-113">_lpcAdrType_</span><span class="sxs-lookup"><span data-stu-id="ff5bd-113">_lpcAdrType_</span></span>
  
> <span data-ttu-id="ff5bd-114">remarquer Pointeur vers le nombre d'entrées dans le tableau vers lequel pointe le paramètre _lpppszAdrTypeArray_ .</span><span class="sxs-lookup"><span data-stu-id="ff5bd-114">[out] A pointer to the count of entries in the array pointed to by the  _lpppszAdrTypeArray_ parameter.</span></span> 
    
 <span data-ttu-id="ff5bd-115">_lpppszAdrTypeArray_</span><span class="sxs-lookup"><span data-stu-id="ff5bd-115">_lpppszAdrTypeArray_</span></span>
  
> <span data-ttu-id="ff5bd-116">remarquer Pointeur vers un pointeur vers un tableau de chaînes qui identifient les types de destinataires.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-116">[out] A pointer to a pointer to an array of strings that identify recipient types.</span></span>
    
 <span data-ttu-id="ff5bd-117">_lpcMAPIUID_</span><span class="sxs-lookup"><span data-stu-id="ff5bd-117">_lpcMAPIUID_</span></span>
  
> <span data-ttu-id="ff5bd-118">remarquer Pointeur vers le nombre d'entrées dans le tableau vers lequel pointe le paramètre _lpppUIDArray_ .</span><span class="sxs-lookup"><span data-stu-id="ff5bd-118">[out] A pointer to the count of entries in the array pointed to by the  _lpppUIDArray_ parameter.</span></span> 
    
 <span data-ttu-id="ff5bd-119">_lpppUIDArray_</span><span class="sxs-lookup"><span data-stu-id="ff5bd-119">_lpppUIDArray_</span></span>
  
> <span data-ttu-id="ff5bd-120">remarquer Pointeur vers un pointeur vers un tableau de pointeurs vers des structures [MAPIUID](mapiuid.md) qui identifient les types de destinataires.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-120">[out] A pointer to a pointer to an array of pointers to [MAPIUID](mapiuid.md) structures that identify recipient types.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ff5bd-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ff5bd-121">Return value</span></span>

<span data-ttu-id="ff5bd-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="ff5bd-122">S_OK</span></span> 
  
> <span data-ttu-id="ff5bd-123">Le fournisseur de transport indiquait les types de destinataires qu'il peut gérer.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-123">The transport provider successfully indicated the types of recipients that it can handle.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="ff5bd-124">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="ff5bd-124">Notes to implementers</span></span>

<span data-ttu-id="ff5bd-125">Le spouleur MAPI appelle la méthode **IXPLogon:: AddressTypes** immédiatement après le retour d'un fournisseur de transport d'un appel à la méthode [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) afin que le fournisseur de transport puisse indiquer les types de destinataires qu'il gère.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-125">The MAPI spooler calls the **IXPLogon::AddressTypes** method immediately after a transport provider returns from a call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method so the transport provider can indicate what types of recipients it handles.</span></span> <span data-ttu-id="ff5bd-126">Pour cela, le fournisseur de transport doit renvoyer dans le paramètre _lpppszAdrTypeArray_ un pointeur vers un tableau de pointeurs vers des chaînes, ou renvoyer le pointeur vers un tableau de pointeurs vers **MAPIUID** à partir du paramètre _lpppUIDArray_ les structures, ou transmettre les valeurs des deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-126">To indicate this, the transport provider should pass back in the  _lpppszAdrTypeArray_ parameter a pointer to an array of pointers to strings, or pass back in the  _lpppUIDArray_ parameter a pointer to an array of pointers to **MAPIUID** structures, or pass values in both parameters.</span></span> 
  
<span data-ttu-id="ff5bd-127">Ces deux tableaux sont utilisés pour différents processus d'identification.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-127">These two arrays are used for different identification processes.</span></span> <span data-ttu-id="ff5bd-128">MAPI et le spouleur MAPI utilisent les structures [MAPIUID](mapiuid.md) dans le tableau _lpppUIDArray_ pour identifier les identificateurs d'entrée de destinataire qui sont directement gérés par le fournisseur de transport ou par le système de messagerie auquel se connecte le fournisseur de transport. .</span><span class="sxs-lookup"><span data-stu-id="ff5bd-128">MAPI and the MAPI spooler use the [MAPIUID](mapiuid.md) structures in the  _lpppUIDArray_ array to identify those recipient entry identifiers that are directly handled by the transport provider or by the messaging system to which the transport provider connects.</span></span> <span data-ttu-id="ff5bd-129">Ni MAPI ni le spouleur MAPI n'étend les adresses à l'aide d'identificateurs d'entrée contenus dans l'une de ces structures **MAPIUID** ; ces structures sont utilisées uniquement pour l'identification du type de destinataire.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-129">Neither MAPI nor the MAPI spooler expands addresses by using entry identifiers contained in any of these **MAPIUID** structures; these structures are used only for recipient type identification.</span></span> 
  
<span data-ttu-id="ff5bd-130">Le spouleur MAPI utilise chacune des chaînes du paramètre _lpppszAdrTypeArray_ pour un test de comparaison lorsqu'il détermine quel fournisseur de transport doit gérer les destinataires d'un message sortant.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-130">The MAPI spooler uses each of the strings in the  _lpppszAdrTypeArray_ parameter for a comparison test when it decides which transport provider should handle which recipients for an outbound message.</span></span> <span data-ttu-id="ff5bd-131">Si la propriété **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) d'un destinataire de message correspond exactement à une chaîne qui identifie l'un des types d'adresse de messagerie fournis par le fournisseur de transport, le fournisseur peut livrer le message à ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-131">If a message recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property exactly matches a string that identifies one of the messaging address types that the transport provider supplies, the provider can deliver the message to that recipient.</span></span>
  
<span data-ttu-id="ff5bd-132">Si plusieurs fournisseurs de transport peuvent gérer le même type de destinataire, MAPI sélectionne un fournisseur de transport en fonction de l'ordre de priorité de transport indiqué dans le profil de l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-132">If multiple transport providers can handle the same type of recipient, MAPI selects a transport provider based on the transport priority order indicated in the client application's profile.</span></span> <span data-ttu-id="ff5bd-133">Pour déterminer le fournisseur de transport à utiliser, le spouleur MAPI analyse toutes les structures **MAPIUID** spécifiées par le fournisseur par ordre de priorité, puis toutes les valeurs de type d'adresse spécifiées par le fournisseur par ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-133">To determine which transport provider to use, the MAPI spooler scans all provider-specified **MAPIUID** structures in priority order, and then all provider-specified address type values in priority order.</span></span> <span data-ttu-id="ff5bd-134">Le premier fournisseur de transport correspondant à un destinataire particulier de cette analyse obtient la première opportunité de gérer ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-134">The first transport provider to match a particular recipient in this scan gets the first opportunity to handle this recipient.</span></span> <span data-ttu-id="ff5bd-135">Si ce fournisseur ne gère pas le destinataire, le spouleur MAPI continue l'analyse pour trouver un fournisseur de transport pour un destinataire qui n'est pas encore géré.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-135">If that provider does not handle the recipient, the MAPI spooler continues the scan to find a transport provider for any recipient not yet handled.</span></span> <span data-ttu-id="ff5bd-136">L'analyse se poursuit jusqu'à ce qu'il n'existe plus de correspondances, auquel cas un rapport de non-remise est généré pour tout destinataire qui n'a pas été géré.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-136">The scan continues until no further matches are found, at which point a nondelivery report is generated for any recipient that was not handled.</span></span> 
  
<span data-ttu-id="ff5bd-137">Si le fournisseur prend toujours en charge un ensemble particulier de types de destinataires, le type d'adresse et les tableaux **MAPIUID** que le fournisseur de transport a transmis peuvent être statiques.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-137">If the provider always supports a particular set of recipient types, the address type and **MAPIUID** arrays that the transport provider passed can be static.</span></span> <span data-ttu-id="ff5bd-138">Si le fournisseur de transport construit ces tableaux de manière dynamique, il peut allouer de la mémoire à l'aide de l'objet de prise en charge précédemment transmis dans l'appel à **TransportLogon**, bien que cela ne soit pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-138">If the transport provider dynamically constructs these arrays, it can allocate memory by using the support object that was previously passed in the call to **TransportLogon**, although this is not necessary.</span></span>
  
<span data-ttu-id="ff5bd-139">La mémoire utilisée pour le type d'adresse et les tableaux **MAPIUID** doit rester allouée jusqu'au dernier appel à la méthode [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) , auquel cas le fournisseur de transport peut libérer de la mémoire, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-139">The memory used for the address type and **MAPIUID** arrays should remain allocated until the final call to the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method, at which time the transport provider can free the memory, if necessary.</span></span> <span data-ttu-id="ff5bd-140">Le fournisseur de transport ne doit pas modifier le contenu de ces tableaux après qu'il a été renvoyé de l'appel **TransportLogoff** .</span><span class="sxs-lookup"><span data-stu-id="ff5bd-140">The transport provider should not alter the contents of these arrays after it returns from the **TransportLogoff** call.</span></span> 
  
<span data-ttu-id="ff5bd-141">Un fournisseur de transport pouvant gérer tout type de destinataire peut renvoyer une valeur NULL dans le paramètre _lpppszAdrTypeArray_ .</span><span class="sxs-lookup"><span data-stu-id="ff5bd-141">A transport provider that can handle any type of recipient can return NULL in the  _lpppszAdrTypeArray_ parameter.</span></span> <span data-ttu-id="ff5bd-142">Les fournisseurs de transport pour les systèmes de messagerie LAN qui utilisent un serveur central pour transmettre les messages sortants à divers systèmes de messagerie étrangers le font généralement.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-142">Transport providers for LAN-based messaging systems that use a central server to deliver outgoing messages to various foreign message systems commonly do this.</span></span> <span data-ttu-id="ff5bd-143">Ce type de fournisseur de transport doit être installé en dernier dans l'ordre de priorité des spouleurs MAPI et MAPI du profil.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-143">This type of transport provider should be installed last in the MAPI and MAPI spooler priority order of transport providers in the profile.</span></span> 
  
<span data-ttu-id="ff5bd-144">Un fournisseur de transport qui ne prend pas en charge les messages sortants qui lui sont envoyés en fonction du type d'adresse doit renvoyer une seule chaîne de longueur nulle dans _lpppszAdrTypeArray_.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-144">A transport provider that does not support outbound messages that are dispatched to it based on address type should return a single zero-length string in  _lpppszAdrTypeArray_.</span></span> <span data-ttu-id="ff5bd-145">Si un fournisseur de transport ne prend en charge aucun type de destinataire, il doit transmettre NULL pour la structure **MAPIUID** et une chaîne vide pour le type d'adresse.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-145">If a transport provider supports no recipient types, it should pass NULL for the **MAPIUID** structure and an empty string for the address type.</span></span> <span data-ttu-id="ff5bd-146">Les fournisseurs de transport de ce type sont généralement utilisés pour installer un préprocesseur de messages.</span><span class="sxs-lookup"><span data-stu-id="ff5bd-146">Transport providers of this type are most commonly used to install a message preprocessor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ff5bd-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff5bd-147">See also</span></span>



[<span data-ttu-id="ff5bd-148">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="ff5bd-148">IXPLogon::TransportLogoff</span></span>](ixplogon-transportlogoff.md)
  
[<span data-ttu-id="ff5bd-149">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="ff5bd-149">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="ff5bd-150">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ff5bd-150">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ff5bd-151">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff5bd-151">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

