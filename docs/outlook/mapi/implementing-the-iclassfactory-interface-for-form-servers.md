---
title: Implémentation de l’interface IClassFactory pour les serveurs de formulaires
description: IClassFactory est l’interface OLE que les applications clientes utilisent pour créer des objets de formulaire de la classe de message de votre serveur de formulaires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
ms.openlocfilehash: d2013469203f68939d7f0eccfe78ea4074b1e63f
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828410"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Implémentation de l’interface IClassFactory pour les serveurs de formulaires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) est l’interface OLE que les applications clientes utilisent pour créer des objets de formulaire de la classe de message de votre serveur de formulaires. Le tableau suivant répertorie les méthodes **IClassFactory** requises. 
  
|**Méthode**|**Description**|
|:-----|:-----|
|[CreateInstance](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |Crée un objet de formulaire. |
|[LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |Verrouille le serveur de formulaires en mémoire afin que la surcharge de démarrage puisse être évitée lors de la création de plusieurs objets de formulaire. |
   
Pour toutes les informations nécessaires à l’implémentation de ces méthodes, consultez la section COM et ActiveX Object Services dans le SDK Windows.
  
## <a name="see-also"></a>Voir aussi



[Écriture du code du serveur de formulaires](writing-form-server-code.md)

