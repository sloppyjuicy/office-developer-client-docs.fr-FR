---
title: Implémentation de l’interface IClassFactory pour les serveurs de formulaires
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388048"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Implémentation de l’interface IClassFactory pour les serveurs de formulaires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) est l’interface OLE qui utilisent des applications clientes pour créer des objets de formulaire de classe de message du serveur de votre formulaire. Le tableau suivant répertorie les méthodes **IClassFactory** qui sont requis. 
  
|**Méthode**|**Description**|
|:-----|:-----|
|[CreateInstance](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |Crée un nouvel objet de formulaire.  <br/> |
|[LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |Verrouille le serveur de formulaire en mémoire afin que la surcharge de démarrage peut être évité lorsque plusieurs objets de formulaire sont créés.  <br/> |
   
Pour toutes les informations nécessaires pour implémenter ces méthodes, voir la section COM et ActiveX Object Services dans le SDK de Windows.
  
## <a name="see-also"></a>Voir aussi



[Écriture de code du serveur de formulaire](writing-form-server-code.md)

