---
title: Fournisseurs de services MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1f931382e790da13e7d4a746e286d9dc176b7b6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571905"
---
# <a name="mapi-service-providers"></a>Fournisseurs de services MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Il existe trois principaux types de fournisseurs de services :
  
- Fournisseurs de carnet d’adresses.
    
- Fournisseurs de magasins de message.
    
- Fournisseurs de transport.
    
Fournisseurs de magasin de messages et du carnet d’adresses présentent de nombreuses similitudes. Ils inscrivent un identificateur unique MAPI qu’ils utilisent pour construire les identificateurs d’entrée pour leurs objets. Elles fournissent une hiérarchie d’objets et que les clients peuvent accéder et manipuler les propriétés. Pour les objets conteneur, elles prennent en charge une table de hiérarchie et une table des matières. Elles prennent en charge les notifications sur ces tables et éventuellement sur des objets individuels afin que les clients peuvent être informés des modifications qui se produisent pendant la session. Lorsque les opérations sont longues, ils peuvent afficher un indicateur de progression pour informer l’utilisateur de l’état de l’opération. Les clients peuvent communiquer avec des fournisseurs de banque de messages et du carnet d’adresse soit indirectement via MAPI à l’aide de la [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) et [IMAPISession : IUnknown](imapisessioniunknown.md) interfaces ou directement à l’aide d’une des interfaces de fournisseur de service dans la tableau suivant. 
  
|**Interfaces de fournisseur de carnet d’adresses**|**Interfaces de fournisseur de magasin de message**|
|:-----|:-----|
|[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList : IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser : IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage : IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach : IMAPIProp](iattachimapiprop.md) <br/> |
   
Fournisseurs de transport diffèrent auprès de fournisseurs de banque des messages et du carnet d’adresses de la façon de que communiquer avec MAPI et les clients. Fournisseurs de transport attendre généralement MAPI pour demander les informations plutôt que d’établir une communication. Contrairement aux autres fournisseurs, fournisseurs de transport ne prennent pas charge une variété de tables couramment utilisés par les clients et les objets. Toutefois, elles prennent en charge un objet état, tous les fournisseurs de services, et publier ses propriétés dans la table d’état. Tandis que les fournisseurs de magasins de messages et du carnet d’adresses appeler la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) pour enregistrer des identificateurs uniques pour construire les identificateurs d’entrée, fournisseurs de transport appellent la méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) Enregistrez les identificateurs uniques, ainsi que les types d’adresses pour responsabilité pour la remise de messages spécifiques. 
  
Votre fournisseur de services doit avoir les trois fichiers d’en-tête : un fichier d’en-tête public et deux fichiers internes. Utilisez le fichier d’en-tête public pour la configuration et de la documentation des propriétés et leurs valeurs. Inclure dans un des fichiers d’en-tête interne tous les publics MAPI en-têtes nécessaires ; Ce fichier d’en-tête doit être inclus dans l’ensemble de vos fichiers source du fournisseur de service. Utilisez l’autre fichier interne pour définir les identificateurs de ressource.
  
Carnet d’adresses, banque de messages et les fournisseurs de transport effectuent les tâches suivantes :
  
- Fournir une fonction de point d’entrée. 
    
- Fournir un fournisseur et un objet d’ouverture de session pour gérer l’ouverture de session et d’initialisation. 
    
- Si le fournisseur appartient à un service de message, fournir une fonction de point d’entrée de message service. 
    
- Configuration de la prise en charge par l’implémentation d’une feuille de propriétés.
    
- Mettre en œuvre un objet d’état et prise en charge de la table d’état. 
    
- Poignée arrêtée.
    
## <a name="see-also"></a>Voir aussi



[Concepts MAPI](mapi-concepts.md)

