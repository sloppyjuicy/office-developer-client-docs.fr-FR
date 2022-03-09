---
title: Mise en œuvre d’une interface de configuration pour les fournisseurs de magasins de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
ms.openlocfilehash: aed74737bc5f908531c852cdd8b80a94a1bcbd13
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372576"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>Mise en œuvre d’une interface de configuration pour les fournisseurs de magasins de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de magasins de messages sont requis pour implémenter une interface qui permet à l’utilisateur de configurer le fournisseur de magasin de messages pour qu’il s’exécute sur l’ordinateur de cet utilisateur. En règle générale, le fournisseur de magasin de messages est configuré lorsque le fournisseur de la boutique de messages est ajouté au profil d’un utilisateur. L’interface de configuration du fournisseur de magasins de messages gère généralement des tâches telles que la définition des noms d’utilisateur et des mots de passe pour les magasins de messages protégés, le choix des chemins d’accès aux fichiers nécessaires et la création du mécanisme de stockage sous-jacent qu’il utilisera, si nécessaire.
  
L’interface de configuration que vous implémentez est accessible via des points d’entrée supplémentaires dans la DLL de votre fournisseur de services de messagerie. Pour plus d’informations, [voir Configuring a Message Service](configuring-a-message-service.md). L’interface de configuration du fournisseur de magasin de messages est la seule interface utilisateur qu’un fournisseur de magasin de messages doit implémenter.
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

