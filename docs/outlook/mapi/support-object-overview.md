---
title: Prise en charge de la vue d’ensemble de l’objet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5b062891-39ab-4334-9706-5b376719d5e4
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ecc5439b4abbbfd920fba5456db7462f7967388f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787268"
---
# <a name="support-object-overview"></a>Prise en charge de la vue d’ensemble de l’objet

  
  
**S’applique à**: Outlook 
  
MAPI fournit un objet de prise en charge, un objet qui implémente le [IMAPISupport : IUnknown](imapisupportiunknown.md) interface, pour tous les fournisseurs de services au cours de l’ouverture de session et pour tous les services de message lors de la configuration. 
  
Prise en charge des objets ne sont pas accessibles par les clients ; ils sont implémentés par MAPI et appelées uniquement par les fournisseurs de services. L’interface **IMAPISupport** est spécifié dans le fichier d’en-tête Mapispi.h. Son identificateur est IID_IMAPISup et son type de pointeur est LPMAPISUP. Aucuns propriétés MAPI ne sont exposées par les objets de prise en charge. 
  
Un fournisseur peut être attribué à un ou plusieurs objets de prise en charge, selon le nombre de fois que le fournisseur de session MAPI ou le nombre de répétitions de que fonction de l’entrée de service de message du fournisseur est appelée. En règle générale, un fournisseur sera connecté au moins une fois par session. Fournisseurs de transport et le carnet d’adresses sont enregistrés chaque fois qu’un client démarre une session avec une entrée de profil qui les demande. Fournisseurs de banque de messages sont enregistrés sur chaque fois qu’un client appelle la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . 
  
Dans le cas d’ouvertures de session multiples dans une session, vous pouvez choisir de conserver et d’utiliser chaque objet prise en charge séparément ou de conserver et d’utiliser uniquement le premier, en supprimant chaque objet prise en charge suivantes. Pour conserver un objet de prise en charge, appelez la méthode **IUnknown::AddRef** . L’appel de **AddRef** sur un objet de prise en charge que vous souhaitez conserver au sein d’une session est extrêmement important ; Si l’appel n’est pas effectué, MAPI libère l’objet de prise en charge et libère de la mémoire. 
  
L’objectif de l’objet de prise en charge est de fournir des implémentations pour un grand nombre des méthodes couramment utilisées par les fournisseurs. Chaque objet de prise en charge contient également des données contextuelles spécifiques à sa propre instance, telles que la session que le fournisseur est en cours d’exécution dans la section profil qu'utilise le fournisseur et les informations d’erreur pour la session. 
  
Il existe quatre types d’objets de prise en charge : un pour chaque type de fournisseur principales (carnet d’adresses, banque de messages et de transport) et un pour la prise en charge de la configuration. 
  
MAPI personnalise chaque objet prise en charge par, y compris les implémentations des méthodes qui sont pertinents pour son utilisation. Implémentations de certaines méthodes, telles [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), sont incluses dans tous les objets de prise en charge. Implémentations d’autres méthodes, telles [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md), s’appliquent uniquement aux objets de prise en charge particulière. Magasin des messages uniquement et fournisseurs de transport peuvent utiliser cette méthode ; Lorsqu’un fournisseur de carnet d’adresses ou d’un service de message essayez d’appeler, MAPI renvoie MAPI_E_NO_SUPPORT.
  
Objets de prise en charge peuvent être utilisés pour réaliser de nombreuses tâches, telles que les suivantes :
  
- Accès à une section de profil.
    
- Copie de dossiers ou des messages. Pour plus d’informations, voir [copie ou déplacement d’un Message ou un dossier](copying-or-moving-a-message-or-a-folder.md).
    
- Accès aux objets qui appartiennent à d’autres fournisseurs. Pour plus d’informations, voir [prise en charge l’accès aux objets et comparaison](supporting-object-access-and-comparison.md). 
    
- Gestion de notification d’événement. Pour plus d’informations, voir [Prise en charge de Notification d’événement](supporting-event-notification.md).
    
- Allocation et libération de la mémoire.
    
- Obtention d’un identificateur unique.
    
- Invalidation d’objets.
    
- Gestion des erreurs.
    
- Inscription Préprocesseurs du message. 
    
- Préparation des rapports de remise de message. 
    
Au moment de l’ouverture de session MAPI appelle la méthode d’ouverture de session de l’objet de fournisseur de chaque fournisseur de services. Pour les fournisseurs de carnet d’adresses, MAPI appelle [IABProvider::Logon](iabprovider-logon.md). Pour les fournisseurs de banque de messages, [IMSProvider::Logon](imsprovider-logon.md)appels MAPI. Pour les fournisseurs de transport, [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)appels MAPI. MAPI passe un pointeur vers l’objet de prise en charge appropriée dans l’un des paramètres à cette méthode. À son tour, la méthode d’ouverture de session instancie un objet d’ouverture de session, en lui transmettant le pointeur d’objet prise en charge. L’objet d’ouverture de session appelle la prise en charge de méthode l’objet **IUnknown::AddRef** pour conserver, si nécessaire. Pour plus d’informations sur le processus d’ouverture de session pour les fournisseurs de service, voir [démarrage d’un fournisseur de services](starting-a-service-provider.md).
  
Quand un client se déconnecte, MAPI appelle la méthode de fermeture de session de l’objet d’ouverture de session. La méthode de fermeture de session appelle la méthode **IUnknown::Release** de l’objet de la prise en charge pour indiquer que le fournisseur a n’est plus l’intention d’appeler une des méthodes de prise en charge. Comme avec l’ouverture de session, les méthodes de fermeture de session ont des noms légèrement différents. Les interfaces [IABLogon](iablogoniunknown.md) et [IMSLogon](imslogoniunknown.md) ont des méthodes de **fermeture de session** ; l’interface [IXPLogon](ixplogoniunknown.md) a une méthode [TransportLogoff](ixplogon-transportlogoff.md) . 
  
Fonctions de point d’entrée message service sont appelées lorsqu’une tentative d’ouverture de session échoue avec l’erreur MAPI_E_UNCONFIGURED ou lorsqu’un client lance une demande de configuration. MAPI instancie un objet de configuration de prise en charge et appelle la fonction de point d’entrée de message service pour le fournisseur non configuré ou le fournisseur dont la configuration est sur le point de changer. Contrairement à d’autres objets, objets de configuration de prise en charge sont valides jusqu'à ce que le point d’entrée fonction renvoie ; services message n’appelez pas les méthodes **AddRef** de ces objets pour les conserver. 
  
En règle générale, MAPI effectue des appels à la fonction de point d’entrée du service de message d’un fournisseur, mais parfois un fournisseur est posée à l’appel. Cela peut se produire lorsqu’un client appelle une méthode de fournisseur [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) pour demander le fournisseur pour afficher sa feuille de propriétés de configuration. **Dialogue** doit appeler [IMAPISupport::GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) pour obtenir un objet de prise en charge de configuration il peut passer à la fonction de point d’entrée de message service. 
  
La méthode [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) est disponible pour déterminer les adresses des fonctions allocation et libération de mémoire sans créer de lien MAPI. À l’aide de **GetMemAllocRoutines** facilite également effectuer le suivi de fuites de mémoire en mettant les appels de fonction allocation avec code de débogage. Si vous appelez **GetMemAllocRoutines**, comme est recommandé, le faire avant d’appeler la fonction [CreateIProp](createiprop.md) , qui requiert l’allocation des adresses fonction en tant que paramètres. 
  
Lorsque vous avez besoin créer un nouveau carnet d’adresses ou un message objet banque, créer et définir une clé de recherche pour l’objet dans sa propriété **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Appelez [IMAPISupport::NewUID](imapisupport-newuid.md) pour obtenir un identificateur unique à utiliser lors de la création d’une clé de recherche. N’utilisez pas votre propre codé en dur [MAPIUID](mapiuid.md). D’un fournisseur **MAPIUID** doit être utilisé uniquement pour les identificateurs d’entrée. Pour plus d’informations sur la construction clés de recherche, voir [enregistrement MAPI et les clés de recherche](mapi-record-and-search-keys.md).
  
Une application cliente peut parfois libérer un objet sans libère un ou plusieurs de ses objets affiliés. Dans ce cas, un fournisseur devrez de rendre un objet non publiée inutilisable. Pour ce faire, le fournisseur libère toutes les ressources liées à l’objet, puis appelle [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) pour invalider vtable de l’objet. **MakeInvalid** remplace les méthodes de **IUnknown** de vtable (**QueryInterface**, **AddRef**et **Release**) et les implémentations de MAPI standards et affiche toutes les autres méthodes renvoyer MAPI_E_INVALID_OBJECT. **MakeInvalid** également libère de la mémoire de de tous les objets autre que la vtable. 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

