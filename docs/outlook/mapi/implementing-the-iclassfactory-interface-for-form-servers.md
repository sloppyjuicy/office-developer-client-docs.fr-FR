---
title: Implémentation de l’Interface IClassFactory pour les serveurs de formulaire
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3ecae23d8631c818fb3d1c6786b2d180e9f32a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784198"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Implémentation de l’Interface IClassFactory pour les serveurs de formulaire

  
  
**S’applique à**: Outlook 
  
[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) est l’interface OLE qui utilisent des applications clientes pour créer des objets de formulaire de classe de message du serveur de votre formulaire. Le tableau suivant répertorie les méthodes **IClassFactory** qui sont requis. 
  
|**Méthode**|**Description**|
|:-----|:-----|
|[CreateInstance](http://msdn.microsoft.com/en-us/library/ms682215%28v=VS.85%29.aspx) <br/> |Crée un nouvel objet de formulaire.  <br/> |
|[LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) <br/> |Verrouille le serveur de formulaire en mémoire afin que la surcharge de démarrage peut être évité lorsque plusieurs objets de formulaire sont créés.  <br/> |
   
Pour toutes les informations nécessaires pour implémenter ces méthodes, voir la section COM et ActiveX Object Services dans le SDK de Windows.
  
## <a name="see-also"></a>Voir aussi



[Écriture de Code de formulaire Server](writing-form-server-code.md)

