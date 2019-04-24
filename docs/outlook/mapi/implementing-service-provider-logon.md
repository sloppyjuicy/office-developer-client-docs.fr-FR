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
# <a name="implementing-service-provider-logon"></a>Implémentation de la connexion au fournisseur de services

**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI appelle une méthode dans votre objet fournisseur pour commencer le processus d'ouverture de session à l'aide du pointeur que vous avez renvoyé à partir de votre fonction de point d'entrée. La méthode varie, selon le type de votre fournisseur de services:
  
- [IABProvider:: Logon](iabprovider-logon.md) pour les fournisseurs de carnet d'adresses 
    
- [IMSProvider:: Logon](imsprovider-logon.md) pour les fournisseurs de banque de messages 
    
- [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) pour les fournisseurs de transport 
    
Effectuez les tâches suivantes dans la méthode de connexion que vous implémentez:
  
1. Incrémentez le décompte de références sur l'objet de prise en charge qui est passé en tant que paramètre d'entrée en appelant sa méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) . 
    
2. Appelez la méthode [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) de l'objet de prise en charge pour accéder à votre section de profil. 
    
3. Appelez la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) de la section profile pour définir les propriétés suivantes: 
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
  - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
  - **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > N'essayez pas de définir les propriétés **PR_RESOURCE_FLAGS** ou **PR_PROVIDER_DLL_NAME** de la section profil. Au moment de la connexion, ces propriétés sont en lecture seule. 
  
4. Vérifiez que les propriétés dont vous avez besoin pour la configuration sont soit stockées dans le profil, soit disponibles auprès de l'utilisateur. Pour plus d'informations sur la vérification de votre configuration, consultez la rubrique vérification de la [configuration du fournisseur de services](verifying-service-provider-configuration.md).
    
5. Appelez la méthode [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) de l'objet de prise en charge pour enregistrer un identificateur unique, ou [MAPIUID](mapiuid.md), si votre fournisseur est un carnet d'adresses ou un fournisseur de banque de messages. Les fournisseurs de transport inscrivent les structures **MAPIUID** lorsque MAPI appelle leur méthode [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) . Pour plus d'informations sur l'inscription d'un **MAPIUID**, consultez la rubrique [Register Service Provider unique Identifiers](registering-service-provider-unique-identifiers.md).
    
6. Instanciez un objet Logon et renvoyez avec l'une des valeurs suivantes:
    
  - S_OK pour indiquer la réussite de l'ouverture de session.
    
  - MAPI_E_UNCONFIGURED pour indiquer qu'une ou plusieurs propriétés de configuration n'étaient pas disponibles.
    
  - MAPI_E_USER_CANCEL pour indiquer que l'utilisateur a annulé la boîte de dialogue de configuration, ce qui entraîne l'indisponibilité des propriétés de configuration.
    
  - MAPI_E_FAILONEPROVIDER pour indiquer que votre fournisseur n'a pas pu être configuré, mais que MAPI doit l'autoriser à être utilisé indépendamment. Les méthodes d'ouverture de session doivent renvoyer cette valeur pour signaler une erreur récupérable, par exemple lorsque le fournisseur requiert un mot de passe et ne peut pas l'inviter à l'utilisateur, car l'interface utilisateur est désactivée. 
    
La liste de tâches précédente décrit une implémentation minimale pour une méthode de connexion au fournisseur de services. Vous pouvez inclure des fonctionnalités supplémentaires, le cas échéant. Par exemple, certains fournisseurs appellent [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) pour mettre à jour la table d'État dans leur méthode d'ouverture de session. 
  
> [!NOTE]
> Pour obtenir les meilleures performances lors de la connexion, évitez d'appeler [IMAPISupport::P reparesubmit](imapisupport-preparesubmit.md) ou [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md). Avant que ces appels puissent effectuer et rendre le contrôle de votre méthode d'ouverture de session, le spouleur MAPI doit être démarré. 
  
## <a name="see-also"></a>Voir aussi

- [Démarrage d'un fournisseur de services](starting-a-service-provider.md)

