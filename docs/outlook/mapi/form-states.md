---
title: États de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 195a82bfcc163ee01d2d42c71e79a8f5c9c620e5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564632"
---
# <a name="form-states"></a>États de formulaire

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Objets de formulaire peuvent être l’un des cinq états distincts, en fonction de quelles méthodes ont été appelées y et si des erreurs se sont produites dans l’exécution de ces méthodes. Les États sont décrits dans les rubriques suivantes :
  
- [État non initialisé](uninitialized-state.md)
    
- [État normal](normal-state.md)
    
- [État NoScribble](noscribble-state.md)
    
- [État HandsOffAfterSave](handsoffaftersave-state.md)
    
- [État HandsOffFromNormal](handsofffromnormal-state.md)
    
Les États concernent principalement l’état des données de l’objet form. Si les données doivent être enregistrés, si l’objet form doit autoriser les modifications apportées aux données et quel point en cours de l’enregistrement des données en que du formulaire est de refléter les différents états. De ce fait, les transitions entre les États de formulaire ont plus faire de l’implémentation du serveur de votre formulaire de [IPersistMessage : IUnknown](ipersistmessageiunknown.md) que d’autres méthodes de l’interface. La base de connaissances de ces États est très utile pour la bonne mise en oeuvre des interfaces de formulaire MAPI que votre serveur de formulaire doit implémenter. 
  
Les rubriques de cette section décrivent les différents états possibles, ainsi que les actions autorisées qui provoquent des transitions vers d’autres États. Toute transition ne pas répertoriée dans les rubriques n’est pas autorisées. Si vos objets formulaire apportez non autorisées transitions entre les États, ils seront comporte pas comme que les clients de messagerie prévoient et peuvent entraîner des comportement imprévisible de l’objet client ou un formulaire.
  
> [!NOTE]
> Transitions d’état dépendent des informations issues des États précédents. Serveur de votre formulaire aura probablement implémenter un indicateur dans ses objets formulaire pour indiquer si les valeurs des propriétés du message ont été modifiés pour faciliter les modifications ultérieures de l’état. 
  
## <a name="see-also"></a>Voir aussi

- [Développement de serveurs de formulaires MAPI](developing-mapi-form-servers.md)

