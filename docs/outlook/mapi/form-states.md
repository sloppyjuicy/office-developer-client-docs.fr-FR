---
title: États de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
ms.openlocfilehash: 2b1ab46aa7d81e229f9e984fce411e01c38d5b76
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373234"
---
# <a name="form-states"></a>États de formulaire

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les objets de formulaire peuvent être dans l’un des cinq états distincts, selon les méthodes qui y ont été appelées et selon si des erreurs se sont produites lors de l’utilisation de ces méthodes. Les états sont décrits dans les rubriques suivantes :
  
- [État nonnitialisé](uninitialized-state.md)
    
- [État normal](normal-state.md)
    
- [NoScribble State](noscribble-state.md)
    
- [HandsOffAfterSave, état](handsoffaftersave-state.md)
    
- [HandsOffFromNormal State](handsofffromnormal-state.md)
    
Les états concernent principalement l’état des données dans l’objet de formulaire. Les différents états indiquent si les données doivent être enregistrées, si l’objet de formulaire doit autoriser les modifications apportées aux données et à quel point dans le processus d’enregistrement des données se trouve le formulaire. En tant que tel, les états de formulaire et les transitions entre eux ont plus à faire avec l’implémentation de votre serveur de formulaires des méthodes d’interface [IPersistMessage : IUnknown](ipersistmessageiunknown.md) que les autres. La connaissance de ces états est très utile pour une implémentation correcte des interfaces de formulaire MAPI que votre serveur de formulaires doit implémenter. 
  
Les rubriques de cette section décrivent les différents états, ainsi que les actions autorisées qui provoquent des transitions vers d’autres états. Les transitions non répertoriées dans les rubriques ne sont pas autorisées. Si vos objets de formulaire font des transitions non possibles entre les états, ils ne se comporteront pas de la même façon que les clients de messagerie et pourraient entraîner un comportement imprévisible du client ou de l’objet formulaire.
  
> [!NOTE]
> Certaines transitions d’état dépendent des informations des états précédents. Votre serveur de formulaires devra probablement implémenter un indicateur dans ses objets de formulaire pour indiquer si les valeurs des propriétés du message ont été modifiées pour faciliter les changements d’état ultérieurs. 
  
## <a name="see-also"></a>Voir aussi

- [Développement de serveurs de formulaire MAPI](developing-mapi-form-servers.md)

