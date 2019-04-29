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
ms.openlocfilehash: c430160ee508a86f36d840c7916c0516cfc10fbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417286"
---
# <a name="implementing-security"></a>Implémentation de la sécurité

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si le système de messagerie l'exige, le fournisseur de transport est responsable de l'implémentation d'un niveau de sécurité approprié pour l'accès au système de messagerie. Chaque message entrant ou sortant envoyé par le biais d'un fournisseur de transport par le spouleur MAPI est géré dans le contexte d'une session de connexion du fournisseur. Le fournisseur de transport peut afficher une boîte de dialogue de connexion à l'utilisateur qui demande les informations d'identification d'un utilisateur avant d'établir une telle connexion. En guise d'alternative, le fournisseur de transport peut stocker les informations d'identification précédemment saisies de l'utilisateur dans la plage de propriétés sécurisée au sein d'une section de profil et les utiliser pour l'accès sans invite.
  
Lors de l'implémentation de la sécurité de votre fournisseur de transport, prenez en compte les éléments suivants:
  
- Avec plusieurs fournisseurs de services installés, il peut y avoir une multitude de noms et de mots de passe associés à un utilisateur.
    
- MAPI autorise plusieurs sessions avec plusieurs identités. Les fournisseurs sont encouragés à prendre en charge plusieurs sessions, mais ne sont pas tenus de le faire.
    
- Chaque session avec un fournisseur de transport est associée à MAPI avec une section discrète dans le profil de l'utilisateur. Le fournisseur de transport peut utiliser la méthode [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) pour accéder à cette section, qui peut être utilisée pour stocker les informations associées à cette session, notamment les informations d'identification. 
    
- Avec plusieurs fournisseurs de transport installés, il n'est pas nécessairement vrai que l'utilisateur ne possède qu'une seule adresse de messagerie. Un utilisateur peut avoir une adresse de messagerie distincte pour chaque fournisseur de transport installé ou peut avoir une adresse différente pour chaque session sur un fournisseur unique.
    
Pour plus d'informations sur le stockage des informations d'identification dans les sections de profil, consultez la rubrique [messages services and](message-services-and-profiles.md) Profiles and [IProfSect: IMAPIProp](iprofsectimapiprop.md).
  

