---
title: Construction d’identificateurs d’entrée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 1d38c0ac7ddbd24123dd51d7315644f3ad786d15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783053"
---
# <a name="constructing-entry-identifiers"></a><span data-ttu-id="f012a-103">Construction d’identificateurs d’entrée</span><span class="sxs-lookup"><span data-stu-id="f012a-103">Constructing Entry Identifiers</span></span>

  
  
<span data-ttu-id="f012a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f012a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f012a-105">Identificateurs d’entrée sont construits avec la structure [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="f012a-105">Entry identifiers are constructed with the [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="f012a-106">La structure de la **propriété ENTRYID** est composée d’un indicateur qui décrit les attributs de l’identificateur d’entrée et de l’identificateur d’entrée réelle.</span><span class="sxs-lookup"><span data-stu-id="f012a-106">The **ENTRYID** structure is composed of a flag that describes the attributes of the entry identifier and the actual entry identifier.</span></span> 
  
## <a name="entryid-structure"></a><span data-ttu-id="f012a-107">Propriété ENTRYID Structure</span><span class="sxs-lookup"><span data-stu-id="f012a-107">ENTRYID Structure</span></span>

<span data-ttu-id="f012a-108">La structure de la **propriété ENTRYID** est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="f012a-108">The **ENTRYID** structure is defined as follows:</span></span> 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

<span data-ttu-id="f012a-109">MAPI_DIM est une constante qui est définie dans le fichier d’en-tête MapiDefs.h.</span><span class="sxs-lookup"><span data-stu-id="f012a-109">MAPI_DIM is a constant that is defined in the MapiDefs.h header file.</span></span> 
  
<span data-ttu-id="f012a-110">Le premier octet du membre 4 octets **abFlags** décrit le type et utilisation de l’identificateur d’entrée et peut avoir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f012a-110">The first byte of the 4-byte **abFlags** member describes the type and use of the entry identifier and can have the following values:</span></span> 
  
- <span data-ttu-id="f012a-111">MAPI_NOTRECI — Indique l’identificateur d’entrée ne peut pas être utilisé en tant que destinataire d’un message.</span><span class="sxs-lookup"><span data-stu-id="f012a-111">MAPI_NOTRECI — Indicates the entry identifier cannot be used as a recipient on a message.</span></span>
    
- <span data-ttu-id="f012a-112">MAPI_NOTRESERVED — Indique que les autres utilisateurs ne peuvent pas accéder à l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f012a-112">MAPI_NOTRESERVED — Indicates that other users cannot access the entry identifier.</span></span>
    
- <span data-ttu-id="f012a-113">MAPI_NOW — Indique que l’identificateur d’entrée ne peut pas être utilisé à d’autres moments.</span><span class="sxs-lookup"><span data-stu-id="f012a-113">MAPI_NOW — Indicates that the entry identifier cannot be used at other times.</span></span>
    
- <span data-ttu-id="f012a-114">MAPI_SHORTTERM — Indique que l’identificateur d’entrée est à court terme.</span><span class="sxs-lookup"><span data-stu-id="f012a-114">MAPI_SHORTTERM — Indicates that the entry identifier is short-term.</span></span> <span data-ttu-id="f012a-115">Toutes les autres valeurs dans cet octet doivent être définies à moins que les autres utilisations de l’identificateur d’entrée sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="f012a-115">All other values in this byte must be set unless other uses of the entry identifier are allowed.</span></span>
    
- <span data-ttu-id="f012a-116">MAPI_THISSESSION — Indique que l’identificateur d’entrée ne peut pas être utilisé sur d’autres sessions.</span><span class="sxs-lookup"><span data-stu-id="f012a-116">MAPI_THISSESSION — Indicates that the entry identifier cannot be used on other sessions.</span></span>
    
- <span data-ttu-id="f012a-117">MAPI_NOTRESERVED — Indique que l’identificateur d’entrée peut être utilisée par les autres fournisseurs de services pour d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="f012a-117">MAPI_NOTRESERVED — Indicates that the entry identifier can be used by other service providers for other objects.</span></span>
    
<span data-ttu-id="f012a-118">Le membre de **Carnet d’adresses** d’identificateurs d’entrée qui est créé par les fournisseurs de banque de messages et du carnet d’adresse est composé de deux parties : une structure [MAPIUID](mapiuid.md) de 16 octets qui identifie le fournisseur de services et un élément pour identifier l’objet.</span><span class="sxs-lookup"><span data-stu-id="f012a-118">The **ab** member of entry identifiers that is created by address book and message store providers is composed of two pieces: a 16-byte [MAPIUID](mapiuid.md) structure that identifies the service provider, and a piece to identify the object.</span></span> <span data-ttu-id="f012a-119">**MAPIUID** est une structure qui contient un identificateur global unique, ou le GUID.</span><span class="sxs-lookup"><span data-stu-id="f012a-119">**MAPIUID** is a structure that contains a globally unique identifier, or GUID.</span></span> <span data-ttu-id="f012a-120">Un GUID est un identificateur indépendant de l’ordre octets qui peut être créé à l’aide de Microsoft Visual Studio*Create GUID*\* outil.</span><span class="sxs-lookup"><span data-stu-id="f012a-120">A GUID is a byte-order-independent identifier that can be created by using the Microsoft Visual Studio*Create GUID*\* tool.</span></span> 
  
<span data-ttu-id="f012a-121">Un fournisseur de services enregistre sa structure **MAPIUID** MAPI au cours du processus d’ouverture de session dans un appel à la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) .</span><span class="sxs-lookup"><span data-stu-id="f012a-121">A service provider registers its **MAPIUID** structure with MAPI during the logon process in a call to the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="f012a-122">Lorsqu’un client appelle une méthode **OpenEntry** pour accéder à un objet, MAPI utilise la structure **MAPIUID** pour déterminer quel service fournisseur peut fournir cet accès.</span><span class="sxs-lookup"><span data-stu-id="f012a-122">When a client calls an **OpenEntry** method to access an object, MAPI uses the **MAPIUID** structure to determine which service provider can provide that access.</span></span> <span data-ttu-id="f012a-123">Fournisseurs de services doivent utiliser la même structure **MAPIUID** pour toutes les versions de leur DLL.</span><span class="sxs-lookup"><span data-stu-id="f012a-123">Service providers should use the same **MAPIUID** structure for all versions of their DLL.</span></span> <span data-ttu-id="f012a-124">Cela permet aux clients avec la version la plus récente répondre aux messages envoyés et enregistré avec la version antérieure.</span><span class="sxs-lookup"><span data-stu-id="f012a-124">This enables clients with the newer version to respond to messages sent and saved with the older version.</span></span> 
  
<span data-ttu-id="f012a-125">Le reste du membre **ab** après le 16 octets **MAPIUID** contient des données binaires spécifique au fournisseur de service pour identifier des objets particulières.</span><span class="sxs-lookup"><span data-stu-id="f012a-125">The rest of the **ab** member after the 16-byte **MAPIUID** contains service-provider-specific binary data for identifying particular objects.</span></span> <span data-ttu-id="f012a-126">Il n’existe aucune taille fixe pour cette partie de l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f012a-126">There is no fixed size for this portion of the entry identifier.</span></span> <span data-ttu-id="f012a-127">Il peut être n’importe quelle taille, dans le motif.</span><span class="sxs-lookup"><span data-stu-id="f012a-127">It can be any size, within reason.</span></span> <span data-ttu-id="f012a-128">En règle générale, un fournisseur de services comprend les informations suivantes dans cette partie de son identificateur d’entrée :</span><span class="sxs-lookup"><span data-stu-id="f012a-128">A service provider typically includes the following information in this part of its entry identifiers:</span></span> 
  
- <span data-ttu-id="f012a-129">Informations de version, car il est courant pour un fournisseur de services modifier le format de son identificateur d’entrée pour chaque version, le stockage des informations de version permet de déterminer rapidement comment déchiffrer un identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f012a-129">Version information — Because it is common for a service provider to change the format of its entry identifiers from version to version, storing version information makes it possible to quickly determine how to decipher any entry identifier.</span></span>
    
- <span data-ttu-id="f012a-130">Informations d’emplacement, informations d’emplacement sont des données qui permet à un fournisseur de services indique comment localiser l’objet représenté par l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f012a-130">Location information — Location information is data that gives a service provider an indicator of how to locate the object represented by the entry identifier.</span></span> <span data-ttu-id="f012a-131">Par exemple, un fournisseur de services peut stocker le disque décalage du dernier lieu dans un fichier de données que l’objet a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="f012a-131">For example, a service provider can store the disk offset for the last place in a data file that the object was stored.</span></span> <span data-ttu-id="f012a-132">Car ce type d’informations peut changer au fil du temps, les fournisseurs de services doivent fournir plusieurs façons pour localiser des objets dans leurs identificateurs d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f012a-132">Because this type of information can change over time, service providers should provide multiple ways for locating objects in their entry identifiers.</span></span>
    
<span data-ttu-id="f012a-133">Bien que les fournisseurs de services peuvent recycler leurs identificateurs d’entrée, ils doivent éviter cette pratique.</span><span class="sxs-lookup"><span data-stu-id="f012a-133">Although service providers can recycle their entry identifiers, they should avoid this practice.</span></span> <span data-ttu-id="f012a-134">S’il est nécessaire réutiliser un identificateur d’entrée, les fournisseurs de services procèdent à la période de temps qui s’écoule entre la première utilisation et la réutilisation dès que possible.</span><span class="sxs-lookup"><span data-stu-id="f012a-134">If it is necessary to reuse an entry identifier, service providers should make the time period that elapses between the initial use and the reuse as long as possible.</span></span> <span data-ttu-id="f012a-135">En outre, l’identificateur d’entrée doit être réaffecté à un autre objet du même type.</span><span class="sxs-lookup"><span data-stu-id="f012a-135">Also, the entry identifier should be reassigned to another object of the same type.</span></span> <span data-ttu-id="f012a-136">Autrement dit, un identificateur d’entrée particulier ne doit pas être associé à tout d’abord avec un message, puis avec un dossier.</span><span class="sxs-lookup"><span data-stu-id="f012a-136">That is, a particular entry identifier should not be associated first with a message and then with a folder.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f012a-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f012a-137">See also</span></span>



[<span data-ttu-id="f012a-138">Identificateurs d’entrée MAPI</span><span class="sxs-lookup"><span data-stu-id="f012a-138">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

