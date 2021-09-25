---
title: Mise en œuvre de l’logo du fournisseur de services
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5651ab674071b832eb14d2ca217bd8cf0fa90196
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575693"
---
# <a name="implementing-service-provider-logon"></a>Mise en œuvre de l’logo du fournisseur de services

**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI appelle une méthode dans l’objet fournisseur pour commencer le processus d’inscription à l’aide du pointeur que vous renvoyez à partir de votre fonction de point d’entrée. La méthode varie selon le type de votre fournisseur de services :
  
- [IABProvider::Logon](iabprovider-logon.md) for address book providers 
    
- [IMSProvider::Logon](imsprovider-logon.md) for message store providers 
    
- [IXPProvider::TransportLogon pour](ixpprovider-transportlogon.md) les fournisseurs de transport 
    
Effectuez les tâches suivantes dans n’importe quelle méthode de logo que vous implémentez :
  
1. Incrémentez le nombre de références sur l’objet de prise en charge transmis en tant que paramètre d’entrée en appelant sa méthode [IUnknown::AddRef.](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) 
    
2. Appelez la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) de l’objet de support pour accéder à votre section de profil. 
    
3. Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de la section de profil pour définir les propriétés suivantes : 
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
  - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
  - **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > N’essayez pas de définir les propriétés de PR_RESOURCE_FLAGS **ou** **PR_PROVIDER_DLL_NAME** de la section de profil. Au moment de l’logo, ces propriétés sont en lecture seule. 
  
4. Vérifiez que les propriétés dont vous avez besoin pour la configuration sont stockées dans le profil ou sont disponibles pour l’utilisateur. Pour plus d’informations sur la vérification de votre configuration, voir [Vérification de la configuration du fournisseur de services.](verifying-service-provider-configuration.md)
    
5. Appelez la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) de l’objet de support pour inscrire un identificateur unique, [ou MAPIUID,](mapiuid.md)si votre fournisseur est un carnet d’adresses ou un fournisseur de magasins de messages. Les fournisseurs de transport enregistrent les structures **MAPIUID** lorsque MAPI appelle leur [méthode IXPLogon::AddressTypes.](ixplogon-addresstypes.md) Pour plus d’informations sur l’inscription **d’un MAPIUID,** voir [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).
    
6. Ins instantiate a logon object and return with one of the following values:
    
  - S_OK pour indiquer une bonne logon.
    
  - MAPI_E_UNCONFIGURED pour indiquer qu’une ou plusieurs des propriétés de configuration n’étaient pas disponibles.
    
  - MAPI_E_USER_CANCEL pour indiquer que l’utilisateur a annulé la boîte de dialogue de configuration, ce qui a provoqué l’indisponibilité des propriétés de configuration.
    
  - MAPI_E_FAILONEPROVIDER pour indiquer que votre fournisseur n’a pas pu être configuré, mais que MAPI doit l’autoriser à être utilisé indépendamment. Les méthodes d’accès doivent renvoyer cette valeur pour signaler une erreur non fatale, par exemple lorsque le fournisseur requiert un mot de passe et ne peut pas en faire la demande à l’utilisateur, car l’interface utilisateur est désactivée. 
    
La liste de tâches précédente décrit une implémentation minimale pour une méthode d’accès au fournisseur de services. Vous pouvez inclure des fonctionnalités supplémentaires, si nécessaire. Par exemple, certains fournisseurs appellent [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) pour mettre à jour la table d’état dans leur méthode d’accès. 
  
> [!NOTE]
> Pour obtenir les meilleures performances au moment de l’accès, évitez d’appeler [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) ou [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md). Pour que ces appels soient terminés et qu’ils retournent le contrôle à votre méthode d’accès, lepooler MAPI doit être démarré. 
  
## <a name="see-also"></a>Voir aussi

- [Démarrage d’un fournisseur de services](starting-a-service-provider.md)

