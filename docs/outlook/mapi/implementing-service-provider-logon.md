---
title: Implémentation d’une ouverture de session de fournisseur de services
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 533c00a0c994e7dfc5adc476899553bc39a2a9ab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401642"
---
# <a name="implementing-service-provider-logon"></a><span data-ttu-id="3bafe-103">Implémentation d’une ouverture de session de fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="3bafe-103">Implementing Service Provider Logon</span></span>

<span data-ttu-id="3bafe-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bafe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bafe-105">MAPI appelle une méthode dans votre objet de fournisseur pour commencer le processus d’ouverture de session en utilisant le pointeur vous renvoyez à partir de la fonction de point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3bafe-105">MAPI calls a method in your provider object to begin the logon process by using the pointer that you return from your entry point function.</span></span> <span data-ttu-id="3bafe-106">La méthode varie comme suit, en fonction du type de votre fournisseur de services :</span><span class="sxs-lookup"><span data-stu-id="3bafe-106">The method varies as follows, depending on the type of your service provider:</span></span>
  
- <span data-ttu-id="3bafe-107">[IABProvider::Logon](iabprovider-logon.md) pour les fournisseurs de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="3bafe-107">[IABProvider::Logon](iabprovider-logon.md) for address book providers</span></span> 
    
- <span data-ttu-id="3bafe-108">[IMSProvider::Logon](imsprovider-logon.md) pour les fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="3bafe-108">[IMSProvider::Logon](imsprovider-logon.md) for message store providers</span></span> 
    
- <span data-ttu-id="3bafe-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) pour les fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="3bafe-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) for transport providers</span></span> 
    
<span data-ttu-id="3bafe-110">Effectuer les tâches suivantes dans n’importe quelle méthode d’ouverture de session vous implémentez :</span><span class="sxs-lookup"><span data-stu-id="3bafe-110">Perform the following tasks in whatever logon method you implement:</span></span>
  
1. <span data-ttu-id="3bafe-111">Incrémente le décompte de références sur l’objet de prise en charge qui est passé comme paramètre d’entrée en appelant la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3bafe-111">Increment the reference count on the support object that is passed as an input parameter by calling its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> 
    
2. <span data-ttu-id="3bafe-112">Appeler la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) de l’objet de la prise en charge pour accéder à la section de profil.</span><span class="sxs-lookup"><span data-stu-id="3bafe-112">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your profile section.</span></span> 
    
3. <span data-ttu-id="3bafe-113">Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de la section profil pour définir les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="3bafe-113">Call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set the following properties:</span></span> 
    
  - <span data-ttu-id="3bafe-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3bafe-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
  - <span data-ttu-id="3bafe-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3bafe-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
  - <span data-ttu-id="3bafe-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3bafe-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
  - <span data-ttu-id="3bafe-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3bafe-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="3bafe-118">N’essayez pas de définir les propriétés **PR_RESOURCE_FLAGS** ou **PR_PROVIDER_DLL_NAME** de la section profil.</span><span class="sxs-lookup"><span data-stu-id="3bafe-118">Do not attempt to set the profile section's **PR_RESOURCE_FLAGS** or **PR_PROVIDER_DLL_NAME** properties.</span></span> <span data-ttu-id="3bafe-119">Au moment de l’ouverture de session, ces propriétés sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3bafe-119">At logon time, these properties are read-only.</span></span> 
  
4. <span data-ttu-id="3bafe-120">Vérifiez que les propriétés que vous avez besoin pour la configuration sont stockées soit dans le profil ou qui sont disponibles à partir de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3bafe-120">Check that the properties you need for configuration are either stored in the profile or are available from the user.</span></span> <span data-ttu-id="3bafe-121">Pour plus d’informations sur la vérification de votre configuration, voir [Configuration du fournisseur de Service de vérification](verifying-service-provider-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="3bafe-121">For more information about checking your configuration, see [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).</span></span>
    
5. <span data-ttu-id="3bafe-122">Appelez la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) de l’objet de la prise en charge pour inscrire un identificateur unique, ou [MAPIUID](mapiuid.md), si votre fournisseur est un fournisseur de magasin de message ou de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="3bafe-122">Call the support object's [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md), if your provider is an address book or message store provider.</span></span> <span data-ttu-id="3bafe-123">Fournisseurs de transport inscrire **MAPIUID** structures lors de leur méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) des appels MAPI.</span><span class="sxs-lookup"><span data-stu-id="3bafe-123">Transport providers register **MAPIUID** structures when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="3bafe-124">Pour plus d’informations sur l’inscription d’un **MAPIUID**, voir [Inscription des identificateurs uniques Service fournisseur](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="3bafe-124">For more information about registering a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
    
6. <span data-ttu-id="3bafe-125">Instancier un objet d’ouverture de session et retourner avec une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3bafe-125">Instantiate a logon object and return with one of the following values:</span></span>
    
  - <span data-ttu-id="3bafe-126">S_OK pour indiquer une ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="3bafe-126">S_OK to indicate a successful logon.</span></span>
    
  - <span data-ttu-id="3bafe-127">MAPI_E_UNCONFIGURED pour indiquer qu’une ou plusieurs des propriétés de configuration n’étaient pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="3bafe-127">MAPI_E_UNCONFIGURED to indicate that one or more of the configuration properties were unavailable.</span></span>
    
  - <span data-ttu-id="3bafe-128">MAPI_E_USER_CANCEL pour indiquer que l’utilisateur a annulé la boîte de dialogue de configuration à l’origine des propriétés de configuration afin de ne pas être disponible.</span><span class="sxs-lookup"><span data-stu-id="3bafe-128">MAPI_E_USER_CANCEL to indicate that the user canceled the configuration dialog box, causing configuration properties to be unavailable.</span></span>
    
  - <span data-ttu-id="3bafe-129">Référence à MAPI_E_FAILONEPROVIDER pour indiquer que votre fournisseur ne peut pas être configuré, mais que MAPI doit autoriser qu’il soit utilisé ou non.</span><span class="sxs-lookup"><span data-stu-id="3bafe-129">MAPI_E_FAILONEPROVIDER to indicate that your provider could not be configured, but that MAPI should allow it to be used regardless.</span></span> <span data-ttu-id="3bafe-130">Méthodes d’ouverture de session doivent renvoyer cette valeur pour signaler une erreur récupérable, telles que lorsque le fournisseur exige un mot de passe et ne peut pas demander à l’utilisateur pour qu’il parce que l’interface utilisateur est désactivée.</span><span class="sxs-lookup"><span data-stu-id="3bafe-130">Logon methods should return this value to report a nonfatal error, such as when the provider requires a password and cannot prompt the user for it because the user interface is disabled.</span></span> 
    
<span data-ttu-id="3bafe-131">La liste des tâches ci-dessus décrit une implémentation minimale pour une méthode de connexion de fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="3bafe-131">The preceding list of tasks describes a minimum implementation for a service provider logon method.</span></span> <span data-ttu-id="3bafe-132">Vous pouvez inclure des fonctionnalités supplémentaires, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3bafe-132">You can include additional functionality, if necessary.</span></span> <span data-ttu-id="3bafe-133">Par exemple, certains fournisseurs appeler [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) pour mettre à jour la table d’état dans leur méthode d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="3bafe-133">For example, some providers call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) to update the status table in their logon method.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3bafe-134">Pour optimiser les performances au moment de l’ouverture de session, évitez d’appeler [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) ou [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span><span class="sxs-lookup"><span data-stu-id="3bafe-134">To achieve the best performance at logon time, avoid calling either [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) or [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span></span> <span data-ttu-id="3bafe-135">Avant de ces appels peuvent effectuer et retourner le contrôle à votre méthode d’ouverture de session, le spouleur MAPI doit être démarré.</span><span class="sxs-lookup"><span data-stu-id="3bafe-135">Before these calls can complete and return control to your logon method, the MAPI spooler must be started.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3bafe-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bafe-136">See also</span></span>

- [<span data-ttu-id="3bafe-137">Démarrage d’un fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="3bafe-137">Starting a Service Provider</span></span>](starting-a-service-provider.md)

