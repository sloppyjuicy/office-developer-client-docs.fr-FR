---
title: Objets de clients MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 11304a4c-d986-4ad9-a140-19a59825a8df
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fb37c15e6544798a956e865e6c8c6d62bee44d28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784588"
---
# <a name="mapi-client-objects"></a>Objets de clients MAPI
  
**S’applique à**: Outlook 
  
Applications clientes de messagerie standard n'implémentent qu’un seul objet, un récepteur de notifications. Récepteurs d’héritent de notification la [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) de l’interface et sont utilisés par MAPI et de service de fournisseurs de notification d’événement. Certains clients également implémentent des objets de l’avancement pour prendre en charge l’affichage des boîtes de dialogue de progression. 
  
Récepteur de clients plus complexes que prise en charge des formulaires personnalisés implémentent advise un autre objet et quelques autres objets, tels que l’objet de site de message qui hérite de la [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface et l’objet de contexte de vue qui hérite de la [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface. L’objet de récepteur advise supplémentaires hérite de la [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface. 
  
Le tableau suivant récapitule les objets MAPI implémentées par les clients de messagerie standards et par les clients qui prennent en charge l’affichage de formulaires personnalisés.
  
|**Objet client**|**Description**|
|:-----|:-----|
|Récepteur de notification  <br/> |Fournit une fonction de rappel pour les événements qui se produisent dans la banque de messages, carnet d’adresses ou la session.  <br/> |
|Site de message  <br/> |Gère la manipulation des objets de formulaire.  <br/> |
|Progress  <br/> |Affiche une boîte de dialogue pour afficher la progression d’une opération.  <br/> |
|Affichage de récepteur de notification  <br/> |Fournit des fonctions de rappel pour les événements qui se produisent dans un formulaire.  <br/> |
|Contexte de vue  <br/> |Prend en charge des commandes pour l’impression et l’enregistrement de formulaires et pour la navigation entre les formulaires.  <br/> |
   
L’illustration suivante montre la relation entre ces objets client différent, les interfaces à partir de laquelle ils héritent et les composants MAPI qui les utilisent. 
  
![Objets clients et interfaces correspondantes] (media/amapi_65.gif "Objets clients et interfaces correspondantes")
  
Les clients utilisent beaucoup plus d’objets qu’elles implémentent. Tous les clients utilisent un objet de session pour accéder à une grande variété d’objets de fournisseur de service et des objets implémentés par MAPI. Les clients interagissent avec les fournisseurs de services indirectement, par le biais de la session, le carnet d’adresses ou les objets d’état qui fournit MAPI, soit directement via un grand nombre d’objets qui implémentent des fournisseurs de service en particulier. Pour rendre le contact direct avec les fournisseurs de carnet d’adresses, les clients utilisent les conteneurs de carnet d’adresses, des listes de distribution et des utilisateurs de messagerie. Pour accéder à un fournisseur de banque de messages, les clients utilisent directement l’objet de banque de messages, les dossiers, les messages et les pièces jointes. Lorsque les fournisseurs de services prend en charge un objet état, les clients peuvent utiliser l’objet d’état pour surveiller l’état du fournisseur de services.
  
Les clients qui prennent en charge le fournisseur de services et de configuration du service de message utilisent trois objets implémentés par MAPI : les objet d’administration de service de message, un objet d’administration de profil et un objet d’administration de fournisseur. Les clients qui affichent des formulaires personnalisés utilisent plusieurs objets de formulaire qui implémente un fournisseur de bibliothèque de formulaire ou d’un serveur de formulaire.
  
## <a name="see-also"></a>Voir aussi

- [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) 
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)  
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
- [Objet MAPI et vue d’ensemble de l’Interface](mapi-object-and-interface-overview.md)

