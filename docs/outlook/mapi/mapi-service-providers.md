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
  
Il existe trois types de fournisseurs de services courants:
  
- Fournisseurs de carnet d'adresses.
    
- Fournisseurs de banques de messages.
    
- Fournisseurs de transport.
    
Les fournisseurs de carnet d'adresses et de banque de messages présentent beaucoup de similitudes. Ils enregistrent un identificateur unique avec MAPI qu'ils utilisent pour créer des identificateurs d'entrée pour leurs objets. Elles fournissent une hiérarchie des objets et des propriétés auxquels les clients peuvent accéder et manipuler. Pour leurs objets Container, ils prennent en charge une table de hiérarchie et une table des matières. Elles prennent en charge les notifications d'événement sur ces tables et éventuellement sur des objets individuels afin que les clients puissent être informés des modifications apportées au cours de la session. Lorsque les opérations deviennent longues, elles peuvent afficher un indicateur de progression pour informer l'utilisateur de l'état de l'opération. Les clients peuvent communiquer avec les fournisseurs de carnet d'adresses et de banque de messages soit indirectement via MAPI à l'aide des interfaces [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) et [IMAPISession: IUnknown](imapisessioniunknown.md) , soit directement à l'aide de l'une des interfaces du fournisseur de services dans le tableau suivant. 
  
|**Interfaces de fournisseur de carnet d'adresses**|**Interfaces du fournisseur de banque de messages**|
|:-----|:-----|
|[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList : IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser : IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage : IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach : IMAPIProp](iattachimapiprop.md) <br/> |
   
Les fournisseurs de transport diffèrent des fournisseurs de carnet d'adresses et de banque de messages dans la façon dont ils communiquent avec MAPI et avec les clients. Les fournisseurs de transport attendent généralement que MAPI les invite à entrer des informations au lieu d'initier la communication. Contrairement aux autres fournisseurs, les fournisseurs de transport ne prennent pas en charge un grand nombre d'objets et de tables fréquemment utilisés par les clients. Toutefois, ils prennent en charge un objet Status, tout comme les fournisseurs de services, et publient leurs propriétés dans le tableau d'État. Tandis que les fournisseurs de banques de messages et de carnets d'adresses appellent la méthode [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) pour enregistrer des identificateurs uniques pour la création de leurs identificateurs d'entrée, les fournisseurs de transport appellent la méthode [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) pour enregistrer des identificateurs uniques, ainsi que des types d'adresses pour la responsabilité de la remise de messages particuliers. 
  
Votre fournisseur de services doit avoir trois fichiers d'en-tête: un fichier d'en-tête public et deux fichiers internes. Utilisez le fichier d'en-tête public pour la configuration et pour la documentation des propriétés, ainsi que leurs valeurs. Incluez dans l'un des fichiers d'en-tête internes tous les en-têtes MAPI publics nécessaires; ce fichier d'en-tête doit être inclus dans tous les fichiers sources de votre fournisseur de services. Utilisez l'autre fichier interne pour définir des identificateurs de ressources.
  
Les fournisseurs de carnet d'adresses, de banque de messages et de transport effectuent les tâches suivantes:
  
- Fournissez une fonction de point d'entrée. 
    
- Fournissez un objet fournisseur et de connexion pour gérer l'ouverture et l'initialisation de l'ouverture de session. 
    
- Si le fournisseur appartient à un service de messagerie, fournissez une fonction de point d'entrée de service de messagerie. 
    
- Prendre en charge la configuration en implémentant une feuille de propriétés.
    
- Implémenter un objet d'État et prendre en charge la table d'État. 
    
- Handle arrêté.
    
## <a name="see-also"></a>Voir aussi



[Concepts MAPI](mapi-concepts.md)

