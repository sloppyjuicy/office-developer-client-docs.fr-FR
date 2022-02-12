---
title: Objets clients MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 11304a4c-d986-4ad9-a140-19a59825a8df
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 54d1c3fe856d9d12e39ef9637af38537e88f3b5e
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62778903"
---
# <a name="mapi-client-objects"></a>Objets clients MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes de messagerie standard implémentent un seul objet : un sink de conseil. Les réceptions de conseil héritent de l’interface [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) et sont utilisées par MAPI et les fournisseurs de services pour la notification d’événement. Certains clients implémentent également des objets de progression pour prendre en charge l’affichage des boîtes de dialogue de progression. 
  
Les clients plus complexes qui la prise en charge des formulaires personnalisés implémentent un autre objet de sink de conseil et quelques autres objets, tels que l’objet de site de message qui hérite de l’interface [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) et l’objet de contexte d’affichage qui hérite de l’interface [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) . L’objet de sink advise supplémentaire hérite de l’interface [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) . 
  
Le tableau suivant récapitule les objets MAPI implémentés par les clients de messagerie standard et les clients qui supportent l’affichage de formulaires personnalisés.
  
|**Objet client**|**Description**|
|:-----|:-----|
|Conseiller le sink  <br/> |Fournit une fonction de rappel pour les événements qui se produisent dans le magasin de messages, le carnet d’adresses ou la session. |
|Site de message  <br/> |Gère la manipulation des objets de formulaire. |
|Progression  <br/> |Affiche une boîte de dialogue pour afficher la progression d’une opération. |
|Afficher le dos à l’avis  <br/> |Fournit des fonctions de rappel pour les événements qui se produisent dans un formulaire. |
|Contexte d’affichage  <br/> |Prend en charge les commandes d’impression et d’enregistrement des formulaires et de navigation entre les formulaires. |
   
L’illustration suivante montre la relation entre ces différents objets clients, les interfaces dont ils héritent et les composants MAPI qui les utilisent. 
  
![Objets clients et interfaces correspondantes](media/amapi_65.gif "Objets clients et interfaces correspondantes")
  
Les clients utilisent beaucoup plus d’objets qu’ils n’implémentent. Tous les clients utilisent un objet de session pour accéder à un large éventail d’objets et d’objets fournisseur de services implémentés par MAPI. Les clients interagissent avec les fournisseurs de services indirectement, via la session, le carnet d’adresses ou les objets d’état que MAPI fournit, ou directement via une variété d’objets implémentés par des fournisseurs de services particuliers. Pour effectuer un contact direct avec des fournisseurs de carnets d’adresses, les clients utilisent des conteneurs de carnet d’adresses, des utilisateurs de messagerie et des listes de distribution. Pour accéder directement à un fournisseur de magasins de messages, les clients utilisent l’objet, les dossiers, les messages et les pièces jointes de la boutique de messages. Lorsque les fournisseurs de services supportent un objet d’état, les clients peuvent utiliser l’objet d’état pour surveiller l’état du fournisseur de services.
  
Les clients qui supportent la configuration du fournisseur de services et du service de messagerie utilisent trois objets implémentés par MAPI : l’objet d’administration du service de messagerie, l’objet d’administration de profil et l’objet d’administration du fournisseur. Les clients qui affichent des formulaires personnalisés utilisent plusieurs objets de formulaire qu’un fournisseur de bibliothèque de formulaires ou un serveur de formulaires implémente.
  
## <a name="see-also"></a>Voir aussi

- [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) 
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)  
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
- [Vue d’ensemble de l’interface et de l’objet MAPI](mapi-object-and-interface-overview.md)

