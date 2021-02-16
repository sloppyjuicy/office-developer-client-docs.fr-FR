---
title: ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ENTRYID
api_type:
- COM
ms.assetid: 8ebb21ca-5ad1-4dcc-97b6-2390664b5d8d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c77acb5226361ce31a7f6b1694de7fe23f8dd71b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415270"
---
# <a name="entryid"></a><span data-ttu-id="df64a-103">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="df64a-103">ENTRYID</span></span>

  
  
<span data-ttu-id="df64a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df64a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df64a-105">Contient un identificateur d’entrée pour un objet MAPI.</span><span class="sxs-lookup"><span data-stu-id="df64a-105">Contains an entry identifier for a MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df64a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="df64a-106">Header file:</span></span>  <br/> |<span data-ttu-id="df64a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df64a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="df64a-108">Macros associées :</span><span class="sxs-lookup"><span data-stu-id="df64a-108">Related macros:</span></span>  <br/> |<span data-ttu-id="df64a-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span><span class="sxs-lookup"><span data-stu-id="df64a-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a><span data-ttu-id="df64a-110">Members</span><span class="sxs-lookup"><span data-stu-id="df64a-110">Members</span></span>

 <span data-ttu-id="df64a-111">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="df64a-111">**abFlags**</span></span>
  
> <span data-ttu-id="df64a-112">Masque de bits d’indicateurs qui fournissent des informations décrivent l’objet.</span><span class="sxs-lookup"><span data-stu-id="df64a-112">Bitmask of flags that provide information that describes the object.</span></span> <span data-ttu-id="df64a-113">Seul le premier byte des indicateurs, **abFlags[0]**, peut être définie par le fournisseur ; les trois autres sont réservés.</span><span class="sxs-lookup"><span data-stu-id="df64a-113">Only the first byte of the flags, **abFlags[0]**, may be set by the provider; the other three are reserved.</span></span> <span data-ttu-id="df64a-114">Ces indicateurs ne doivent pas être définies pour les identificateurs d’entrée permanents ; Elles sont uniquement définies pour les identificateurs d’entrée à court terme.</span><span class="sxs-lookup"><span data-stu-id="df64a-114">These flags must not be set for permanent entry identifiers; they are only set for short-term entry identifiers.</span></span> <span data-ttu-id="df64a-115">Pour les clients, cette structure est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="df64a-115">To clients, this structure is read-only.</span></span> <span data-ttu-id="df64a-116">Les indicateurs suivants peuvent être **définies dans abFlags[0]**:</span><span class="sxs-lookup"><span data-stu-id="df64a-116">The following flags can be set in **abFlags[0]**:</span></span>
    
<span data-ttu-id="df64a-117">MAPI_NOTRECIP</span><span class="sxs-lookup"><span data-stu-id="df64a-117">MAPI_NOTRECIP</span></span> 
  
> <span data-ttu-id="df64a-118">L’identificateur d’entrée ne peut pas être utilisé comme destinataire d’un message.</span><span class="sxs-lookup"><span data-stu-id="df64a-118">The entry identifier cannot be used as a recipient on a message.</span></span>
    
<span data-ttu-id="df64a-119">MAPI_NOTRESERVED</span><span class="sxs-lookup"><span data-stu-id="df64a-119">MAPI_NOTRESERVED</span></span> 
  
> <span data-ttu-id="df64a-120">Les autres utilisateurs ne peuvent pas accéder à l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="df64a-120">Other users cannot access the entry identifier.</span></span>
    
<span data-ttu-id="df64a-121">MAPI_NOW</span><span class="sxs-lookup"><span data-stu-id="df64a-121">MAPI_NOW</span></span> 
  
> <span data-ttu-id="df64a-122">L’identificateur d’entrée ne peut pas être utilisé à d’autres moments.</span><span class="sxs-lookup"><span data-stu-id="df64a-122">The entry identifier cannot be used at other times.</span></span>
    
<span data-ttu-id="df64a-123">MAPI_SHORTTERM</span><span class="sxs-lookup"><span data-stu-id="df64a-123">MAPI_SHORTTERM</span></span> 
  
> <span data-ttu-id="df64a-124">L’identificateur d’entrée est à court terme.</span><span class="sxs-lookup"><span data-stu-id="df64a-124">The entry identifier is short-term.</span></span> <span data-ttu-id="df64a-125">Toutes les autres valeurs de cet byte doivent être définies, sauf si d’autres utilisations de l’identificateur d’entrée sont activées.</span><span class="sxs-lookup"><span data-stu-id="df64a-125">All other values in this byte must be set unless other uses of the entry identifier are enabled.</span></span>
    
<span data-ttu-id="df64a-126">MAPI_THISSESSION</span><span class="sxs-lookup"><span data-stu-id="df64a-126">MAPI_THISSESSION</span></span> 
  
> <span data-ttu-id="df64a-127">L’identificateur d’entrée ne peut pas être utilisé sur d’autres sessions.</span><span class="sxs-lookup"><span data-stu-id="df64a-127">The entry identifier cannot be used on other sessions.</span></span>
    
 <span data-ttu-id="df64a-128">**ab**</span><span class="sxs-lookup"><span data-stu-id="df64a-128">**ab**</span></span>
  
> <span data-ttu-id="df64a-129">Indique un tableau de données binaires utilisées par les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="df64a-129">Indicates an array of binary data that is used by service providers.</span></span> <span data-ttu-id="df64a-130">L’application cliente ne peut pas utiliser ce tableau.</span><span class="sxs-lookup"><span data-stu-id="df64a-130">The client application cannot use this array.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="df64a-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="df64a-131">Remarks</span></span>

<span data-ttu-id="df64a-132">La structure **ENTRYID** est utilisée par les fournisseurs de magasins de messages et de carnets d’adresses pour construire des identificateurs uniques pour leurs objets.</span><span class="sxs-lookup"><span data-stu-id="df64a-132">The **ENTRYID** structure is used by message store and address book providers to construct unique identifiers for their objects.</span></span> <span data-ttu-id="df64a-133">Les identificateurs d’entrée sont utilisés pour identifier les types d’objets suivants :</span><span class="sxs-lookup"><span data-stu-id="df64a-133">Entry identifiers are used to identify the following types of objects:</span></span> 
  
- <span data-ttu-id="df64a-134">Magasins de messages</span><span class="sxs-lookup"><span data-stu-id="df64a-134">Message stores</span></span>
    
- <span data-ttu-id="df64a-135">Folders</span><span class="sxs-lookup"><span data-stu-id="df64a-135">Folders</span></span>
    
- <span data-ttu-id="df64a-136">Messages</span><span class="sxs-lookup"><span data-stu-id="df64a-136">Messages</span></span>
    
- <span data-ttu-id="df64a-137">Conteneurs de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="df64a-137">Address book containers</span></span>
    
- <span data-ttu-id="df64a-138">Listes de distribution</span><span class="sxs-lookup"><span data-stu-id="df64a-138">Distribution lists</span></span>
    
- <span data-ttu-id="df64a-139">Utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="df64a-139">Messaging users</span></span>
    
- <span data-ttu-id="df64a-140">Objets de statut</span><span class="sxs-lookup"><span data-stu-id="df64a-140">Status objects</span></span>
    
- <span data-ttu-id="df64a-141">Sections de profil</span><span class="sxs-lookup"><span data-stu-id="df64a-141">Profile sections</span></span>
    
<span data-ttu-id="df64a-142">Chaque fournisseur utilise un format pour la structure **ENTRYID** qui est logique pour ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="df64a-142">Each provider uses a format for the **ENTRYID** structure that makes sense for that provider.</span></span> 
  
<span data-ttu-id="df64a-143">Chaque identificateur d'entrée ne peut être comparé directement, car un objet peut être représenté par deux valeurs binaires différentes.</span><span class="sxs-lookup"><span data-stu-id="df64a-143">Entry identifiers cannot be compared directly because one object can be represented by two different binary values.</span></span> <span data-ttu-id="df64a-144">Pour déterminer si deux identificateurs d’entrée représentent le même objet, appelez la méthode [IMAPISession::CompareEntryIDs.](imapisession-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="df64a-144">To determine whether two entry identifiers represent the same object, call the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
<span data-ttu-id="df64a-145">Lorsqu’un client appelle la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) d’un objet pour récupérer son identificateur d’entrée, l’objet renvoie la forme la plus permanente de l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="df64a-145">When a client calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its entry identifier, the object returns the most permanent form of the entry identifier.</span></span> <span data-ttu-id="df64a-146">Un client peut vérifier qu’un identificateur d’entrée est à long terme en vérifiant qu’aucun des indicateurs n’est définie dans le premier byte du membre **abFlags.**</span><span class="sxs-lookup"><span data-stu-id="df64a-146">A client can verify that an entry identifier is long-term by checking that none of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="df64a-147">Lorsqu’un client accède à un identificateur d’entrée par le biais d’une colonne dans une table, il est fort probable que cet identificateur d’entrée soit à court terme plutôt qu’à long terme.</span><span class="sxs-lookup"><span data-stu-id="df64a-147">When a client accesses an entry identifier through a column in a table, most likely this entry identifier is short-term instead of long-term.</span></span> <span data-ttu-id="df64a-148">Les identificateurs d’entrée à court terme peuvent être utilisés pour ouvrir leurs objets correspondants uniquement dans la session MAPI en cours.</span><span class="sxs-lookup"><span data-stu-id="df64a-148">Short-term entry identifiers can be used to open their corresponding objects only in the current MAPI session.</span></span> <span data-ttu-id="df64a-149">Un client peut vérifier qu’un identificateur d’entrée est à court terme en vérifiant que tous les indicateurs sont définies dans le premier byte du membre **abFlags.**</span><span class="sxs-lookup"><span data-stu-id="df64a-149">A client can verify that an entry identifier is short-term by checking that all of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="df64a-150">Certains identificateurs d’entrée sont à court terme, mais ont une utilisation à long terme.</span><span class="sxs-lookup"><span data-stu-id="df64a-150">Some entry identifiers are short-term, but have long-term use.</span></span> <span data-ttu-id="df64a-151">Un identificateur d’entrée de ce type aura un ou plusieurs des indicateurs appropriés définies dans le premier byte de son membre **abFlags.**</span><span class="sxs-lookup"><span data-stu-id="df64a-151">Such an entry identifier will have one or more of the appropriate flags set in the first byte of its **abFlags** member.</span></span> 
  
<span data-ttu-id="df64a-152">Une structure **ENTRYID** ressemble à une structure [FLATENTRY.](flatentry.md)</span><span class="sxs-lookup"><span data-stu-id="df64a-152">An **ENTRYID** structure resembles a [FLATENTRY](flatentry.md) structure.</span></span> <span data-ttu-id="df64a-153">Toutefois, il existe certaines différences :</span><span class="sxs-lookup"><span data-stu-id="df64a-153">However, there are some differences:</span></span> 
  
- <span data-ttu-id="df64a-154">Une structure **ENTRYID** ne stocke pas la taille de l’identificateur d’entrée ; une structure **FLATENTRY** le fait.</span><span class="sxs-lookup"><span data-stu-id="df64a-154">An **ENTRYID** structure does not store the size of the entry identifier; a **FLATENTRY** structure does.</span></span> 
    
- <span data-ttu-id="df64a-155">Une structure **ENTRYID** stocke séparément les données d’indicateur et le reste de l’identificateur d’entrée ; une **structure FLATENTRY** stocke les données d’indicateur avec le reste de l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="df64a-155">An **ENTRYID** structure stores the flag data and the rest of the entry identifier separately; a **FLATENTRY** structure stores the flag data with the rest of the entry identifier.</span></span> 
    
- <span data-ttu-id="df64a-156">Une structure **ENTRYID** est transmise en tant que paramètre aux méthodes de l’interface [IMAPIProp](imapipropiunknown.md) et aux méthodes **OpenEntry** suivantes : [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="df64a-156">An **ENTRYID** structure is passed as a parameter to the methods of the [IMAPIProp](imapipropiunknown.md) interface and to the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="df64a-157">Une structure **ENTRYID** est utilisée pour stocker un identificateur d’entrée sur le disque.</span><span class="sxs-lookup"><span data-stu-id="df64a-157">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> <span data-ttu-id="df64a-158">Une structure **FLATENTRY** permet de stocker un identificateur d’entrée dans un fichier ou de le transmettre dans un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="df64a-158">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> 
    
<span data-ttu-id="df64a-159">Les clients doivent toujours transmettre des identificateurs d’entrée alignés naturellement.</span><span class="sxs-lookup"><span data-stu-id="df64a-159">Clients should always pass in naturally aligned entry identifiers.</span></span> <span data-ttu-id="df64a-160">Bien que les fournisseurs doivent gérer des identificateurs d’entrée arbitrairement alignés, les clients ne doivent pas s’attendre à ce comportement.</span><span class="sxs-lookup"><span data-stu-id="df64a-160">Although providers should handle arbitrarily aligned entry identifiers, clients should not expect this behavior.</span></span> <span data-ttu-id="df64a-161">L’échec de la passe d’un bon identificateur d’entrée aligné à une méthode peut provoquer une erreur d’alignement sur les processeurs RISC.</span><span class="sxs-lookup"><span data-stu-id="df64a-161">Failure to pass a good aligned entry identifier to a method can cause an alignment fault on RISC processors.</span></span> 
  
<span data-ttu-id="df64a-162">Le facteur d’alignement naturel, généralement 8 octets, est le plus grand type de données pris en charge par le processeur, et généralement le même facteur d’alignement utilisé par l’allocation de mémoire système.</span><span class="sxs-lookup"><span data-stu-id="df64a-162">The natural alignment factor, typically 8 bytes, is the largest data type supported by the CPU, and usually the same alignment factor used by the system memory allocator.</span></span> <span data-ttu-id="df64a-163">Une adresse mémoire alignée naturellement permet au processeur d’accéder à n’importe quel type de données qu’il prend en charge à cette adresse sans générer de panne d’alignement.</span><span class="sxs-lookup"><span data-stu-id="df64a-163">A naturally aligned memory address allows the CPU to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="df64a-164">Pour les processeurs RISC, un type de données de taille N octets doit généralement être aligné sur un même multiple de N octets, l’adresse étant un même multiple de N.</span><span class="sxs-lookup"><span data-stu-id="df64a-164">For RISC CPUs, a data type of size N bytes must usually be aligned on an even multiple of N bytes, with the address being an even multiple of N.</span></span>
  
<span data-ttu-id="df64a-165">Pour plus d’informations, voir [Identificateurs d’entrée.](mapi-entry-identifiers.md)</span><span class="sxs-lookup"><span data-stu-id="df64a-165">For more information, see [Entry Identifiers](mapi-entry-identifiers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="df64a-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df64a-166">See also</span></span>



[<span data-ttu-id="df64a-167">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="df64a-167">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="df64a-168">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="df64a-168">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="df64a-169">Propriété canonique PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="df64a-169">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)


[<span data-ttu-id="df64a-170">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="df64a-170">MAPI Structures</span></span>](mapi-structures.md)

