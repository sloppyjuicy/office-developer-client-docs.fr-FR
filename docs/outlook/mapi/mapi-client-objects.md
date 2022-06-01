---
title: Objets clients MAPI
description: Décrit et résume les objets MAPI implémentés par les clients de messagerie standard et par les clients qui prennent en charge l’affichage des formulaires personnalisés.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 11304a4c-d986-4ad9-a140-19a59825a8df
ms.openlocfilehash: b1c12a49bc821b121da40c006034b0d423f7f1a5
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812060"
---
# <a name="mapi-client-objects"></a>Objets clients MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes de messagerie standard implémentent un seul objet : un récepteur de conseils. Les récepteurs de conseils héritent de l’interface [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) et sont utilisés par MAPI et les fournisseurs de services pour la notification d’événements. Certains clients implémentent également des objets de progression pour prendre en charge l’affichage des boîtes de dialogue de progression. 
  
Les clients plus complexes qui prennent en charge les formulaires personnalisés implémentent un autre objet récepteur de conseils et quelques autres objets, tels que l’objet de site de message qui hérite de l’interface [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) et l’objet de contexte de vue qui hérite de l’interface [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) . L’objet récepteur conseiller supplémentaire hérite de l’interface [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) . 
  
Le tableau suivant récapitule les objets MAPI implémentés par les clients de messagerie standard et par les clients qui prennent en charge l’affichage des formulaires personnalisés.
  
|**Objet client**|**Description**|
|:-----|:-----|
|Conseiller le récepteur  <br/> |Fournit une fonction de rappel pour les événements qui se produisent dans le magasin de messages, le carnet d’adresses ou la session. |
|Site de message  <br/> |Gère la manipulation des objets de formulaire. |
|Progression  <br/> |Affiche une boîte de dialogue pour afficher la progression d’une opération. |
|Afficher le récepteur de conseils  <br/> |Fournit des fonctions de rappel pour les événements qui se produisent dans un formulaire. |
|Contexte d’affichage  <br/> |Prend en charge les commandes d’impression et d’enregistrement de formulaires et de navigation entre les formulaires. |
   
L’illustration suivante montre la relation entre ces différents objets clients, les interfaces dont ils héritent et les composants MAPI qui les utilisent. 
  
![Objets clients et interfaces correspondantes](media/amapi_65.gif "Objets clients et interfaces correspondantes")
  
Les clients utilisent beaucoup plus d’objets qu’ils n’implémentent. Tous les clients utilisent un objet de session pour accéder à un large éventail d’objets et d’objets de fournisseur de services implémenté par MAPI. Les clients interagissent avec les fournisseurs de services indirectement, par le biais de la session, du carnet d’adresses ou des objets d’état que MAPI fournit, ou directement par le biais d’une variété d’objets implémenté par des fournisseurs de services particuliers. Pour établir un contact direct avec les fournisseurs de carnets d’adresses, les clients utilisent des conteneurs de carnets d’adresses, des utilisateurs de messagerie et des listes de distribution. Pour accéder directement à un fournisseur de magasin de messages, les clients utilisent l’objet, les dossiers, les messages et les pièces jointes du magasin de messages. Lorsque les fournisseurs de services prennent en charge un objet d’état, les clients peuvent utiliser l’objet d’état pour surveiller l’état du fournisseur de services.
  
Les clients qui prennent en charge le fournisseur de services et la configuration du service de message utilisent trois objets implémentées par MAPI : l’objet d’administration du service de message, l’objet d’administration de profil et l’objet d’administration du fournisseur. Les clients qui affichent des formulaires personnalisés utilisent plusieurs objets de formulaire implémenté par un fournisseur de bibliothèque de formulaires ou un serveur de formulaires.
  
## <a name="see-also"></a>Voir aussi

- [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) 
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)  
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
- [Vue d’ensemble de l’objet et de l’interface MAPI](mapi-object-and-interface-overview.md)

