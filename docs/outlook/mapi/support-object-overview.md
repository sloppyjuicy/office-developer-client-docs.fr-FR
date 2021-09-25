---
title: Vue d’ensemble de l’objet support
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5b062891-39ab-4334-9706-5b376719d5e4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b22632aecc048089f49aa92681bf6af1b43b7947
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566366"
---
# <a name="support-object-overview"></a>Vue d’ensemble de l’objet support

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI fournit un objet de support, un objet qui implémente l’interface [IMAPISupport : IUnknown,](imapisupportiunknown.md) pour tous les fournisseurs de services lors de l’logonation et pour tous les services de message pendant la configuration. 
  
Les objets de support ne sont pas accessibles par les clients ; Elles sont implémentées par MAPI et appelées uniquement par les fournisseurs de services. **L’interface IMAPISupport** est spécifiée dans le fichier d’en-tête Mapispi.h. Son identificateur IID_IMAPISup et son type de pointeur est LPMAPISUP. Aucune propriété MAPI n’est exposée par les objets de prise en charge. 
  
Un fournisseur peut se voir donner un ou plusieurs objets de prise en charge, selon le nombre de connexions MAPI au fournisseur ou le nombre d’appel de la fonction d’entrée de service de messagerie du fournisseur. En règle générale, un fournisseur est connecté au moins une fois par session. Les fournisseurs de carnet d’adresses et de transport sont connectés chaque fois qu’un client démarre une session avec une entrée de profil qui les demande. Les fournisseurs de magasins de messages sont connectés chaque fois qu’un client appelle la méthode [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md) 
  
Dans le cas de plusieurs ouvertures de session dans une session, vous pouvez choisir de conserver et d’utiliser chaque objet de support séparément ou de conserver et d’utiliser uniquement le premier, en rejetant chaque objet de support suivant. Pour conserver un objet de support, appelez sa **méthode IUnknown::AddRef.** Il est extrêmement important d’appeler **AddRef** sur un objet de support que vous souhaitez conserver tout au long d’une session . Si l’appel n’est pas effectué, MAPI libère l’objet de support et libère sa mémoire. 
  
L’objectif de l’objet de support est de fournir des implémentations pour un nombre relativement élevé de méthodes couramment utilisées par les fournisseurs. Chaque objet de support contient également des données contextuelles spécifiques à sa propre instance, telles que la session dans qui le fournisseur est en cours d’exécution, la section de profil que le fournisseur utilise et les informations d’erreur pour la session. 
  
Il existe quatre types différents d’objets de support : un pour chaque type de fournisseur principal (carnet d’adresses, magasin de messages et transport) et un pour la prise en charge de la configuration. 
  
MAPI personnalise chaque objet de prise en charge en incluant des implémentations de méthodes pertinentes pour son utilisation. Les implémentations de certaines méthodes, telles que [IMAPISupport::OpenProfileSection,](imapisupport-openprofilesection.md)sont incluses dans tous les objets de prise en charge. Les implémentations d’autres méthodes, telles que [IMAPISupport::SpoolerNotify,](imapisupport-spoolernotify.md)s’appliquent uniquement à des objets de support particuliers. Seuls les fournisseurs de transport et de magasin de messages peuvent utiliser cette méthode . lorsqu’un fournisseur de carnet d’adresses ou un service de messagerie tente de l’appeler, MAPI renvoie MAPI_E_NO_SUPPORT.
  
Les objets de support peuvent être utilisés pour accomplir de nombreuses tâches, telles que les suivantes :
  
- Accès à une section de profil.
    
- Copie de dossiers ou de messages. Pour plus d’informations, [voir Copier ou déplacer un message ou un dossier.](copying-or-moving-a-message-or-a-folder.md)
    
- Accès aux objets appartenant à d’autres fournisseurs. Pour plus d’informations, voir [Supporting Object Access and Comparison](supporting-object-access-and-comparison.md). 
    
- Gestion des notifications d’événement. Pour plus d’informations, voir [Notification d’événement de prise en charge.](supporting-event-notification.md)
    
- Allocation et libération de mémoire.
    
- Obtention d’un identificateur unique.
    
- Invalidation d’objets.
    
- Gestion des erreurs.
    
- Inscription des préprocesseurs de messages. 
    
- Préparation des rapports de remise des messages. 
    
Au moment de l’logo, MAPI appelle la méthode d’accès à l’objet fournisseur de chaque fournisseur de services. Pour les fournisseurs de carnet d’adresses, MAPI appelle [IABProvider::Logon](iabprovider-logon.md). Pour les fournisseurs de magasins de messages, MAPI appelle [IMSProvider::Logon](imsprovider-logon.md). Pour les fournisseurs de transport, MAPI appelle [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). MAPI transmet un pointeur vers l’objet de support approprié dans l’un des paramètres de cette méthode. La méthode d' logon ins instantique à son tour un objet d’accès, en lui passant le pointeur d’objet de prise en charge. L’objet d’logon appelle la méthode **IUnknown::AddRef** de l’objet de support pour le conserver, si nécessaire. Pour plus d’informations sur le processus d’accès pour les fournisseurs de services, voir [Démarrage d’un fournisseur de services.](starting-a-service-provider.md)
  
Lorsqu’un client se déconnecte, MAPI appelle la méthode de connexion de l’objet de connexion. La méthode logoff appelle la méthode **IUnknown::Release** de l’objet de support pour indiquer que le fournisseur n’a plus l’intention d’appeler les méthodes de support. Comme pour l' logon, les méthodes de ff de logo ont des noms légèrement différents. Les interfaces [IABLogon](iablogoniunknown.md) et [IMSLogon](imslogoniunknown.md) ont des méthodes **Logoff** ; [L’interface IXPLogon](ixplogoniunknown.md) possède une [méthode TransportLogoff.](ixplogon-transportlogoff.md) 
  
Les fonctions de point d’entrée de service de message sont appelées lorsqu’une tentative d’accès échoue avec l’erreur MAPI_E_UNCONFIGURED ou lorsqu’un client lance une demande de configuration. MAPI ins instantie un objet de prise en charge de configuration et appelle la fonction de point d’entrée du service de messagerie pour le fournisseur non configuré ou le fournisseur dont la configuration est sur le point de changer. Contrairement aux autres objets de prise en charge, les objets de prise en charge de configuration ne sont valides que jusqu’à ce que la fonction de point d’entrée soit de retour . les services de message n’appellent pas les méthodes **AddRef** de ces objets pour les conserver. 
  
En règle générale, MAPI effectue des appels vers la fonction de point d’entrée du service de messagerie d’un fournisseur, mais parfois, un fournisseur est invité à passer l’appel. Cela peut se produire lorsqu’un client appelle la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) d’un fournisseur pour l’inviter à afficher sa feuille de propriétés de configuration. **SettingsDialog** doit appeler [IMAPISupport::GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) pour obtenir un objet de prise en charge de configuration qu’il peut transmettre à la fonction de point d’entrée du service de message. 
  
La [méthode IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) permet de déterminer les adresses des fonctions d’allocation et de déallocation de la mémoire sans avoir à établir de liaison avec MAPI. **L’utilisation de GetMemAllocRoutines** facilite également le suivi des fuites de mémoire en entourant les appels de fonction d’allocation avec du code de débogage. Si vous appelez **GetMemAllocRoutines,** comme recommandé, faites-le avant d’appeler la fonction [CreateIProp,](createiprop.md) qui requiert les adresses de la fonction d’allocation en tant que paramètres. 
  
Lorsque vous devez créer un objet de carnet d’adresses ou de magasin de messages, créez et définissez une clé de recherche pour l’objet dans sa propriété **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Appelez [IMAPISupport::NewUID](imapisupport-newuid.md) pour obtenir un identificateur unique à utiliser dans la création d’une clé de recherche. N’utilisez pas votre propre [MAPIUID](mapiuid.md)codé en dur. **MapIUID** d’un fournisseur doit être utilisé uniquement pour les identificateurs d’entrée. Pour plus d’informations sur la construction de clés de recherche, voir [MapI Record and Search Keys](mapi-record-and-search-keys.md).
  
Une application cliente peut parfois libérer un objet sans libérer un ou plusieurs de ses objets affiliés. Dans ce cas, un fournisseur peut avoir besoin de rendre un objet non nouveau inutilisable. Pour ce faire, le fournisseur libère toutes les ressources connectées à l’objet, puis appelle [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) pour invalider la table vtable de l’objet. **MakeInvalid** remplace les méthodes **IUnknown** du vtable (**QueryInterface**, **AddRef** et **Release**) par des implémentations MAPI standard et entraîne le retour de toutes les autres méthodes MAPI_E_INVALID_OBJECT. **MakeInvalid** libère également toute la mémoire de l’objet autre que le vtable. 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

