---
title: Implémentation de l'interface IClassFactory pour les serveurs de formulaires
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310030"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Implémentation de l'interface IClassFactory pour les serveurs de formulaires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) est l'interface OLE utilisée par les applications clientes pour créer de nouveaux objets Form de la classe de message de votre serveur de formulaire. Le tableau suivant répertorie les méthodes **IClassFactory** requises. 
  
|**Méthode**|**Description**|
|:-----|:-----|
|[CreateInstance](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |Crée un nouvel objet Form.  <br/> |
|[LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |Verrouille le serveur de formulaires en mémoire afin que la charge de démarrage puisse être évitée lors de la création d'objets de formulaire.  <br/> |
   
Pour obtenir toutes les informations nécessaires à l'implémentation de ces méthodes, voir la section COM and ActiveX Object Services dans le kit de développement logiciel (SDK) Windows.
  
## <a name="see-also"></a>Voir aussi



[Écriture de code de serveur de formulaire](writing-form-server-code.md)

