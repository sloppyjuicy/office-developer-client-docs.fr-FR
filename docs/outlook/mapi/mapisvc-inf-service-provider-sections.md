---
title: Sections du fournisseur de services MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ea192ec6356cc3b929bf8379567144d3a54223f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405561"
---
# <a name="mapisvcinf-service-provider-sections"></a><span data-ttu-id="7f6eb-103">Sections du fournisseur de services MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="7f6eb-103">MapiSvc.inf Service Provider Sections</span></span>

<span data-ttu-id="7f6eb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f6eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f6eb-105">Mapisvc.inf comprend une section de fournisseur de services pour chacune des **entrées** répertoriées dans l’entrée Fournisseurs de la section services de messagerie précédente.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-105">Mapisvc.inf includes one service provider section for each of the entries listed in the **Providers** entry in the preceding message services section.</span></span> <span data-ttu-id="7f6eb-106">**Les** sections du fournisseur de services sont similaires aux sections de service de messagerie, dans la sorte que les deux types de sections contiennent des entrées de ce format :</span><span class="sxs-lookup"><span data-stu-id="7f6eb-106">**Service** provider sections are similar to message service sections in that both types of sections contain entries in this format:</span></span> 
  
<span data-ttu-id="7f6eb-107">**balise de propriété** = valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="7f6eb-107">**property tag** = property value</span></span> 
  
<span data-ttu-id="7f6eb-108">Toutefois, les sections du fournisseur de services et les sections de service de messagerie diffèrent dans le fait que ces entrées de propriété sont le seul type d’entrée inclus dans les sections du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-108">However, service provider sections and message service sections differ in that such property entries are the only type of entry included in service provider sections.</span></span> <span data-ttu-id="7f6eb-109">Il ne peut pas y avoir de sections supplémentaires ou liées pour les fournisseurs de services ; Toutes les informations du fournisseur de services doivent être contenues dans la même section.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-109">There can be no additional or linked sections for service providers; all service provider information must be contained within the one section.</span></span> 
  
<span data-ttu-id="7f6eb-110">Certaines des propriétés définies dans les sections du service de messagerie sont également définies dans les sections du fournisseur de services, car ces propriétés sont logiques pour les deux.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-110">Some of the properties set in message service sections are also set in service provider sections because these properties make sense for both.</span></span> <span data-ttu-id="7f6eb-111">La **propriété PR_DISPLAY_NAME** est un exemple.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-111">The **PR_DISPLAY_NAME** property is an example.</span></span> <span data-ttu-id="7f6eb-112">Les fournisseurs de services et les services de messagerie ont un nom qui est utilisé pour l’affichage dans l’interface utilisateur de configuration.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-112">Both service providers and message services have a name that is used for display in the configuration user interface.</span></span> <span data-ttu-id="7f6eb-113">Selon le fournisseur de services, ce nom peut ou non être identique.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-113">Depending on the service provider, that name may or may not be the same.</span></span> <span data-ttu-id="7f6eb-114">D’autres propriétés sont spécifiques aux fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-114">Other properties are specific to service providers.</span></span> 
  
<span data-ttu-id="7f6eb-115">Les sections des fournisseurs de services classiques incluent les entrées suivantes, qui sont toutes requises :</span><span class="sxs-lookup"><span data-stu-id="7f6eb-115">Typical service provider sections include the following entries, all of which are required:</span></span>
  
<span data-ttu-id="7f6eb-116">**PR_DISPLAY_NAME**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="7f6eb-116">**PR_DISPLAY_NAME** =  _string_</span></span>
  
<span data-ttu-id="7f6eb-117">**PR_PROVIDER_DISPLAY**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="7f6eb-117">**PR_PROVIDER_DISPLAY** =  _string_</span></span>
  
<span data-ttu-id="7f6eb-118">**PR_PROVIDER_DLL_NAME**  =   _nom du fichier DLL_</span><span class="sxs-lookup"><span data-stu-id="7f6eb-118">**PR_PROVIDER_DLL_NAME** =  _name of DLL file_</span></span>
  
<span data-ttu-id="7f6eb-119">**PR_RESOURCE_TYPE**  =   _long_</span><span class="sxs-lookup"><span data-stu-id="7f6eb-119">**PR_RESOURCE_TYPE** =  _long_</span></span>
  
<span data-ttu-id="7f6eb-120">**PR_RESOURCE_FLAGS**  =   _masque de bits_</span><span class="sxs-lookup"><span data-stu-id="7f6eb-120">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="7f6eb-121">**L PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) est similaire à celle **PR_SERVICE_DLL_NAME**; il indique le nom de fichier de la DLL qui contient le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-121">The **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) entry is similar to **PR_SERVICE_DLL_NAME**; it indicates the filename for the DLL that contains the service provider.</span></span> <span data-ttu-id="7f6eb-122">Le code du service de messagerie peut être stocké avec l’un de ses fournisseurs de services dans le même fichier DLL ou exister en tant que DLL distincte.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-122">Message service code may be stored with one of its service providers in the same DLL file or exist as a separate DLL.</span></span> <span data-ttu-id="7f6eb-123">Notez qu’aucun suffixe n’est inclus dans l’entrée, quelle que soit la plateforme cible . MAPI s’occupe de l’ajout d’un suffixe si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-123">Note that no suffix is included in the entry regardless of the target platform; MAPI takes care of adding a suffix if necessary.</span></span> 
  
<span data-ttu-id="7f6eb-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) représente le type de fournisseur de services ; les fournisseurs de services le définissent sur la constante prédéfinée appropriée.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) entry represents the type of service provider; service providers set it to the appropriate predefined constant.</span></span> <span data-ttu-id="7f6eb-125">Les valeurs valides sont MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER et MAPI_AB_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-125">Valid values include MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER, and MAPI_AB_PROVIDER.</span></span>
  
<span data-ttu-id="7f6eb-126">Une autre entrée de propriété qui s’applique à la fois aux services de messagerie et aux fournisseurs de services, l’entrée **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) indique les options.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-126">Another property entry that applies to both message services and service providers, the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry indicates options.</span></span> <span data-ttu-id="7f6eb-127">Les paramètres de cette entrée de propriété peuvent varier en fonction du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-127">The settings for this property entry can differ depending on the service provider.</span></span> <span data-ttu-id="7f6eb-128">Par exemple, certains fournisseurs de magasins de messages peuvent définir PR_RESOURCE_FLAGS **sur** STATUS_NO_DEFAULT_STORE s’ils ne peuvent jamais fonctionner en tant que magasin de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-128">For example, some message store providers might set **PR_RESOURCE_FLAGS** to STATUS_NO_DEFAULT_STORE if they can never operate as the default message store.</span></span> 
  
<span data-ttu-id="7f6eb-129">Voici trois exemples de sections sur les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-129">Three examples of service provider sections follow.</span></span> <span data-ttu-id="7f6eb-130">La section **[Fournisseur AB]** est la section du fournisseur de services pour le service de carnet d’adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-130">The **[AB Provider]** section is the service provider section for the Default Address Book service.</span></span> <span data-ttu-id="7f6eb-131">Les **sections [MsgService Prov1]** et **[MsgService Prov2]** appartiennent à Mon propre service ; La première est une section de fournisseur de carnet d’adresses et la seconde est une section de fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="7f6eb-131">The **[MsgService Prov1]** and **[MsgService Prov2]** sections belong to My Own Service; the first is an address-book provider section and the second is a message-store provider section.</span></span> 
  
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


