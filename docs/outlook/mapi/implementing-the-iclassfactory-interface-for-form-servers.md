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
ms.openlocfilehash: 5532cfc248d170952b45ba5a449f2e81a443f705
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551253"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Mise en œuvre de l’interface IClassFactory pour les serveurs de formulaires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
[IClassFactory est l’interface](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) OLE que les applications clientes utilisent pour créer des objets de formulaire de la classe de message de votre serveur de formulaires. Le tableau suivant répertorie **les méthodes IClassFactory** qui sont requises. 
  
|**Méthode**|**Description**|
|:-----|:-----|
|[CreateInstance](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |Crée un objet de formulaire.  <br/> |
|[LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |Verrouille le serveur de formulaires en mémoire afin d’éviter la surcharge de démarrage lors de la création de plusieurs objets de formulaire.  <br/> |
   
Pour toutes les informations nécessaires pour implémenter ces méthodes, voir la section COM et ActiveX Object Services dans Windows SDK.
  
## <a name="see-also"></a>Voir aussi



[Écriture de code serveur de formulaires](writing-form-server-code.md)

