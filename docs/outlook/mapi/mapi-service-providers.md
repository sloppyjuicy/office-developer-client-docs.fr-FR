---
title: Fournisseurs de services MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bb40891376ac511869ba157b675e53ee236b24ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409537"
---
# <a name="mapi-service-providers"></a>Fournisseurs de services MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe trois types courants de fournisseurs de services :
  
- Fournisseurs de carnet d’adresses.
    
- Fournisseurs de magasins de messages.
    
- Fournisseurs de transport.
    
Les fournisseurs de carnet d’adresses et de magasin de messages ont de nombreuses similitudes. Ils enregistrent un identificateur unique auprès de MAPI qu’ils utilisent pour construire des identificateurs d’entrée pour leurs objets. Elles fournissent une hiérarchie d’objets et de propriétés accessibles et manipulées par les clients. Pour leurs objets conteneur, ils supportent une table hiérarchique et une table des matières. Ils peuvent prendre en charge les notifications d’événement sur ces tables et éventuellement sur des objets individuels afin que les clients soient informés des modifications qui se produisent au cours de la session. Lorsque les opérations deviennent longues, elles peuvent afficher un indicateur de progression pour informer l’utilisateur de l’état de l’opération. Les clients peuvent communiquer avec les fournisseurs de carnet d’adresses et de magasin de messages indirectement via MAPI à l’aide de [l’IAddrBook : IMAPIProp](iaddrbookimapiprop.md) et [IMAPISession : interfaces IUnknown](imapisessioniunknown.md) ou directement à l’aide de l’une des interfaces de fournisseur de services dans le tableau suivant. 
  
|**Interfaces du fournisseur de carnet d’adresses**|**Interfaces des fournisseurs de magasins de messages**|
|:-----|:-----|
|[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList : IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser : IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage : IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach : IMAPIProp](iattachimapiprop.md) <br/> |
   
Les fournisseurs de transport diffèrent des fournisseurs de carnet d’adresses et de magasin de messages dans la façon dont ils communiquent avec MAPI et avec les clients. Les fournisseurs de transport attendent généralement que MAPI les invite à fournir des informations plutôt que de lancer la communication. Contrairement aux autres fournisseurs, les fournisseurs de transport ne sont pas en charge une variété d’objets et de tables couramment accessibles par les clients. Toutefois, ils ne prisent en charge un objet d’état, comme tous les fournisseurs de services, et publient ses propriétés dans le tableau d’état. Tandis que les fournisseurs de carnet d’adresses et de magasin de messages appellent la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) pour inscrire des identificateurs uniques pour la construction de leurs identificateurs d’entrée, les fournisseurs de transport appellent la méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) pour inscrire des identificateurs uniques, ainsi que des types d’adresses pour assumer la responsabilité de la remise de messages particuliers. 
  
Votre fournisseur de services doit avoir trois fichiers d’en-tête : un fichier d’en-tête public et deux fichiers internes. Utilisez le fichier d’en-tête public pour la configuration et la documentation des propriétés et de leurs valeurs. Inclure dans l’un des fichiers d’en-tête internes tous les en-têtes MAPI publics nécessaires ; Ce fichier d’en-tête doit être inclus dans tous les fichiers sources de votre fournisseur de services. Utilisez l’autre fichier interne pour définir les identificateurs de ressources.
  
Les fournisseurs de carnet d’adresses, de magasin de messages et de transport effectuent les tâches suivantes :
  
- Fournir une fonction de point d’entrée. 
    
- Fournir un fournisseur et un objet d’personnalisation pour gérer l’personnalisation et l’personnalisation. 
    
- Si le fournisseur appartient à un service de messagerie, fournissons une fonction de point d’entrée de service de messagerie. 
    
- Prise en charge de la configuration en implémentant une feuille de propriétés.
    
- Implémenter un objet d’état et la prise en charge de la table d’état. 
    
- Gérer l’arrêt.
    
## <a name="see-also"></a>Voir aussi



[Concepts MAPI](mapi-concepts.md)

