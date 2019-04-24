---
title: États de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 61d20ff7010151a82c53cafc69270e6925796a5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327516"
---
# <a name="form-states"></a>États de formulaire

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les objets Form peuvent être dans l'un des cinq États distincts, en fonction des méthodes qui ont été appelées et si des erreurs se sont produites lors de l'exécution de ces méthodes. Les États sont décrits dans les rubriques suivantes:
  
- [État non initialisé](uninitialized-state.md)
    
- [État normal](normal-state.md)
    
- [État noScribble](noscribble-state.md)
    
- [État HandsOffAfterSave](handsoffaftersave-state.md)
    
- [État HandsOffFromNormal](handsofffromnormal-state.md)
    
Les États sont principalement liés à l'état des données dans l'objet Form. Les différents États indiquent si les données doivent être enregistrées, si l'objet Form doit autoriser les modifications apportées aux données et le moment où se trouve le formulaire. En tant que telles, les États de formulaire et les transitions entre eux ont davantage à faire avec l'implémentation de IPersistMessage Server de votre serveur de formulaires: les méthodes d'interface [IUnknown](ipersistmessageiunknown.md) que n'importe quel autre. La connaissance de ces États est très utile pour mettre en œuvre correctement les interfaces de formulaire MAPI que votre serveur de formulaire doit implémenter. 
  
Les rubriques de cette section décrivent les différents États, ainsi que les actions autorisées entraînant des transitions vers d'autres États. Les transitions non répertoriées dans les rubriques ne sont pas autorisées. Si vos objets de formulaire effectuent des transitions non autorisées entre les États, ils ne se comportent pas de la façon dont les clients de messagerie attendent et peuvent entraîner un comportement imprévisible du client ou de l'objet de formulaire.
  
> [!NOTE]
> Certaines transitions d'État dépendent des informations des États précédents. Votre serveur de formulaire devra probablement implémenter un indicateur dans ses objets de formulaire pour indiquer si les valeurs des propriétés du message ont été modifiées afin de faciliter les modifications ultérieures à l'État. 
  
## <a name="see-also"></a>Voir aussi

- [Développement de serveurs de formulaires MAPI](developing-mapi-form-servers.md)

