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
ms.openlocfilehash: 65d633f0c2b0ce56793eaa55a417b5d6a816d449
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589846"
---
# <a name="ixplogonaddresstypes"></a><span data-ttu-id="bc352-103">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="bc352-103">IXPLogon::AddressTypes</span></span>

  
  
<span data-ttu-id="bc352-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc352-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc352-105">Renvoie les types de destinataires qui gère le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="bc352-105">Returns the types of recipients that the transport provider handles.</span></span>
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a><span data-ttu-id="bc352-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc352-106">Parameters</span></span>

 <span data-ttu-id="bc352-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="bc352-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="bc352-108">[out] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="bc352-108">[out] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="bc352-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="bc352-109">The following flag can be set:</span></span>
    
<span data-ttu-id="bc352-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bc352-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bc352-111">Les chaînes retournées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="bc352-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="bc352-112">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="bc352-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="bc352-113">_lpcAdrType_</span><span class="sxs-lookup"><span data-stu-id="bc352-113">_lpcAdrType_</span></span>
  
> <span data-ttu-id="bc352-114">[out] Un pointeur vers le nombre d’entrées dans le tableau indiqué par le paramètre _lpppszAdrTypeArray_ .</span><span class="sxs-lookup"><span data-stu-id="bc352-114">[out] A pointer to the count of entries in the array pointed to by the  _lpppszAdrTypeArray_ parameter.</span></span> 
    
 <span data-ttu-id="bc352-115">_lpppszAdrTypeArray_</span><span class="sxs-lookup"><span data-stu-id="bc352-115">_lpppszAdrTypeArray_</span></span>
  
> <span data-ttu-id="bc352-116">[out] Pointeur vers un pointeur vers un tableau de chaînes qui identifient les types de destinataires.</span><span class="sxs-lookup"><span data-stu-id="bc352-116">[out] A pointer to a pointer to an array of strings that identify recipient types.</span></span>
    
 <span data-ttu-id="bc352-117">_lpcMAPIUID_</span><span class="sxs-lookup"><span data-stu-id="bc352-117">_lpcMAPIUID_</span></span>
  
> <span data-ttu-id="bc352-118">[out] Un pointeur vers le nombre d’entrées dans le tableau indiqué par le paramètre _lpppUIDArray_ .</span><span class="sxs-lookup"><span data-stu-id="bc352-118">[out] A pointer to the count of entries in the array pointed to by the  _lpppUIDArray_ parameter.</span></span> 
    
 <span data-ttu-id="bc352-119">_lpppUIDArray_</span><span class="sxs-lookup"><span data-stu-id="bc352-119">_lpppUIDArray_</span></span>
  
> <span data-ttu-id="bc352-120">[out] Pointeur vers un pointeur vers un tableau de pointeurs vers des structures [MAPIUID](mapiuid.md) qui identifient les types de destinataires.</span><span class="sxs-lookup"><span data-stu-id="bc352-120">[out] A pointer to a pointer to an array of pointers to [MAPIUID](mapiuid.md) structures that identify recipient types.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bc352-121">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="bc352-121">Return value</span></span>

<span data-ttu-id="bc352-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="bc352-122">S_OK</span></span> 
  
> <span data-ttu-id="bc352-123">Le fournisseur de transport indiqué correctement les types de destinataires qu’il peut traiter.</span><span class="sxs-lookup"><span data-stu-id="bc352-123">The transport provider successfully indicated the types of recipients that it can handle.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="bc352-124">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="bc352-124">Notes to implementers</span></span>

<span data-ttu-id="bc352-125">Le spouleur MAPI appelle la méthode **IXPLogon::AddressTypes** immédiatement après qu’un fournisseur de transport renvoie à partir d’un appel à la méthode [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) afin que le fournisseur de transport peut indiquer quels types de destinataires qu’il gère.</span><span class="sxs-lookup"><span data-stu-id="bc352-125">The MAPI spooler calls the **IXPLogon::AddressTypes** method immediately after a transport provider returns from a call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method so the transport provider can indicate what types of recipients it handles.</span></span> <span data-ttu-id="bc352-126">Pour indiquer cela, le fournisseur de transport doit passer dans le paramètre _lpppszAdrTypeArray_ un pointeur vers un tableau de pointeurs vers des chaînes, ou passer dans le paramètre _lpppUIDArray_ un pointeur vers un tableau de pointeurs vers **MAPIUID** structures, ou passer de valeurs dans les deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="bc352-126">To indicate this, the transport provider should pass back in the  _lpppszAdrTypeArray_ parameter a pointer to an array of pointers to strings, or pass back in the  _lpppUIDArray_ parameter a pointer to an array of pointers to **MAPIUID** structures, or pass values in both parameters.</span></span> 
  
<span data-ttu-id="bc352-127">Ces deux tableaux est utilisés pour les processus d’identification différent.</span><span class="sxs-lookup"><span data-stu-id="bc352-127">These two arrays are used for different identification processes.</span></span> <span data-ttu-id="bc352-128">MAPI et le spouleur MAPI utilisent les structures [MAPIUID](mapiuid.md) dans le tableau _lpppUIDArray_ pour identifier les identificateurs d’entrée du destinataire qui sont directement gérés par le fournisseur de transport ou par le système de messagerie à laquelle se connecte le fournisseur de transport .</span><span class="sxs-lookup"><span data-stu-id="bc352-128">MAPI and the MAPI spooler use the [MAPIUID](mapiuid.md) structures in the  _lpppUIDArray_ array to identify those recipient entry identifiers that are directly handled by the transport provider or by the messaging system to which the transport provider connects.</span></span> <span data-ttu-id="bc352-129">Le spouleur MAPI ni MAPI développe des adresses à l’aide d’identificateurs d’entrée contenues dans une de ces structures **MAPIUID** ; Ces structures sont utilisés uniquement pour l’identification du type de destinataire.</span><span class="sxs-lookup"><span data-stu-id="bc352-129">Neither MAPI nor the MAPI spooler expands addresses by using entry identifiers contained in any of these **MAPIUID** structures; these structures are used only for recipient type identification.</span></span> 
  
<span data-ttu-id="bc352-130">Le spouleur MAPI utilise chacune des chaînes dans le paramètre _lpppszAdrTypeArray_ pour un test de comparaison lorsqu’il détermine quel fournisseur de transport doit gérer les destinataires d’un message sortant.</span><span class="sxs-lookup"><span data-stu-id="bc352-130">The MAPI spooler uses each of the strings in the  _lpppszAdrTypeArray_ parameter for a comparison test when it decides which transport provider should handle which recipients for an outbound message.</span></span> <span data-ttu-id="bc352-131">Si la propriété de **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) d’un destinataire de message correspond exactement à une chaîne qui identifie un des types d’adresse messagerie qui fournit le fournisseur de transport, le fournisseur peut remettre le message au destinataire.</span><span class="sxs-lookup"><span data-stu-id="bc352-131">If a message recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property exactly matches a string that identifies one of the messaging address types that the transport provider supplies, the provider can deliver the message to that recipient.</span></span>
  
<span data-ttu-id="bc352-132">Si plusieurs fournisseurs de transport peuvent gérer le même type de destinataire, MAPI sélectionne un fournisseur de transport selon l’ordre de priorité transport indiqué dans le profil de l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="bc352-132">If multiple transport providers can handle the same type of recipient, MAPI selects a transport provider based on the transport priority order indicated in the client application's profile.</span></span> <span data-ttu-id="bc352-133">Pour déterminer le fournisseur de transport à utiliser, le spouleur MAPI analyse tous les structures **MAPIUID** fournisseur spécifié dans l’ordre de priorité et ensuite tous les adresse spécifiée par fournisseur de valeurs de type dans l’ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="bc352-133">To determine which transport provider to use, the MAPI spooler scans all provider-specified **MAPIUID** structures in priority order, and then all provider-specified address type values in priority order.</span></span> <span data-ttu-id="bc352-134">Le premier fournisseur de transport pour correspondre à un destinataire particulier dans cette analyse Obtient la première possibilité de gérer ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="bc352-134">The first transport provider to match a particular recipient in this scan gets the first opportunity to handle this recipient.</span></span> <span data-ttu-id="bc352-135">Si ce fournisseur ne gère pas le destinataire, le spouleur MAPI continue l’analyse pour trouver un fournisseur de transport pour n’importe quel destinataire n’est pas encore géré.</span><span class="sxs-lookup"><span data-stu-id="bc352-135">If that provider does not handle the recipient, the MAPI spooler continues the scan to find a transport provider for any recipient not yet handled.</span></span> <span data-ttu-id="bc352-136">L’analyse se poursuit jusqu'à ce qu’aucune correspondance n’est détectée, à partir de laquelle un rapport de non-remise est généré pour n’importe quel destinataire n’est pas géré.</span><span class="sxs-lookup"><span data-stu-id="bc352-136">The scan continues until no further matches are found, at which point a nondelivery report is generated for any recipient that was not handled.</span></span> 
  
<span data-ttu-id="bc352-137">Si le fournisseur prend toujours en charge un ensemble particulier de types de destinataires, le type d’adresse et tableaux **MAPIUID** que le fournisseur de transport passé peuvent être statiques.</span><span class="sxs-lookup"><span data-stu-id="bc352-137">If the provider always supports a particular set of recipient types, the address type and **MAPIUID** arrays that the transport provider passed can be static.</span></span> <span data-ttu-id="bc352-138">Si le fournisseur de transport construit dynamiquement ces tableaux, elle peut allouer de la mémoire à l’aide de l’objet de prise en charge qui a été précédemment passée dans l’appel à **TransportLogon**, bien que cela n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bc352-138">If the transport provider dynamically constructs these arrays, it can allocate memory by using the support object that was previously passed in the call to **TransportLogon**, although this is not necessary.</span></span>
  
<span data-ttu-id="bc352-139">La mémoire utilisée pour le type d’adresse et tableaux **MAPIUID** doit rester allouée jusqu'à ce que le dernier appel à la méthode [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) , date à laquelle le fournisseur de transport peut libérer de la mémoire, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bc352-139">The memory used for the address type and **MAPIUID** arrays should remain allocated until the final call to the [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method, at which time the transport provider can free the memory, if necessary.</span></span> <span data-ttu-id="bc352-140">Le fournisseur de transport ne doit pas modifier le contenu de ces tableaux après le retour de l’appel **TransportLogoff** .</span><span class="sxs-lookup"><span data-stu-id="bc352-140">The transport provider should not alter the contents of these arrays after it returns from the **TransportLogoff** call.</span></span> 
  
<span data-ttu-id="bc352-141">Un fournisseur de transport qui peut gérer n’importe quel type de destinataire peut renvoyer la valeur NULL dans le paramètre _lpppszAdrTypeArray_ .</span><span class="sxs-lookup"><span data-stu-id="bc352-141">A transport provider that can handle any type of recipient can return NULL in the  _lpppszAdrTypeArray_ parameter.</span></span> <span data-ttu-id="bc352-142">Fournisseurs de transport pour les systèmes messages basée sur le réseau local qui permet de remettre les messages sortants à différents systèmes de messagerie étrangers généralement un serveur central pour cela.</span><span class="sxs-lookup"><span data-stu-id="bc352-142">Transport providers for LAN-based messaging systems that use a central server to deliver outgoing messages to various foreign message systems commonly do this.</span></span> <span data-ttu-id="bc352-143">Ce type de fournisseur de transport doit être installé en dernier dans le MAPI et MAPI ordre de priorité spouleur des fournisseurs de transport dans le profil.</span><span class="sxs-lookup"><span data-stu-id="bc352-143">This type of transport provider should be installed last in the MAPI and MAPI spooler priority order of transport providers in the profile.</span></span> 
  
<span data-ttu-id="bc352-144">Un fournisseur de transport qui ne prend pas en charge des messages sortants sont réparties selon le type d’adresse doit renvoyer une seule chaîne de longueur nulle dans _lpppszAdrTypeArray_.</span><span class="sxs-lookup"><span data-stu-id="bc352-144">A transport provider that does not support outbound messages that are dispatched to it based on address type should return a single zero-length string in  _lpppszAdrTypeArray_.</span></span> <span data-ttu-id="bc352-145">Si un fournisseur de transport prend en charge aucun type de destinataire, il doit passer la valeur NULL pour la structure **MAPIUID** et une chaîne vide pour le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="bc352-145">If a transport provider supports no recipient types, it should pass NULL for the **MAPIUID** structure and an empty string for the address type.</span></span> <span data-ttu-id="bc352-146">Fournisseurs de transport de ce type sont plus fréquemment utilisés pour installer un préprocesseur de message.</span><span class="sxs-lookup"><span data-stu-id="bc352-146">Transport providers of this type are most commonly used to install a message preprocessor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc352-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc352-147">See also</span></span>



[<span data-ttu-id="bc352-148">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="bc352-148">IXPLogon::TransportLogoff</span></span>](ixplogon-transportlogoff.md)
  
[<span data-ttu-id="bc352-149">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="bc352-149">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="bc352-150">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="bc352-150">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="bc352-151">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bc352-151">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

