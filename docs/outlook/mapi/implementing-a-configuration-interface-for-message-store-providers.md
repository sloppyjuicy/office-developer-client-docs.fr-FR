---
title: Mise en œuvre d’une interface de configuration pour les fournisseurs de magasins de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 56ef4e25ad432acc42959aa1b6034ad0c02add31
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575651"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>Mise en œuvre d’une interface de configuration pour les fournisseurs de magasins de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de magasins de messages sont requis pour implémenter une interface qui permet à l’utilisateur de configurer le fournisseur de magasin de messages pour qu’il s’exécute sur l’ordinateur de cet utilisateur. En règle générale, le fournisseur de la boutique de messages est configuré lorsque le fournisseur de la boutique de messages est ajouté au profil d’un utilisateur. L’interface de configuration du fournisseur de magasins de messages gère généralement des tâches telles que la définition des noms d’utilisateur et des mots de passe pour les magasins de messages protégés, le choix des chemins d’accès aux fichiers nécessaires et la création du mécanisme de stockage sous-jacent qu’il utilisera, si nécessaire.
  
L’interface de configuration que vous implémentez est accessible via des points d’entrée supplémentaires dans la DLL de votre fournisseur de services de messagerie. Pour plus d’informations, [voir Configuring a Message Service](configuring-a-message-service.md). L’interface de configuration du fournisseur de magasins de messages est la seule interface utilisateur qu’un fournisseur de magasins de messages doit implémenter.
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

