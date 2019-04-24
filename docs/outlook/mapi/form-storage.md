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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328083"
---
# <a name="form-storage"></a>Stockage des formulaires

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Bien qu'il ne soit pas nécessaire de connaître tous les détails du stockage physique des formulaires, il est utile de comprendre quelques-uns des principaux concepts. Par conséquent, avant de décrire les trois types de bibliothèques de formulaires pris en charge par le gestionnaire de formulaires par défaut, cette rubrique offre une vue d'ensemble du mode de stockage des formulaires.
  
Les définitions de formulaire peuvent être physiquement stockées dans des dossiers dans une ou plusieurs banques de messages MAPI. Chaque dossier MAPI peut être considéré comme présentant deux zones de stockage des objets de message: la partie standard et le composant associé. La partie standard du dossier inclut les messages et les dossiers que les utilisateurs manipulent.
  
Le composant associé inclut des objets message masqués qui sont associés au dossier, y compris les définitions de formulaire, les affichages, les modèles de règle, les modèles de réponse, etc. Cet autre composant est appelé le tableau des contenus associés aux dossiers, et l'ensemble des messages dans le tableau des contenus associés est appelé informations associées au dossier. Les messages masqués font partie intégrante du dossier et sont copiés avec le contenu de dossier standard lorsque le dossier est copié. Bien qu'ils soient stockés physiquement sous forme de messages, les informations contenues dans la table de contenu associée à un dossier se comportent plus comme les messages affichables. Tout objet Folder qui prend en charge un tableau de contenu associé est capable de stocker des formulaires personnalisés. La méthode [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) peut renvoyer le contenu standard ou le contenu associé du dossier, en fonction de la valeur du paramètre _ulflags_ de la méthode. 
  
Une bibliothèque de formulaires se compose de définitions de formulaire stockées dans le tableau contenu associé d'un dossier. La définition du formulaire inclut les propriétés du formulaire, les actions prises en charge par le formulaire et même le fichier exécutable du serveur de formulaires, qui est stocké en tant que pièce jointe d'un ou de plusieurs messages.
  
En outre, les formulaires peuvent être stockés dans n'importe quel fichier ou emplacement pris en charge par le gestionnaire de formulaires. Le gestionnaire de formulaires par défaut stocke les serveurs de formulaires dans les dossiers MAPI, mais un gestionnaire de formulaires personnalisés peut implémenter son propre stockage pour les serveurs de formulaires.
  
Un formulaire peut avoir plusieurs interfaces utilisateur qui sont liées à sa classe de message. Par exemple, un formulaire peut avoir des interfaces utilisateur de composition et de lecture distinctes. Le formulaire s'occupe de l'appel de l'interface utilisateur appropriée pour différentes demandes utilisateur, en fonction de l'appel des verbes du formulaire. Par exemple, si votre serveur de formulaire comporte des interfaces utilisateur de composition et de lecture distinctes, l'interface utilisateur de composition peut être ouverte automatiquement lorsque l'utilisateur crée un message de la classe de message du formulaire et que l'interface utilisateur de lecture peut être ouverte automatiquement lorsque le un utilisateur ouvre un message existant de la classe de message du formulaire.
  
La plupart des informations stockées dans une définition de formulaire sont disponibles en appelant la méthode [IMAPIFormInfo:: IMAPIProp](imapiforminfoimapiprop.md) sur un objet **IMAPIFormInfo** . L'interface **IMAPIFormInfo** simplifie l'accès aux informations de formulaire en appelant toutes les méthodes de message et de dossier MAPI nécessaires pour extraire les informations. Un objet **IMAPIFormInfo** peut être obtenu en appelant la méthode [IMAPIFormContainer:: ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) . 
  
Les trois types de bibliothèques de formulaires sont décrits dans les [bibliothèques](local-form-libraries.md)de formulaires locaux, les bibliothèques de [formulaires de dossiers](folder-form-libraries.md) et les [bibliothèques de formulaires personnels](personal-form-libraries.md).
  
## <a name="see-also"></a>Voir aussi

- [Formulaires MAPI](mapi-forms.md)

