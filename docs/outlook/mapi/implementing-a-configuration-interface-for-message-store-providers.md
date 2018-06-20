---
title: Implémentation d’une Interface de Configuration pour les fournisseurs de banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f7151841eef180a78a13ad161d197af783decfb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784139"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>Implémentation d’une Interface de Configuration pour les fournisseurs de banque de messages

  
  
**S’applique à**: Outlook 
  
Fournisseurs de magasins de message sont requis pour implémenter une interface qui permet à l’utilisateur de configurer le fournisseur de banque de messages à exécuter sur l’ordinateur de l’utilisateur. En règle générale, le fournisseur de banque de messages est configuré lorsque le fournisseur de banque de message est ajouté à un profil utilisateur. Interface de configuration du fournisseur de banque de messages gère généralement les tâches telles que la définition des noms d’utilisateur et mots de passe pour les magasins de message protégé, choix des chemins d’accès aux fichiers nécessaires, et création de mécanisme de stockage sous-jacent qu’il utilise, si nécessaire.
  
Vous implémentez l’interface de configuration est accessible via les points d’entrée supplémentaires dans une DLL de votre fournisseur de service de message. Pour plus d’informations, voir [configuration d’un Service de Message](configuring-a-message-service.md). Interface de configuration du fournisseur de banque de messages est la seule interface utilisateur qu’un fournisseur de magasin de message doit implémenter.
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

