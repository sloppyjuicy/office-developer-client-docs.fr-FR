---
title: Implémentation de la connexion au fournisseur de services
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 533c00a0c994e7dfc5adc476899553bc39a2a9ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310086"
---
# <a name="implementing-service-provider-logon"></a><span data-ttu-id="a154b-103">Implémentation de la connexion au fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="a154b-103">Implementing Service Provider Logon</span></span>

<span data-ttu-id="a154b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a154b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a154b-105">MAPI appelle une méthode dans votre objet fournisseur pour commencer le processus d'ouverture de session à l'aide du pointeur que vous avez renvoyé à partir de votre fonction de point d'entrée.</span><span class="sxs-lookup"><span data-stu-id="a154b-105">MAPI calls a method in your provider object to begin the logon process by using the pointer that you return from your entry point function.</span></span> <span data-ttu-id="a154b-106">La méthode varie, selon le type de votre fournisseur de services:</span><span class="sxs-lookup"><span data-stu-id="a154b-106">The method varies as follows, depending on the type of your service provider:</span></span>
  
- <span data-ttu-id="a154b-107">[IABProvider:: Logon](iabprovider-logon.md) pour les fournisseurs de carnet d'adresses</span><span class="sxs-lookup"><span data-stu-id="a154b-107">[IABProvider::Logon](iabprovider-logon.md) for address book providers</span></span> 
    
- <span data-ttu-id="a154b-108">[IMSProvider:: Logon](imsprovider-logon.md) pour les fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="a154b-108">[IMSProvider::Logon](imsprovider-logon.md) for message store providers</span></span> 
    
- <span data-ttu-id="a154b-109">[IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) pour les fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="a154b-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) for transport providers</span></span> 
    
<span data-ttu-id="a154b-110">Effectuez les tâches suivantes dans la méthode de connexion que vous implémentez:</span><span class="sxs-lookup"><span data-stu-id="a154b-110">Perform the following tasks in whatever logon method you implement:</span></span>
  
1. <span data-ttu-id="a154b-111">Incrémentez le décompte de références sur l'objet de prise en charge qui est passé en tant que paramètre d'entrée en appelant sa méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a154b-111">Increment the reference count on the support object that is passed as an input parameter by calling its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> 
    
2. <span data-ttu-id="a154b-112">Appelez la méthode [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) de l'objet de prise en charge pour accéder à votre section de profil.</span><span class="sxs-lookup"><span data-stu-id="a154b-112">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your profile section.</span></span> 
    
3. <span data-ttu-id="a154b-113">Appelez la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) de la section profile pour définir les propriétés suivantes:</span><span class="sxs-lookup"><span data-stu-id="a154b-113">Call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set the following properties:</span></span> 
    
  - <span data-ttu-id="a154b-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a154b-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
  - <span data-ttu-id="a154b-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a154b-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
  - <span data-ttu-id="a154b-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a154b-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
  - <span data-ttu-id="a154b-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a154b-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="a154b-118">N'essayez pas de définir les propriétés **PR_RESOURCE_FLAGS** ou **PR_PROVIDER_DLL_NAME** de la section profil.</span><span class="sxs-lookup"><span data-stu-id="a154b-118">Do not attempt to set the profile section's **PR_RESOURCE_FLAGS** or **PR_PROVIDER_DLL_NAME** properties.</span></span> <span data-ttu-id="a154b-119">Au moment de la connexion, ces propriétés sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a154b-119">At logon time, these properties are read-only.</span></span> 
  
4. <span data-ttu-id="a154b-120">Vérifiez que les propriétés dont vous avez besoin pour la configuration sont soit stockées dans le profil, soit disponibles auprès de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a154b-120">Check that the properties you need for configuration are either stored in the profile or are available from the user.</span></span> <span data-ttu-id="a154b-121">Pour plus d'informations sur la vérification de votre configuration, consultez la rubrique vérification de la [configuration du fournisseur de services](verifying-service-provider-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="a154b-121">For more information about checking your configuration, see [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).</span></span>
    
5. <span data-ttu-id="a154b-122">Appelez la méthode [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) de l'objet de prise en charge pour enregistrer un identificateur unique, ou [MAPIUID](mapiuid.md), si votre fournisseur est un carnet d'adresses ou un fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="a154b-122">Call the support object's [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md), if your provider is an address book or message store provider.</span></span> <span data-ttu-id="a154b-123">Les fournisseurs de transport inscrivent les structures **MAPIUID** lorsque MAPI appelle leur méthode [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="a154b-123">Transport providers register **MAPIUID** structures when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="a154b-124">Pour plus d'informations sur l'inscription d'un **MAPIUID**, consultez la rubrique [Register Service Provider unique Identifiers](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="a154b-124">For more information about registering a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
    
6. <span data-ttu-id="a154b-125">Instanciez un objet Logon et renvoyez avec l'une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="a154b-125">Instantiate a logon object and return with one of the following values:</span></span>
    
  - <span data-ttu-id="a154b-126">S_OK pour indiquer la réussite de l'ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="a154b-126">S_OK to indicate a successful logon.</span></span>
    
  - <span data-ttu-id="a154b-127">MAPI_E_UNCONFIGURED pour indiquer qu'une ou plusieurs propriétés de configuration n'étaient pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="a154b-127">MAPI_E_UNCONFIGURED to indicate that one or more of the configuration properties were unavailable.</span></span>
    
  - <span data-ttu-id="a154b-128">MAPI_E_USER_CANCEL pour indiquer que l'utilisateur a annulé la boîte de dialogue de configuration, ce qui entraîne l'indisponibilité des propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="a154b-128">MAPI_E_USER_CANCEL to indicate that the user canceled the configuration dialog box, causing configuration properties to be unavailable.</span></span>
    
  - <span data-ttu-id="a154b-129">MAPI_E_FAILONEPROVIDER pour indiquer que votre fournisseur n'a pas pu être configuré, mais que MAPI doit l'autoriser à être utilisé indépendamment.</span><span class="sxs-lookup"><span data-stu-id="a154b-129">MAPI_E_FAILONEPROVIDER to indicate that your provider could not be configured, but that MAPI should allow it to be used regardless.</span></span> <span data-ttu-id="a154b-130">Les méthodes d'ouverture de session doivent renvoyer cette valeur pour signaler une erreur récupérable, par exemple lorsque le fournisseur requiert un mot de passe et ne peut pas l'inviter à l'utilisateur, car l'interface utilisateur est désactivée.</span><span class="sxs-lookup"><span data-stu-id="a154b-130">Logon methods should return this value to report a nonfatal error, such as when the provider requires a password and cannot prompt the user for it because the user interface is disabled.</span></span> 
    
<span data-ttu-id="a154b-131">La liste de tâches précédente décrit une implémentation minimale pour une méthode de connexion au fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="a154b-131">The preceding list of tasks describes a minimum implementation for a service provider logon method.</span></span> <span data-ttu-id="a154b-132">Vous pouvez inclure des fonctionnalités supplémentaires, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="a154b-132">You can include additional functionality, if necessary.</span></span> <span data-ttu-id="a154b-133">Par exemple, certains fournisseurs appellent [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) pour mettre à jour la table d'État dans leur méthode d'ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="a154b-133">For example, some providers call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) to update the status table in their logon method.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a154b-134">Pour obtenir les meilleures performances lors de la connexion, évitez d'appeler [IMAPISupport::P reparesubmit](imapisupport-preparesubmit.md) ou [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md).</span><span class="sxs-lookup"><span data-stu-id="a154b-134">To achieve the best performance at logon time, avoid calling either [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) or [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span></span> <span data-ttu-id="a154b-135">Avant que ces appels puissent effectuer et rendre le contrôle de votre méthode d'ouverture de session, le spouleur MAPI doit être démarré.</span><span class="sxs-lookup"><span data-stu-id="a154b-135">Before these calls can complete and return control to your logon method, the MAPI spooler must be started.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a154b-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a154b-136">See also</span></span>

- [<span data-ttu-id="a154b-137">Démarrage d'un fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="a154b-137">Starting a Service Provider</span></span>](starting-a-service-provider.md)

