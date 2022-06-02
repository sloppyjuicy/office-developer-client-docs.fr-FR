---
title: Fournisseurs de services MAPI
description: 'Décrit les trois fournisseurs de services MAPI : fournisseurs de carnets d’adresses, fournisseurs de magasins de messages et fournisseurs de transport.'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
ms.openlocfilehash: efc709e9746145f4e6e8eee8d13e2c79e09b9ef6
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828247"
---
# <a name="mapi-service-providers"></a>Fournisseurs de services MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe trois types courants de fournisseurs de services :
  
- Fournisseurs de carnets d’adresses.
    
- Fournisseurs de magasin de messages.
    
- Fournisseurs de transport.
    
Les fournisseurs de carnets d’adresses et de magasins de messages présentent de nombreuses similitudes. Ils inscrivent un identificateur unique avec MAPI qu’ils utilisent pour construire des identificateurs d’entrée pour leurs objets. Ils fournissent une hiérarchie d’objets et de propriétés auxquelles les clients peuvent accéder et manipuler. Pour leurs objets conteneur, ils prennent en charge une table de hiérarchie et une table de contenu. Ils prennent en charge la notification d’événements sur ces tables et éventuellement sur des objets individuels afin que les clients puissent être informés des modifications qui se produisent pendant la session. Lorsque les opérations deviennent longues, elles peuvent afficher un indicateur de progression pour informer l’utilisateur de l’état de l’opération. Les clients peuvent communiquer avec les fournisseurs de carnet d’adresses et de magasins de messages indirectement via MAPI à l’aide de [l’IAddrBook : IMAPIProp](iaddrbookimapiprop.md) et [IMAPISession : interfaces IUnknown](imapisessioniunknown.md) ou directement à l’aide de l’une des interfaces du fournisseur de services dans le tableau suivant. 
  
|**Interfaces du fournisseur de carnet d’adresses**|**Interfaces du fournisseur du magasin de messages**|
|:-----|:-----|
|[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList : IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser : IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage : IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach : IMAPIProp](iattachimapiprop.md) <br/> |
   
Les fournisseurs de transport diffèrent des fournisseurs de carnets d’adresses et de magasins de messages dans la façon dont ils communiquent avec MAPI et avec les clients. Les fournisseurs de transport attendent généralement que MAPI les invite à entrer des informations plutôt que de lancer la communication. Contrairement aux autres fournisseurs, les fournisseurs de transport ne prennent pas en charge une variété d’objets et de tables couramment accessibles par les clients. Toutefois, ils prennent en charge un objet d’état, comme tous les fournisseurs de services, et publient ses propriétés dans la table d’état. Alors que les fournisseurs de carnets d’adresses et de magasins de messages appellent la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) pour inscrire des identificateurs uniques pour la construction de leurs identificateurs d’entrée, les fournisseurs de transport appellent la méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) pour inscrire des identificateurs uniques, ainsi que des types d’adresses pour assumer la responsabilité de la remise de messages particuliers. 
  
Votre fournisseur de services doit avoir trois fichiers d’en-tête : un fichier d’en-tête public et deux fichiers internes. Utilisez le fichier d’en-tête public pour la configuration et la documentation des propriétés et de leurs valeurs. Inclure dans l’un des fichiers d’en-tête internes tous les en-têtes MAPI publics nécessaires ; ce fichier d’en-tête doit être inclus dans tous les fichiers sources de votre fournisseur de services. Utilisez l’autre fichier interne pour définir des identificateurs de ressources.
  
Le carnet d’adresses, le magasin de messages et les fournisseurs de transport effectuent les tâches suivantes :
  
- Fournissez une fonction de point d’entrée. 
    
- Fournissez un fournisseur et un objet d’ouverture de session pour gérer l’ouverture de session et l’initialisation. 
    
- Si le fournisseur appartient à un service de message, fournissez une fonction de point d’entrée de service de message. 
    
- Prise en charge de la configuration en implémentant une feuille de propriétés.
    
- Implémentez un objet d’état et prenez en charge la table d’état. 
    
- Handle shut down.
    
## <a name="see-also"></a>Voir aussi



[Concepts MAPI](mapi-concepts.md)

