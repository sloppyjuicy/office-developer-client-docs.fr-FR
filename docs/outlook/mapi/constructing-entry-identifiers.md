---
title: Construction d'identificateurs d'entrée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8d48c2584fa5b7e862102e401ea8165821607f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427947"
---
# <a name="constructing-entry-identifiers"></a><span data-ttu-id="18fd2-103">Construction d'identificateurs d'entrée</span><span class="sxs-lookup"><span data-stu-id="18fd2-103">Constructing Entry Identifiers</span></span>

  
  
<span data-ttu-id="18fd2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18fd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18fd2-105">Les identificateurs d'entrée sont créés à l'aide de la structure [EntryID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="18fd2-105">Entry identifiers are constructed with the [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="18fd2-106">La structure **EntryID** est composée d'un indicateur qui décrit les attributs de l'identificateur d'entrée et de l'identificateur d'entrée réel.</span><span class="sxs-lookup"><span data-stu-id="18fd2-106">The **ENTRYID** structure is composed of a flag that describes the attributes of the entry identifier and the actual entry identifier.</span></span> 
  
## <a name="entryid-structure"></a><span data-ttu-id="18fd2-107">Structure ENTRYID</span><span class="sxs-lookup"><span data-stu-id="18fd2-107">ENTRYID Structure</span></span>

<span data-ttu-id="18fd2-108">La structure **EntryID** est définie comme suit:</span><span class="sxs-lookup"><span data-stu-id="18fd2-108">The **ENTRYID** structure is defined as follows:</span></span> 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

<span data-ttu-id="18fd2-109">MAPI_DIM est une constante qui est définie dans le fichier d'en-tête MapiDefs. h.</span><span class="sxs-lookup"><span data-stu-id="18fd2-109">MAPI_DIM is a constant that is defined in the MapiDefs.h header file.</span></span> 
  
<span data-ttu-id="18fd2-110">Le premier octet du membre **abFlags** 4 octets décrit le type et l'utilisation de l'identificateur d'entrée et peut avoir les valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="18fd2-110">The first byte of the 4-byte **abFlags** member describes the type and use of the entry identifier and can have the following values:</span></span> 
  
- <span data-ttu-id="18fd2-111">MAPI_NOTRECI — indique que l'identificateur d'entrée ne peut pas être utilisé comme destinataire sur un message.</span><span class="sxs-lookup"><span data-stu-id="18fd2-111">MAPI_NOTRECI — Indicates the entry identifier cannot be used as a recipient on a message.</span></span>
    
- <span data-ttu-id="18fd2-112">MAPI_NOTRESERVED: indique que les autres utilisateurs ne peuvent pas accéder à l'identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="18fd2-112">MAPI_NOTRESERVED — Indicates that other users cannot access the entry identifier.</span></span>
    
- <span data-ttu-id="18fd2-113">MAPI_NOW: indique que l'identificateur d'entrée ne peut pas être utilisé à d'autres moments.</span><span class="sxs-lookup"><span data-stu-id="18fd2-113">MAPI_NOW — Indicates that the entry identifier cannot be used at other times.</span></span>
    
- <span data-ttu-id="18fd2-114">MAPI_SHORTTERM: indique que l'identificateur d'entrée est à court terme.</span><span class="sxs-lookup"><span data-stu-id="18fd2-114">MAPI_SHORTTERM — Indicates that the entry identifier is short-term.</span></span> <span data-ttu-id="18fd2-115">Toutes les autres valeurs de cet octet doivent être définies sauf si les autres utilisations de l'identificateur d'entrée sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="18fd2-115">All other values in this byte must be set unless other uses of the entry identifier are allowed.</span></span>
    
- <span data-ttu-id="18fd2-116">MAPI_THISSESSION: indique que l'identificateur d'entrée ne peut pas être utilisé pour d'autres sessions.</span><span class="sxs-lookup"><span data-stu-id="18fd2-116">MAPI_THISSESSION — Indicates that the entry identifier cannot be used on other sessions.</span></span>
    
- <span data-ttu-id="18fd2-117">MAPI_NOTRESERVED: indique que l'identificateur d'entrée peut être utilisé par d'autres fournisseurs de services pour d'autres objets.</span><span class="sxs-lookup"><span data-stu-id="18fd2-117">MAPI_NOTRESERVED — Indicates that the entry identifier can be used by other service providers for other objects.</span></span>
    
<span data-ttu-id="18fd2-118">Le membre **AB** des identificateurs d'entrée créés par les fournisseurs de carnet d'adresses et de banque de messages est composé de deux éléments: une structure [MAPIUID](mapiuid.md) à 16 octets qui identifie le fournisseur de services, ainsi qu'un élément permettant d'identifier l'objet.</span><span class="sxs-lookup"><span data-stu-id="18fd2-118">The **ab** member of entry identifiers that is created by address book and message store providers is composed of two pieces: a 16-byte [MAPIUID](mapiuid.md) structure that identifies the service provider, and a piece to identify the object.</span></span> <span data-ttu-id="18fd2-119">**MAPIUID** est une structure qui contient un identificateur global unique, ou GUID.</span><span class="sxs-lookup"><span data-stu-id="18fd2-119">**MAPIUID** is a structure that contains a globally unique identifier, or GUID.</span></span> <span data-ttu-id="18fd2-120">Un GUID est un identificateur indépendant de l'ordre des octets qui peut être créé à l'aide de l'outil de*création de GUID*\* de Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="18fd2-120">A GUID is a byte-order-independent identifier that can be created by using the Microsoft Visual Studio*Create GUID*\* tool.</span></span> 
  
<span data-ttu-id="18fd2-121">Un fournisseur de services enregistre sa structure **MAPIUID** avec MAPI pendant le processus d'ouverture de session dans un appel à la méthode [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) .</span><span class="sxs-lookup"><span data-stu-id="18fd2-121">A service provider registers its **MAPIUID** structure with MAPI during the logon process in a call to the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="18fd2-122">Lorsqu'un client appelle une méthode **OpenEntry** pour accéder à un objet, MAPI utilise la structure **MAPIUID** pour déterminer le fournisseur de services qui peut fournir cet accès.</span><span class="sxs-lookup"><span data-stu-id="18fd2-122">When a client calls an **OpenEntry** method to access an object, MAPI uses the **MAPIUID** structure to determine which service provider can provide that access.</span></span> <span data-ttu-id="18fd2-123">Les fournisseurs de services doivent utiliser la même structure **MAPIUID** pour toutes les versions de leur dll.</span><span class="sxs-lookup"><span data-stu-id="18fd2-123">Service providers should use the same **MAPIUID** structure for all versions of their DLL.</span></span> <span data-ttu-id="18fd2-124">Cela permet aux clients disposant de la version plus récente de répondre aux messages envoyés et enregistrés avec l'ancienne version.</span><span class="sxs-lookup"><span data-stu-id="18fd2-124">This enables clients with the newer version to respond to messages sent and saved with the older version.</span></span> 
  
<span data-ttu-id="18fd2-125">Le reste du membre **AB** après l' **MAPIUID** de 16 octets contient des données binaires spécifiques aux fournisseurs de services pour l'identification d'objets particuliers.</span><span class="sxs-lookup"><span data-stu-id="18fd2-125">The rest of the **ab** member after the 16-byte **MAPIUID** contains service-provider-specific binary data for identifying particular objects.</span></span> <span data-ttu-id="18fd2-126">Il n'existe aucune taille fixe pour cette partie de l'identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="18fd2-126">There is no fixed size for this portion of the entry identifier.</span></span> <span data-ttu-id="18fd2-127">Il peut être de n'importe quelle taille, dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="18fd2-127">It can be any size, within reason.</span></span> <span data-ttu-id="18fd2-128">Un fournisseur de services inclut généralement les informations suivantes dans cette partie de ses identificateurs d'entrée:</span><span class="sxs-lookup"><span data-stu-id="18fd2-128">A service provider typically includes the following information in this part of its entry identifiers:</span></span> 
  
- <span data-ttu-id="18fd2-129">Informations sur la version: étant donné qu'il est courant pour un fournisseur de services de modifier le format de ses identificateurs d'entrée de version à version, le stockage des informations de version permet de déterminer rapidement le déchiffrement de n'importe quel identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="18fd2-129">Version information — Because it is common for a service provider to change the format of its entry identifiers from version to version, storing version information makes it possible to quickly determine how to decipher any entry identifier.</span></span>
    
- <span data-ttu-id="18fd2-130">Informations d'emplacement: les informations d'emplacement sont des données qui donnent à un fournisseur de services un indicateur de la localisation de l'objet représenté par l'identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="18fd2-130">Location information — Location information is data that gives a service provider an indicator of how to locate the object represented by the entry identifier.</span></span> <span data-ttu-id="18fd2-131">Par exemple, un fournisseur de services peut stocker le décalage de disque pour la dernière place d'un fichier de données dans lequel l'objet a été stocké.</span><span class="sxs-lookup"><span data-stu-id="18fd2-131">For example, a service provider can store the disk offset for the last place in a data file that the object was stored.</span></span> <span data-ttu-id="18fd2-132">Étant donné que ce type d'informations peut changer au fil du temps, les fournisseurs de services doivent fournir plusieurs méthodes pour rechercher des objets dans leurs identificateurs d'entrée.</span><span class="sxs-lookup"><span data-stu-id="18fd2-132">Because this type of information can change over time, service providers should provide multiple ways for locating objects in their entry identifiers.</span></span>
    
<span data-ttu-id="18fd2-133">Bien que les fournisseurs de services puissent recycler leurs identificateurs d'entrée, ils doivent éviter cette pratique.</span><span class="sxs-lookup"><span data-stu-id="18fd2-133">Although service providers can recycle their entry identifiers, they should avoid this practice.</span></span> <span data-ttu-id="18fd2-134">S'il est nécessaire de réutiliser un identificateur d'entrée, les fournisseurs de services doivent prendre la période qui s'écoule entre l'utilisation initiale et la réutilisation aussi longtemps que possible.</span><span class="sxs-lookup"><span data-stu-id="18fd2-134">If it is necessary to reuse an entry identifier, service providers should make the time period that elapses between the initial use and the reuse as long as possible.</span></span> <span data-ttu-id="18fd2-135">De plus, l'identificateur d'entrée doit être réattribué à un autre objet du même type.</span><span class="sxs-lookup"><span data-stu-id="18fd2-135">Also, the entry identifier should be reassigned to another object of the same type.</span></span> <span data-ttu-id="18fd2-136">Autrement dit, un identificateur d'entrée particulier ne doit pas être associé d'abord à un message, puis à un dossier.</span><span class="sxs-lookup"><span data-stu-id="18fd2-136">That is, a particular entry identifier should not be associated first with a message and then with a folder.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="18fd2-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18fd2-137">See also</span></span>



[<span data-ttu-id="18fd2-138">Identificateurs d'entrée MAPI</span><span class="sxs-lookup"><span data-stu-id="18fd2-138">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

