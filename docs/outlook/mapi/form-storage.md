---
title: Stockage des formulaires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ddf9158-3c10-408a-aeaf-5a382c4339e7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 793a34b093ba69f73be7e186bec0a769584bbac4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414892"
---
# <a name="form-storage"></a>Stockage des formulaires

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Bien qu’il ne soit pas nécessaire de connaître tous les détails de la façon dont les formulaires sont stockés physiquement, il est utile de comprendre quelques-uns des concepts principaux. Par conséquent, avant de décrire les trois types de bibliothèques de formulaires pris en charge par le gestionnaire de formulaires par défaut, cette rubrique donne une vue d’ensemble de la façon dont les formulaires sont stockés.
  
Les définitions de formulaire peuvent être stockées physiquement dans des dossiers dans une ou plusieurs magasins de messages MAPI. Chaque dossier MAPI peut être pensé comme ayant deux zones pour le stockage des objets de message : la partie standard et la partie associée. La partie standard du dossier inclut les messages et dossiers que les utilisateurs manipulent.
  
La partie associée inclut les objets de message masqués qui sont associés au dossier, y compris les définitions de formulaire, les affichages, les modèles de règles, les modèles de réponse, etc. Cette autre partie est appelée table des matières associée au dossier et l’ensemble des messages de la table des matières associée est appelé informations associées au dossier. Les messages masqués font partie intégrante du dossier et sont copiés avec le contenu standard du dossier lorsque le dossier est copié. Bien que stockées physiquement sous forme de messages, les informations de la table des matières associée d’un dossier se comportent plus comme des propriétés que comme des messages consultables. Tout objet dossier qui prend en charge une table des matières associée est capable de stocker des formulaires personnalisés. La méthode [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) peut renvoyer le contenu standard ou le contenu associé du dossier, selon la valeur du paramètre  _lags_ de la méthode. 
  
Une bibliothèque de formulaires se compose de définitions de formulaire stockées dans la table des matières associée d’un dossier. La définition du formulaire inclut les propriétés du formulaire, les actions prises en charge par le formulaire et même le fichier exécutable du serveur de formulaires, qui est stocké sous forme de pièces jointes de message.
  
En outre, les formulaires peuvent être stockés dans n’importe quel fichier ou emplacement que le gestionnaire de formulaires utilisé prend en charge. Le gestionnaire de formulaires par défaut stocke les serveurs de formulaires dans des dossiers MAPI, mais un gestionnaire de formulaires personnalisé peut implémenter son propre stockage pour les serveurs de formulaires.
  
Un formulaire peut avoir plusieurs interfaces utilisateur liées à sa classe de message. Par exemple, un formulaire peut avoir des interfaces utilisateur de composition et de lecture distinctes. Le formulaire prend en charge l’appel de l’interface utilisateur appropriée pour différentes demandes utilisateur, selon les verbes du formulaire appelés. Par exemple, si votre serveur de formulaires dispose d’interfaces utilisateur de composition et de lecture distinctes, l’interface utilisateur Composer peut être ouverte automatiquement lorsque l’utilisateur crée un message de la classe de message du formulaire et que l’interface utilisateur lecture peut être ouverte automatiquement lorsque l’utilisateur ouvre un message existant de la classe de message du formulaire.
  
La plupart des informations stockées dans une définition de formulaire sont disponibles en invoquant la méthode [IMAPIFormInfo::IMAPIProp](imapiforminfoimapiprop.md) sur un objet **IMAPIFormInfo.** **L’interface IMAPIFormInfo** simplifie l’accès aux informations de formulaire en appelant tous les dossiers MAPI et les méthodes de message nécessaires pour récupérer les informations. Un **objet IMAPIFormInfo** peut être obtenu en appelant la méthode [IMAPIFormContainer::ResolveMessageClass.](imapiformcontainer-resolvemessageclass.md) 
  
Les trois types de bibliothèques de formulaires sont décrits dans les rubriques Bibliothèques de [formulaires locales,](local-form-libraries.md)Bibliothèques de formulaires de [dossiers](folder-form-libraries.md) et Bibliothèques de [formulaires personnels.](personal-form-libraries.md)
  
## <a name="see-also"></a>Voir aussi

- [Formulaires MAPI](mapi-forms.md)

