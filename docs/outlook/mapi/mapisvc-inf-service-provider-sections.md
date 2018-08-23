---
title: Sections de fournisseur de services MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 05666d8d6b7279588b4b442151640fa1696aedda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586780"
---
# <a name="mapisvcinf-service-provider-sections"></a><span data-ttu-id="bd415-103">Sections de fournisseur de services MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="bd415-103">MapiSvc.inf Service Provider Sections</span></span>

<span data-ttu-id="bd415-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd415-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd415-105">MAPISVC.inf comprend une section de fournisseur de service pour chacune des entrées répertoriées dans l’entrée de **fournisseurs** dans la section services de message précédente.</span><span class="sxs-lookup"><span data-stu-id="bd415-105">Mapisvc.inf includes one service provider section for each of the entries listed in the **Providers** entry in the preceding message services section.</span></span> <span data-ttu-id="bd415-106">Sections de fournisseur de **service** sont similaires aux sections de service de message dans la mesure où les deux types de sections contiennent des entrées dans ce format :</span><span class="sxs-lookup"><span data-stu-id="bd415-106">**Service** provider sections are similar to message service sections in that both types of sections contain entries in this format:</span></span> 
  
<span data-ttu-id="bd415-107">**balise de propriété** = valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bd415-107">**property tag** = property value</span></span> 
  
<span data-ttu-id="bd415-108">Toutefois, les sections de fournisseur de service et message service diffèrent dans la mesure où ces entrées de propriété sont le seul type d’entrée inclus dans les sections de fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="bd415-108">However, service provider sections and message service sections differ in that such property entries are the only type of entry included in service provider sections.</span></span> <span data-ttu-id="bd415-109">Il ne peut y avoir aucune section liées ou supplémentaires pour les fournisseurs de service ; toutes les informations de fournisseur de service doivent être contenues dans la section.</span><span class="sxs-lookup"><span data-stu-id="bd415-109">There can be no additional or linked sections for service providers; all service provider information must be contained within the one section.</span></span> 
  
<span data-ttu-id="bd415-110">Certaines des propriétés définies dans les sections de service de message sont également définies dans les sections de fournisseur de service, car ces propriétés pour les deux sens.</span><span class="sxs-lookup"><span data-stu-id="bd415-110">Some of the properties set in message service sections are also set in service provider sections because these properties make sense for both.</span></span> <span data-ttu-id="bd415-111">La propriété **PR_DISPLAY_NAME** est un exemple.</span><span class="sxs-lookup"><span data-stu-id="bd415-111">The **PR_DISPLAY_NAME** property is an example.</span></span> <span data-ttu-id="bd415-112">Fournisseurs de services et de services de messagerie ont un nom qui est utilisé pour l’affichage dans l’interface utilisateur de configuration.</span><span class="sxs-lookup"><span data-stu-id="bd415-112">Both service providers and message services have a name that is used for display in the configuration user interface.</span></span> <span data-ttu-id="bd415-113">Selon le fournisseur de services, ce nom peut ou ne peut pas être la même.</span><span class="sxs-lookup"><span data-stu-id="bd415-113">Depending on the service provider, that name may or may not be the same.</span></span> <span data-ttu-id="bd415-114">Autres propriétés sont spécifiques aux fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="bd415-114">Other properties are specific to service providers.</span></span> 
  
<span data-ttu-id="bd415-115">Sections de fournisseur de service par défaut sont les entrées suivantes, qui sont nécessaires :</span><span class="sxs-lookup"><span data-stu-id="bd415-115">Typical service provider sections include the following entries, all of which are required:</span></span>
  
<span data-ttu-id="bd415-116">**PR_DISPLAY_NAME** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="bd415-116">**PR_DISPLAY_NAME** =  _string_</span></span>
  
<span data-ttu-id="bd415-117">**PR_PROVIDER_DISPLAY** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="bd415-117">**PR_PROVIDER_DISPLAY** =  _string_</span></span>
  
<span data-ttu-id="bd415-118">**PR_PROVIDER_DLL_NAME** =  _nom de fichier DLL_</span><span class="sxs-lookup"><span data-stu-id="bd415-118">**PR_PROVIDER_DLL_NAME** =  _name of DLL file_</span></span>
  
<span data-ttu-id="bd415-119">**PR_RESOURCE_TYPE** =  _long_</span><span class="sxs-lookup"><span data-stu-id="bd415-119">**PR_RESOURCE_TYPE** =  _long_</span></span>
  
<span data-ttu-id="bd415-120">**PR_RESOURCE_FLAGS** =  _masque de bits_</span><span class="sxs-lookup"><span data-stu-id="bd415-120">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="bd415-121">L’entrée **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) est similaire à **PR_SERVICE_DLL_NAME**; Il indique le nom de fichier de la DLL qui contient le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="bd415-121">The **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) entry is similar to **PR_SERVICE_DLL_NAME**; it indicates the filename for the DLL that contains the service provider.</span></span> <span data-ttu-id="bd415-122">Code de service de message peut être stocké avec l’un de ses fournisseurs de service dans le même fichier DLL ou exister en tant qu’une DLL distincte.</span><span class="sxs-lookup"><span data-stu-id="bd415-122">Message service code may be stored with one of its service providers in the same DLL file or exist as a separate DLL.</span></span> <span data-ttu-id="bd415-123">Notez qu’aucun suffixe n’est incluse dans l’entrée indépendamment de la plateforme cible ; MAPI prend en charge de l’ajout d’un suffixe si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bd415-123">Note that no suffix is included in the entry regardless of the target platform; MAPI takes care of adding a suffix if necessary.</span></span> 
  
<span data-ttu-id="bd415-124">**PR_RESOURCE_TYPE** Entrée ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) représente le type de fournisseur de services ; fournisseurs de services de lui attribuer la constante prédéfinie appropriée.</span><span class="sxs-lookup"><span data-stu-id="bd415-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) entry represents the type of service provider; service providers set it to the appropriate predefined constant.</span></span> <span data-ttu-id="bd415-125">Les valeurs valides sont MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER et MAPI_AB_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="bd415-125">Valid values include MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER, and MAPI_AB_PROVIDER.</span></span>
  
<span data-ttu-id="bd415-126">Une autre entrée de propriété s’applique aux services de messagerie et de fournisseurs de services, l’entrée **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) indique les options.</span><span class="sxs-lookup"><span data-stu-id="bd415-126">Another property entry that applies to both message services and service providers, the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry indicates options.</span></span> <span data-ttu-id="bd415-127">Les paramètres d’entrée de cette propriété peuvent être différente selon le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="bd415-127">The settings for this property entry can differ depending on the service provider.</span></span> <span data-ttu-id="bd415-128">Par exemple, certains fournisseurs de banque de message peuvent définir **PR_RESOURCE_FLAGS** à STATUS_NO_DEFAULT_STORE si elles ne peuvent jamais fonctionner en tant que la banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="bd415-128">For example, some message store providers might set **PR_RESOURCE_FLAGS** to STATUS_NO_DEFAULT_STORE if they can never operate as the default message store.</span></span> 
  
<span data-ttu-id="bd415-129">Suivent de trois exemples de sections de fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="bd415-129">Three examples of service provider sections follow.</span></span> <span data-ttu-id="bd415-130">La section **[Fournisseur AB]** est la section de fournisseur de service pour le service de carnet d’adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="bd415-130">The **[AB Provider]** section is the service provider section for the Default Address Book service.</span></span> <span data-ttu-id="bd415-131">Les sections **[MsgService Prov1]** et **[MsgService Prov2]** appartiennent à mon Service propre ; le premier est une section de fournisseur de carnet d’adresses et le second est une section de fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="bd415-131">The **[MsgService Prov1]** and **[MsgService Prov2]** sections belong to My Own Service; the first is an address-book provider section and the second is a message-store provider section.</span></span> 
  
```cpp
[AB Provider]
PR_DISPLAY_NAME=Default Address Book
PR_PROVIDER_DISPLAY=Default Address Book
PR_PROVIDER_DLL_NAME=AB.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
6600001e=C:\WINNT35\System32\DEFAB.TXT
[MsgService Prov1]
PR_DISPLAY_NAME=My Own Service
PR_PROVIDER_DISPLAY=My Own Address Book
PR_PROVIDER_DLL_NAME=MYXXX.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
[MsgService Prov2]
PR_DISPLAY_NAME=My Folders
PR_PROVIDER_DISPLAY=My Own Message Store
PR_RESOURCE_TYPE=MAPI_STORE_PROVIDER
PR_PROVIDER_DLL_NAME=MYZZZ.DLL
PR_RESOURCE_FLAGS=STATUS_NO_DEFAULT_STORE
66060003=00000000
66030003=00000000
34140102=78b2fa70aff711cd9bc800aa002fc45a
66090003=06000000
660A0003=03000000

```


