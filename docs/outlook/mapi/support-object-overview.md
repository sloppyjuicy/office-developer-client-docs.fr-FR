---
title: Vue d'ensemble de l'objet support
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5b062891-39ab-4334-9706-5b376719d5e4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 55d8a9c78ae5132eaa8cf0f0aec5b252ef83b926
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433611"
---
# <a name="support-object-overview"></a>Vue d'ensemble de l'objet support

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI fournit un objet de prise en charge, un objet qui implémente l'interface [IMAPISupport: IUnknown](imapisupportiunknown.md) , pour tous les fournisseurs de services lors de l'ouverture de session et pour tous les services de messagerie lors de la configuration. 
  
Les clients ne peuvent pas accéder aux objets de prise en charge; elles sont implémentées par MAPI et appelées uniquement par les fournisseurs de services. L'interface **IMAPISupport** est spécifiée dans le fichier d'en-tête Mapispi. h. Son identificateur est IID_IMAPISup et son type de pointeur est LPMAPISUP. Aucune propriété MAPI n'est exposée par les objets de prise en charge. 
  
Un fournisseur peut recevoir un ou plusieurs objets de prise en charge, selon le nombre de fois que MAPI enregistre le fournisseur ou le nombre de fois que la fonction d'entrée de service de message du fournisseur est appelée. En règle générale, un fournisseur est connecté au moins une fois par session. Le carnet d'adresses et les fournisseurs de transport sont connectés chaque fois qu'un client démarre une session avec une entrée de profil qui le demande. Les fournisseurs de banques de messages sont connectés chaque fois qu'un client appelle la méthode [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) . 
  
Dans le cas de plusieurs ouvertures de session dans une session, vous pouvez choisir de conserver et d'utiliser chaque objet de prise en charge séparément ou de conserver et d'utiliser uniquement le premier objet de prise en charge. Pour conserver un objet de prise en charge, appelez sa méthode **IUnknown:: AddRef** . L'appel de **AddRef** sur un objet de prise en charge que vous souhaitez conserver au cours d'une session est extrêmement important; Si l'appel n'est pas effectué, MAPI libère l'objet de prise en charge et libère sa mémoire. 
  
L'objectif de l'objet support est de fournir des implémentations pour un nombre assez important de méthodes couramment utilisées par les fournisseurs. Chaque objet support contient également des données contextuelles spécifiques à sa propre instance, telles que la session dans laquelle le fournisseur est exécuté, la section de profil utilisée par le fournisseur, ainsi que les informations d'erreur pour la session. 
  
Il existe quatre types d'objets de prise en charge: un pour chaque type de fournisseur principal (carnet d'adresses, Banque de messages et transport) et un autre pour la prise en charge de la configuration. 
  
MAPI personnalise chaque objet de prise en charge en incluant des implémentations de méthodes qui sont pertinentes pour son utilisation. Les implémentations de certaines méthodes, telles que [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md), sont incluses dans tous les objets support. Les implémentations d'autres méthodes, telles que [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md), s'appliquent uniquement à des objets de prise en charge particuliers. Seuls les fournisseurs de banque de messages et de transport peuvent utiliser cette méthode; Lorsqu'un fournisseur de carnet d'adresses ou un service de messagerie tente de l'appeler, MAPI renvoie MAPI_E_NO_SUPPORT.
  
Les objets de prise en charge peuvent être utilisés pour effectuer de nombreuses tâches, telles que les suivantes:
  
- Accès à une section de profil.
    
- Copie de dossiers ou de messages. Pour plus d'informations, consultez [la rubrique copie ou transfert d'un message ou d'un dossier](copying-or-moving-a-message-or-a-folder.md).
    
- Accès aux objets qui appartiennent à d'autres fournisseurs. Pour plus d'informations, consultez la rubrique [prise en charge de l'accès aux objets et comparaison](supporting-object-access-and-comparison.md). 
    
- Gestion des notifications d'événements. Pour plus d'informations, consultez la rubrique [notification d'événement de prise en charge](supporting-event-notification.md).
    
- Allocation et libération de la mémoire.
    
- Obtention d'un identificateur unique.
    
- Invalidation des objets.
    
- Gestion des erreurs.
    
- Enregistrement des préprocesseurs de messages. 
    
- Préparation des rapports de remise des messages. 
    
Lors de l'ouverture de session, MAPI appelle la méthode d'ouverture de session de l'objet fournisseur de chaque fournisseur de services. Pour les fournisseurs de carnet d'adresses, MAPI appelle [IABProvider:: Logon](iabprovider-logon.md). Pour les fournisseurs de banque de messages, MAPI appelle [IMSProvider:: Logon](imsprovider-logon.md). Pour les fournisseurs de transport, MAPI appelle [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md). MAPI transmet un pointeur vers l'objet de prise en charge approprié dans l'un des paramètres à cette méthode. La méthode d'ouverture de session instancie à son tour un objet Logon, lui transmettant le pointeur d'objet support. L'objet Logon appelle la méthode **IUnknown:: AddRef** de l'objet support pour le conserver, le cas échéant. Pour plus d'informations sur le processus d'ouverture de session pour les fournisseurs de services, consultez la rubrique [démarrage d'un fournisseur de services](starting-a-service-provider.md).
  
Lorsqu'un client se déconnecte, MAPI appelle la méthode de fermeture de session de l'objet. La méthode Logoff appelle la méthode **IUnknown:: Release** de l'objet de prise en charge pour indiquer que le fournisseur n'envisage plus d'appeler aucune des méthodes de prise en charge. Comme pour l'ouverture de session, les méthodes de fermeture de session ont des noms légèrement différents. Les interfaces [IABLogon](iablogoniunknown.md) et [IMSLogon](imslogoniunknown.md) ont des méthodes de **fermeture de session** ; l'interface [IXPLogon](ixplogoniunknown.md) possède une méthode [TransportLogoff](ixplogon-transportlogoff.md) . 
  
Les fonctions de point d'entrée du service de messagerie sont appelées lorsqu'une tentative d'ouverture de session échoue avec l'erreur MAPI_E_UNCONFIGURED ou lorsqu'un client lance une demande de configuration. MAPI instancie un objet de prise en charge de la configuration et appelle la fonction de point d'entrée du service de messagerie pour le fournisseur non configuré ou le fournisseur dont la configuration est sur le point d'être modifiée. Contrairement aux autres objets de prise en charge, les objets de prise en charge de la configuration sont valides jusqu'à ce que la fonction de point d'entrée renvoie; les services de messagerie n'appellent pas ces objets' **AddRef** Methods'pour les conserver. 
  
En règle générale, MAPI effectue des appels vers la fonction de point d'entrée du service de messagerie d'un fournisseur, mais parfois un fournisseur est invité à effectuer l'appel. Cela peut se produire lorsqu'un client appelle la méthode [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) d'un fournisseur pour inviter le fournisseur à afficher sa feuille de propriétés de configuration. **SettingsDialog** doit appeler [IMAPISupport:: GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) pour obtenir un objet de prise en charge de la configuration qu'il peut transmettre à la fonction de point d'entrée du service de messagerie. 
  
La méthode [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) est disponible pour déterminer les adresses des fonctions d'allocation et de désallocation de mémoire sans avoir à établir de liaison avec MAPI. L'utilisation de **GetMemAllocRoutines** permet également de suivre plus facilement les fuites de mémoire en entourant les appels de fonction d'allocation avec le code de débogage. Si vous appelez **GetMemAllocRoutines**, comme c'est recommandé, faites-le avant d'appeler la fonction [CreateIProp](createiprop.md) , qui exige que la fonction d'allocation adresse en tant que paramètres. 
  
Lorsque vous avez besoin de créer un nouvel objet de carnet d'adresses ou de banque de messages, créez et définissez une clé de recherche pour l'objet dans sa propriété **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Appelez [IMAPISupport:: NewUID](imapisupport-newuid.md) pour obtenir un identificateur unique à utiliser dans la création d'une clé de recherche. N'utilisez pas votre propre [MAPIUID](mapiuid.md)codé en dur. Le **MAPIUID** d'un fournisseur doit être utilisé uniquement pour les identificateurs d'entrée. Pour plus d'informations sur la création de clés de recherche, voir [enregistrement MAPI et clés de recherche](mapi-record-and-search-keys.md).
  
Une application cliente peut parfois libérer un objet sans libérer un ou plusieurs de ses objets affiliés. Dans ce cas, un fournisseur peut avoir besoin de rendre un objet non publié inutilisable. Pour ce faire, le fournisseur libère toutes les ressources connectées à l'objet, puis appelle [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md) pour invalider le vtable de l'objet. **MakeInvalid** remplace les méthodes **IUnknown** de vtable (**QueryInterface**, **AddRef**et **Release**) par les implémentations MAPI standard et toutes les autres méthodes renvoient MAPI_E_INVALID_OBJECT. **MakeInvalid** libère également toute la mémoire de l'objet autre que vtable. 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

