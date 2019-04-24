---
title: Implémentation d'une interface de configuration pour les fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c349a03b0be465ed1262712372b6ee17a9812abd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332976"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>Implémentation d'une interface de configuration pour les fournisseurs de banques de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de banque de messages doivent implémenter une interface qui permet à l'utilisateur de configurer le fournisseur de banque de messages pour qu'il s'exécute sur l'ordinateur de cet utilisateur. En règle générale, le fournisseur de banque de messages est configuré lorsque le fournisseur de banque de messages est ajouté au profil d'un utilisateur. L'interface de configuration du fournisseur de banque de messages gère généralement des tâches telles que la définition des noms d'utilisateur et des mots de passe pour les banques de messages protégées, le choix des chemins d'accès aux fichiers nécessaires et la création du mécanisme de stockage sous-jacent qu'il utilisera, le cas échéant.
  
L'interface de configuration que vous implémentez est accessible par le biais de points d'entrée supplémentaires dans la DLL de votre fournisseur de services de messagerie. Pour plus d'informations, consultez [la rubrique Configuration d'un service de messagerie](configuring-a-message-service.md). L'interface de configuration du fournisseur de banque de messages est la seule interface utilisateur qu'un fournisseur de banque de messages doit implémenter.
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

