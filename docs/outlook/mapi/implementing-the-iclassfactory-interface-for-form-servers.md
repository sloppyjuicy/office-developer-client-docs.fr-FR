---
title: Mise en œuvre de l’interface IClassFactory pour les serveurs de formulaires
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d123da963a07c60c4c43bf460607bdf51a11ad50
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776318"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Mise en œuvre de l’interface IClassFactory pour les serveurs de formulaires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
[IClassFactory est l’interface](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) OLE que les applications clientes utilisent pour créer des objets de formulaire de la classe de message de votre serveur de formulaires. Le tableau suivant **répertorie les méthodes IClassFactory** qui sont requises. 
  
|**Méthode**|**Description**|
|:-----|:-----|
|[CreateInstance](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |Crée un objet de formulaire. |
|[LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |Verrouille le serveur de formulaires en mémoire afin d’éviter la surcharge de démarrage lors de la création de plusieurs objets de formulaire. |
   
Pour toutes les informations nécessaires pour implémenter ces méthodes, voir la section COM et ActiveX Object Services dans le SDK Windows.
  
## <a name="see-also"></a>Voir aussi



[Écriture de code serveur de formulaire](writing-form-server-code.md)

