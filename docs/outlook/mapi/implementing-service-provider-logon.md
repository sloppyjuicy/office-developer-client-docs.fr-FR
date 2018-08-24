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
ms.openlocfilehash: 1baa987961eecc6ee08b3ceb039062c8f1090ff7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589552"
---
# <a name="implementing-service-provider-logon"></a>Implémentation d’une ouverture de session de fournisseur de services

**S’applique à**: Outlook 2013 | Outlook 2016 
  
MAPI appelle une méthode dans votre objet de fournisseur pour commencer le processus d’ouverture de session en utilisant le pointeur vous renvoyez à partir de la fonction de point d’entrée. La méthode varie comme suit, en fonction du type de votre fournisseur de services :
  
- [IABProvider::Logon](iabprovider-logon.md) pour les fournisseurs de carnet d’adresses 
    
- [IMSProvider::Logon](imsprovider-logon.md) pour les fournisseurs de banque de messages 
    
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) pour les fournisseurs de transport 
    
Effectuer les tâches suivantes dans n’importe quelle méthode d’ouverture de session vous implémentez :
  
1. Incrémente le décompte de références sur l’objet de prise en charge qui est passé comme paramètre d’entrée en appelant la méthode [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) . 
    
2. Appeler la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) de l’objet de la prise en charge pour accéder à la section de profil. 
    
3. Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de la section profil pour définir les propriétés suivantes : 
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
  - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
  - **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > N’essayez pas de définir les propriétés **PR_RESOURCE_FLAGS** ou **PR_PROVIDER_DLL_NAME** de la section profil. Au moment de l’ouverture de session, ces propriétés sont en lecture seule. 
  
4. Vérifiez que les propriétés que vous avez besoin pour la configuration sont stockées soit dans le profil ou qui sont disponibles à partir de l’utilisateur. Pour plus d’informations sur la vérification de votre configuration, voir [Configuration du fournisseur de Service de vérification](verifying-service-provider-configuration.md).
    
5. Appelez la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) de l’objet de la prise en charge pour inscrire un identificateur unique, ou [MAPIUID](mapiuid.md), si votre fournisseur est un fournisseur de magasin de message ou de carnet d’adresses. Fournisseurs de transport inscrire **MAPIUID** structures lors de leur méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) des appels MAPI. Pour plus d’informations sur l’inscription d’un **MAPIUID**, voir [Inscription des identificateurs uniques Service fournisseur](registering-service-provider-unique-identifiers.md).
    
6. Instancier un objet d’ouverture de session et retourner avec une des valeurs suivantes :
    
  - S_OK pour indiquer une ouverture de session.
    
  - MAPI_E_UNCONFIGURED pour indiquer qu’une ou plusieurs des propriétés de configuration n’étaient pas disponibles.
    
  - MAPI_E_USER_CANCEL pour indiquer que l’utilisateur a annulé la boîte de dialogue de configuration à l’origine des propriétés de configuration afin de ne pas être disponible.
    
  - Référence à MAPI_E_FAILONEPROVIDER pour indiquer que votre fournisseur ne peut pas être configuré, mais que MAPI doit autoriser qu’il soit utilisé ou non. Méthodes d’ouverture de session doivent renvoyer cette valeur pour signaler une erreur récupérable, telles que lorsque le fournisseur exige un mot de passe et ne peut pas demander à l’utilisateur pour qu’il parce que l’interface utilisateur est désactivée. 
    
La liste des tâches ci-dessus décrit une implémentation minimale pour une méthode de connexion de fournisseur de service. Vous pouvez inclure des fonctionnalités supplémentaires, si nécessaire. Par exemple, certains fournisseurs appeler [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) pour mettre à jour la table d’état dans leur méthode d’ouverture de session. 
  
> [!NOTE]
> Pour optimiser les performances au moment de l’ouverture de session, évitez d’appeler [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) ou [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md). Avant de ces appels peuvent effectuer et retourner le contrôle à votre méthode d’ouverture de session, le spouleur MAPI doit être démarré. 
  
## <a name="see-also"></a>Voir aussi

- [Démarrage d’un fournisseur de services](starting-a-service-provider.md)

