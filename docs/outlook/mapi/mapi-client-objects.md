---
title: Objets clients MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 11304a4c-d986-4ad9-a140-19a59825a8df
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6e78c80d861a5a56584bfb03bfdf2895efde8730
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319287"
---
# <a name="mapi-client-objects"></a>Objets clients MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes de messagerie standard implémentent un seul objet, un récepteur de Conseil. Les récepteurs de notification héritent de l'interface [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) et sont utilisés par MAPI et les fournisseurs de services pour la notification d'événement. Certains clients implémentent également des objets de progression pour prendre en charge l'affichage des boîtes de dialogue de progression. 
  
Les clients plus complexes qui prennent en charge les formulaires personnalisés implémentent un autre objet de récepteur de notification et quelques autres objets, tels que l'objet de site de messagerie qui hérite de l'interface [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) et l'objet de contexte d'affichage qui hérite de la [IMAPIViewContext: interface IUnknown](imapiviewcontextiunknown.md) . L'objet de récepteur de Conseil supplémentaire hérite de l'interface [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) . 
  
Le tableau suivant récapitule les objets MAPI implémentés par les clients de messagerie standard et par les clients qui prennent en charge l'affichage des formulaires personnalisés.
  
|**Objet client**|**Description**|
|:-----|:-----|
|Récepteur de notifications  <br/> |Fournit une fonction de rappel pour les événements qui se produisent dans la Banque de messages, le carnet d'adresses ou la session.  <br/> |
|Site de messagerie  <br/> |Gère la manipulation des objets Form.  <br/> |
|Progression  <br/> |Affiche une boîte de dialogue qui indique la progression d'une opération.  <br/> |
|Afficher le récepteur de notifications  <br/> |Fournit des fonctions de rappel pour les événements qui se produisent dans un formulaire.  <br/> |
|Contexte d'affichage  <br/> |Prend en charge les commandes pour l'impression et l'enregistrement des formulaires et pour la navigation entre les formulaires.  <br/> |
   
L'illustration suivante montre la relation entre ces différents objets client, les interfaces dont ils héritent et les composants MAPI qui les utilisent. 
  
![Objets clients et interfaces correspondantes] (media/amapi_65.gif "Objets clients et interfaces correspondantes")
  
Les clients utilisent beaucoup plus d'objets qu'ils ne l'implémentent. Tous les clients utilisent un objet session pour accéder à un grand nombre d'objets fournisseurs de services et d'objets implémentés par MAPI. Les clients interagissent avec les fournisseurs de services indirectement, via la session, le carnet d'adresses ou les objets d'état fournis par MAPI, ou directement par le biais d'un éventail d'objets implémentés par des fournisseurs de services particuliers. Pour effectuer un contact direct avec des fournisseurs de carnet d'adresses, les clients utilisent des conteneurs de carnet d'adresses, des utilisateurs de messagerie et des listes de distribution. Pour accéder directement à un fournisseur de banque de messages, les clients utilisent l'objet de banque de messages, les dossiers, les messages et les pièces jointes. Lorsque les fournisseurs de services prennent en charge un objet d'État, les clients peuvent utiliser l'objet d'État pour surveiller l'état du fournisseur de services.
  
Les clients qui prennent en charge la configuration du fournisseur de services et du service de messagerie utilisent trois objets implémentés par MAPI: l'objet d'administration du service de messagerie, l'objet d'administration des profils et l'objet d'administration du fournisseur. Les clients qui affichent des formulaires personnalisés utilisent plusieurs objets de formulaire implémentés par un fournisseur de bibliothèque de formulaires ou un serveur de formulaire.
  
## <a name="see-also"></a>Voir aussi

- [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) 
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)  
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
- [Vue d'ensemble de l'objet et de l'interface MAPI](mapi-object-and-interface-overview.md)

