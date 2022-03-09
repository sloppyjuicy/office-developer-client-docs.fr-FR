---
title: Mise en œuvre de la sécurité
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
ms.openlocfilehash: 8308420eff3775af3737ae5914a9b527797927f1
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375873"
---
# <a name="implementing-security"></a>Mise en œuvre de la sécurité

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si le système de messagerie en a besoin, le fournisseur de transport est responsable de l’implémentation d’un niveau de sécurité approprié pour l’accès au système de messagerie. Chaque message entrant ou sortant envoyé par le biais d’un fournisseur de transport par lepooler MAPI est géré dans le contexte d’une session d’ouverture de session de fournisseur. Le fournisseur de transport peut afficher une boîte de dialogue de connexion à l’utilisateur qui demande les informations d’identification d’un utilisateur avant d’établir une telle connexion. Le fournisseur de transport peut également stocker les informations d’identification précédemment entrées par l’utilisateur dans la plage de propriétés sécurisées d’une section de profil et les utiliser pour l’accès sans invite.
  
Lorsque vous implémentez la sécurité de votre fournisseur de transport, prenons en compte les considérations suivantes :
  
- Avec plusieurs fournisseurs de services installés, il peut y avoir une multitude de noms et de mots de passe associés à un utilisateur.
    
- MAPI autorise plusieurs sessions avec plusieurs identités. Les fournisseurs sont encouragés à prendre en charge plusieurs sessions, mais ne sont pas obligés de le faire.
    
- Chaque session avec un fournisseur de transport est associée par MAPI à une section discrète dans le profil de l’utilisateur. Le fournisseur de transport peut utiliser la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) pour accéder à cette section, qui peut être utilisée pour stocker les informations associées à cette session, y compris les informations d’identification. 
    
- Avec plusieurs fournisseurs de transport installés, il n’est pas nécessairement vrai que l’utilisateur dispose d’une seule adresse de messagerie. Un utilisateur peut avoir une adresse de messagerie distincte pour chaque fournisseur de transport installé ou avoir une adresse différente pour chaque session sur un seul fournisseur.
    
Pour plus d’informations sur le stockage des informations d’identification dans les sections de profil, voir [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect : IMAPIProp](iprofsectimapiprop.md).
  

