---
title: Implémentation de la sécurité
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c2926e7c94178d5a3135f34e2ab3b3ae11d145dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568482"
---
# <a name="implementing-security"></a>Implémentation de la sécurité

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Si le système de messagerie a besoin, le fournisseur de transport est responsable de la mise en œuvre d’un niveau de sécurité pour l’accès au système de messagerie approprié. Chaque message entrant ou sortant envoyé via un fournisseur de transport par le spouleur MAPI est géré dans le contexte d’une session d’ouverture de session du fournisseur. Le fournisseur de transport peut afficher une boîte de dialogue d’ouverture de session à l’utilisateur qui vous invite à fournir les informations d’identification d’un utilisateur avant d’établir une connexion de ce type. Sinon, le fournisseur de transport peut stocker les informations d’identification entrées précédemment dans la plage de la propriété sécurisée dans une section de profil et les utiliser pour l’accès sans demander de confirmation.
  
Lorsque vous implémentez la sécurité de votre fournisseur de transport, considérez les points suivants :
  
- Avec plusieurs fournisseurs de service installé, il peut y avoir une multitude de noms et mots de passe associés à un utilisateur.
    
- MAPI permet à plusieurs sessions avec plusieurs identités. Les fournisseurs sont invités à prendre en charge plusieurs sessions mais ne sont pas nécessaires à le faire.
    
- Chaque session avec un fournisseur de transport est associée à MAPI une section discrète dans le profil utilisateur. Le fournisseur de transport peut utiliser la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) pour accéder à cette section, qui peut être utilisée pour stocker les informations relatives liés cette session, y compris les informations d’identification. 
    
- Avec plusieurs fournisseurs de transport installé, il n’est pas nécessairement vrai que l’utilisateur n’a qu’une adresse de messagerie unique. Un utilisateur peut avoir une adresse de messagerie distinct pour chaque fournisseur de transport installés ou permettre avoir une adresse différente pour chaque session sur un seul fournisseur.
    
Pour plus d’informations sur le stockage des informations d’identification dans les sections de profil, voir [Services de messagerie et les profils](message-services-and-profiles.md) et [IProfSect : IMAPIProp](iprofsectimapiprop.md).
  

